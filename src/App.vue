<template>
<form class="input">
  <input type="text" placeholder="Название">
  <input type="text" placeholder="Описание">
  <button class="btn">Создать</button>
</form>
<div class="post" v-for="post in posts">
<div><strong>Название:</strong> {{post.title}}</div>
<div><strong>Описание:</strong> {{post.body}}</div>
</div>
</template>

<script>
export default {
 data() {
  return {
    posts: [
      {id: 1, title: "JavaScript 1", body: "Описание 1"},
      {id: 2, title: "JavaScript 2", body: "Описание 2"},
      {id: 3, title: "JavaScript 3", body: "Описание 3"},
    ]
  }
 },
}
 
</script>

<style>
* {
    margin: o;
    padding: 0;
    box-sizing: border-box;
}
.post {
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
}
.btn {
  margin: 10px;
  padding: 10px;
  border: 2px solid teal;
  background: none;
  margin-top: 15px;
}
.input {

}

</style>