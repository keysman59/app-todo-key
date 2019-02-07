<template>
  <div class="wrapper">
    <!-- Wrapper-caption -->
    <div class="top-block">

      <div class="left-block">
        <h4 class="top-block__caption" v-if="visibleCaption" @click.prevent="hideCaption" >{{text}}</h4>
        <div class="category-block" v-if="!visibleCaption">
          <input v-model.lazy="text" class="category-block__input" type="text" />
          <button href="#" @click.prevent="onClick" class="category-block__btn">Отправить</button>
        </div>
      </div>

      <div class="add-field">
        <i class="fa fa-plus-circle add-field__icon"></i><h4 class="add-field__caption">Добавить еще категорию...</h4>
      </div>  
    </div>

    <!-- Add-project -->
    <div class="add-project">
      <i class="fa fa-plus-circle add-project__icon"></i>
    </div>





<!-- 
    <p>visibleCaption:{{visibleCaption}}</p>  
    <p>visibleBlock:{{visibleBlock}}</p> -->
    <!-- <p>afterText:{{afterText}}</p>
    <p>onClick():{{onClick()}}</p> -->

  </div>
<!-- <input type="text"> -->
</template>

<style lang="scss">
 @import "../styles/views/About.scss";
</style>


<script>
export default {
  data () {
    return {
      visibleCaption: true,
      visibleBlock: false,
      text: "Категории",
    }
  },
  methods: {
    hideCaption(){
      this.visibleCaption = false;
      // if(this.visibleCaption == true || this.visibleBlock == true) {
      //   this.visibleCaption = false;
      //   this.visibleBlock = true;
      // } else {
      //   this.visibleCaption = true;
      //   this.visibleBlock = false;
      // }
    },
    // hideCaption(){
    //   if(this.visibleCaption == true || this.visibleBlock == true) {
    //     this.visibleCaption = false;
    //     this.visibleBlock = true;
    //   } else {
    //     this.visibleCaption = true;
    //     this.visibleBlock = false;
    //   }
    // },
    onClick() {
      this.visibleCaption = true;
      // this.visibleBlock = false;
      // return this.text;
    }
    // onClick() {
    //   let afterText;
    //   afterText = this.text;
    //   return afterText;
    // }
    // hideBlock(){
    //   if() {
      
    //   }
    // },    
  }
}
</script>


