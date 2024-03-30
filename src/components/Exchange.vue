<script>
export default {
  data() {
    return {}
  }
//   methods:{
//     typeCurrency(event){
//         console.log(event.target.value);
//     }


//     }
  };

</script>

<template>
  {{ Exchange }}
  <div>AMD -> USD կամ USD -> AMD</div>
  <br />
  <div>
    <input type="text" @input="typeCurrency" />
    <input type="text" @input="typeCurrency" />
  </div>
  <br /><br />
  <button>AMD -> USD կամ USD -> AMD</button>
</template>

<style scoped></style>
