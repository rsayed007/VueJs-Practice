<template>
    <div class="card">
        <div class="card-header">Price Table</div>
        <ul class="list-group list-group-flush">
            <li v-for="(item, index) in items" :key="index" class="list-group-item">
                <button @click="removeItem(index)" class="btn text-danger float-left">x</button><span class="float-left">{{item.title}}</span>  <span class="text-success float-right">${{item.price}}</span>
            </li>
            <!-- <li class="list-group-item">Item 2</li> -->
            <hr>
            <li class="list-group-item">
                <span class="float-left">Total</span>  <span class="text-success float-right"><b>${{totalPrice}}</b></span>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props:['items'],
    computed: {
        totalPrice(){
            var total = 0
            this.items.forEach(item => {
                total = total + parseFloat(item.price)
            })
            return total
        }
    },
    methods: {
        removeItem(index){
            this.$emit('itemRemove', index)
        }
    }
}
</script>

<style>

</style>
