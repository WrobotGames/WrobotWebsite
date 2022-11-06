<template>
  <div >
    <AppHeader />
    <nuxt/>
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader';
export default {
    components: {
        AppHeader
    }

}
</script>

<style>
  body{
    background: rgb(243, 244, 246);
  }
  p{
    font-family: Arial, Helvetica, sans-serif;
  }
  h1{
    font-family: Arial, Helvetica, sans-serif;
  }

  .center {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .pagecontent {
    border-radius: 15px;
    
    padding: 1rem;
    margin-left: 15%;
    margin-right: 15%;
    background: white;
    transition: all 0.4s cubic-bezier(.24,.07,.27,1);
    border: 1px solid rgb(232, 232, 232);
    
}
  @media screen and (max-width: 800px) {
    .pagecontent{
      width: calc(100% - 16px);
      border-left: 0px;
      border-right: 0px;
      border-radius: 0px;
      margin-left: -8px;
      margin-right: -8px;
      
    }
    
  }

  
.page-enter-active,
.page-leave-active {
  transition: opacity transfrom 200ms cubic-bezier(.42,0,1,1);
}

.page-leave-active {
  opacity: 0;
  transform: translate(100px, 0px);
  
}
.page-enter{
  opacity: 0;
  transform: translate(-100px, 0px);

}


</style>