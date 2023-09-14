<template>
    <div>
        <table-component :headers="data" :data="data"/>
    </div>
</template>

<script>
import axios from 'axios'
import TableComponent from './TableComponent.vue'

export default {
  components: {TableComponent },
    data() {
        return {
            data: [],
        }
    },
    mounted() {
        axios.get('https://api.coincap.io/v2/assets')
        .then(res => this.data = res.data.data)
        .catch(e => console.log(e))        
    },
}
</script>

<style scoped>

</style>