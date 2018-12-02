<template>
<form v-on:submit.prevent="bookSubmit(bookTitle,bookAuthor)" class="">
  <input v-model="bookTitle" type="text" name="title" value="" placeHolder="bookTitle">
  <input v-model="bookAuthor" type="text" name="author" value="" placeHolder="bookAuthor">
  <button type="submit" name="button">Add</button>
</form>
</template>
<script>
export default {
  name: 'BookForm',
  props: ['books'],
  data() {
  return {
   bookTitle:'',
   bookAuthor:''
  }
},
methods:{
bookSubmit(bookTitle,bookAuthor)
{
  this.$emit('addBook',bookTitle,bookAuthor);
}
},
}
</script>
<style>
</style>
