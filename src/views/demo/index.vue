<template>
    <div class="app-container">
      1111
    </div>
  </template>
  
  
  <script>
  import service from '@/utils/request'
  export default {
    data() {
      return {
        form: {
          name: '',
          region: '',
          date1: '',
          date2: '',
          delivery: false,
          type: [],
          resource: '',
          desc: ''
        }
      }
    },
    created() {
        this.getData()
    },
    methods: {
        getData() {
            service.post("1111").then(ret => {
            console.log(ret)
        })
        console.log(222)
      },
      onSubmit() {
        this.$message('submit!')
      },
      onCancel() {
        this.$message({
          message: 'cancel!',
          type: 'warning'
        })
      }
    }
  }
  </script>
  
  <style scoped>
  .line{
    text-align: center;
  }
  </style>
  
  