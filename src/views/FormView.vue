<template>
    <div>
        <button class="p-2 bg-slate-400" @click="dropdown=!dropdown">menu</button>
        <div>this is dropdown</div>
    </div>
    <div> this is onchange </div>
    <input type="text" @change="count++" class="p-2 vorder-2">
    <div>
        count is {{count}}
    </div>
</template>

<script>
export default {
    data(){
        return{
            dropdown: false
        }
        return{
            count: 0
        }
    }
}
</script>

<style>

</style>