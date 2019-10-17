<template>
    <Box class="box" :pose="isVisible ? 'visible' : 'hidden'">
        <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
            viewBox="0 0 270 270" style="enable-background:new 0 0 270 270;" xml:space="preserve">
            <style type="text/css">
                .st0{fill:none;stroke:#03AEEF;stroke-width:3;stroke-miterlimit:10;}
                .st1{fill:none;stroke:#FD6A62;stroke-width:3;stroke-miterlimit:10;}
            </style>
            <circle class="st0" cx="135" cy="135" r="70.5"/>
            <circle class="st1" cx="135" cy="135" r="131.5"/>
        </svg>
    </Box>
</template>
    
<script>
import posed from 'vue-pose';

const config = {
  visible: {
    opacity: .3,
    scale: 1,
    transition: {
      opacity: { ease: 'easeInOut', duration: 1500 },
      scale: { ease: 'easeInOut', duration: 2000 }
    }
  },
  hidden: {
    opacity: 0,
    scale: 0,
    transition: {
      opacity: { ease: 'easeInOut', duration: 1500 },
      scale: { ease: 'easeInOut', duration: 2000 }
    }
  }
};

export default {
    data: () => ({ isVisible: false }),
    mounted() {
        setInterval(() => {
            this.isVisible = !this.isVisible;
        }, 2000);
    },
    components: {
        Box: posed.div(config)
    } 
}
</script>

<style lang="scss"scoped>
.box {
    margin: 100px;
    width: 300px;
    height: 300px;
    z-index: 1000;
}
</style>
