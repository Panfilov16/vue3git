<template>
   <form @submit.prevent >
  <h4>Создание поста</h4>
  <input 
  v-model="post.title" 
  class="input" 
  type="text" 
  placeholder="Название">
  <input 
  v-model="post.body" 
  class="input" 
  type="text" 
  placeholder="Описание">
  <button 
  class="btn" 
  @click="createPost"
  >
    Создать
  </button>
</form>
</template>

<script>
    export default {
        data(){
          return {
            post: {
              title: '',
              body: '',
            }
          }
        },
       methods: {
        createPost() {
      this.post = Date.now();
      this.posts.push(newPost);
      this.title = "";
      this.body = "";
       },
    }
    }
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}

.input {
 width: 100%;
 border: 2px solid teal;
 padding: 10px 15px;
 margin-top: 15px;
}
.btn {
  align-self: flex-end;
  padding: 10px 15px;
  border: 2px solid teal;
  background: none;
  margin-top: 15px;
  color: teal;
}
</style>