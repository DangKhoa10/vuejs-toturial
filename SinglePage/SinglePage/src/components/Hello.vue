<script>
export default {
    name: "Hello",
    props: {
        mes: String,
        
    },
    data() {
        return {
            name: "OKla",
            isShow: false
        }
    },
    methods: {
        onchange(){
            this.isShow = !this.isShow
        },
        onClickComponent(){
            this.$emit("clickComponent")
        }
    },
    computed: {
       changeName(){
        return this.name + "aaaa"
       }
    }
}
</script>

<template>
    <div v-if="isShow">
        {{ changeName }}
    </div>
    <button @click="onchange">
        Click
    </button>
    <button @click="onClickComponent">onUp</button>
    <div>
        {{ name }}
    </div>
    <h5>{{ mes }}</h5>
</template>

<style scoped></style>