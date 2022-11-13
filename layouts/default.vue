<template>
  <div >
    <AppHeader/>
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
    margin: 0;
  }
  p, h1, h2, h3, h4, h5, h6{
    font-family: Arial, Helvetica, sans-serif;
    color: rgb(54, 54, 54);
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
    border: 1px solid rgb(232, 232, 232);
    
}
  @media screen and (max-width: 800px) {
    .pagecontent{
      width: calc(100% - 4rem);
      margin-inline: 0;
      padding-inline: 2rem;
      border-left: 0px;
      border-right: 0px;
      border-radius: 0px;
    }
    
  }

/* Page Transitions */
.page-enter-active,
.page-leave-active {
  transition: opacity filter 600ms cubic-bezier(.42,0,1,1);
}

.page-leave-active {
  opacity: 0;
  
}
.page-enter{
  opacity: 0;

}


</style>