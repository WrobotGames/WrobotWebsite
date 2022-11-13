<template>
  <div class="joke">
    <p>{{ joke }}</p>
  </div>
</template>

<script>
export default {
    name: 'Joke',
    props: ['joke', 'id']
}
</script>

<style>
.joke {
  border-top:2px solid rgb(76, 117, 176);
  display: flex;
  align-items: center;
  padding: 10px;
  margin-top: 20px;
  margin-bottom: 20px;
  margin-left: 15%;
  margin-right: 15%;
  line-height: 20px;
  height: 100px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
  background: white;
  transition: all 0.4s cubic-bezier(.24,.07,.27,1);
  border-radius: 15px;
  
}
@media screen and (max-width: 800px) {
    .joke{
      margin-left: 0.75rem;
      margin-right: 0.75rem;
    }
    
  }


.joke:hover{
  border-radius: 15px;
  border-top: 8px solid rgb(76, 117, 176);
  height: 110px;
  line-height: 20px;
  box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
  border-radius: 15px;
}
</style>