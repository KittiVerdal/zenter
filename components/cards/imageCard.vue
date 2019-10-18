<template>
<div>
<b-container>
      <b-row>
        <b-col md="3">
            <div class="image" v-for="injuries in injuries" :key="injuries.id" @mouseover="hovered = injuries.id" @mouseleave="hovered = null">
            <transition name="fade">
                <div class="overlay" v-if="hovered === injuries.id">
                </div>
            </transition>
            <img :src="injuries.path" :alt="injuries.alt" :title="injuries.titleattr"/>
            <h3>{{injuries.category}}</h3>
            <h2>{{injuries.title}}</h2>
        </div>
        </b-col>
      </b-row>
</b-container>
</div>
</template>

<script>
export default {
    data:{
        injuries: [ 
            {id:1,
            path:'~/assets/images/ryggsmerter.jpg',
            category:'Plager/Lidelser',
            title: 'Rygg og muskelsmerter',
            alt:'Dame med vond rygg',
            titleattr:'Dame med vond rygg',
            link:'/behandlinger',
            
            },
            {id:2,
            path:'~/assets/images/migrene.jpg',
            category:'Plager/Lidelser',
            title: 'Migrene eller hodepine',
            alt:'Middelaldrene dame med vondt i hode',
            titleattr:'Middelaldrene dame med vondt i hode',
            link:'/behandlinger',
            
            }


        ],
        hovered: null,
    }
    
}
</script>

<style lang="scss" scoped>
a{
    cursor: pointer;
}
.overlay {
	background: rgba($secondaryDark, .7);
    height:100%;
    width:100%;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}

</style>