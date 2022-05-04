<template>
    <section>
        <div class="wrapper">
            <div>--> Content Goes Here &lt;--</div>
        </div>
    </section>
</template>

<script>


export default {
    name: 'AppContent' 
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables';

   section{
       width: 100%;
       background-color: $bg-black;
       color: white;
   }
   .wrapper{
       padding: $section-padding;
       @include wrapper;
   }
    
</style>