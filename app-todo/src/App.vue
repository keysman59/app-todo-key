<template>
  <div id="app">
  
    <div class="category" style="display:flex;">
      <h4 v-if="visibleCaption" @click.prevent="hideCaption" class="category-caption">{{text}}</h4>
      <div class="category-block" v-if="!visibleCaption">
        <input v-model.lazy="text" class="category-input" type="text" />
        <button href="#" @click.prevent="onClick" class="category-btn">Отправить</button>
      </div>
      <div style="">
        <i class="fa fa-plus-circle"></i><h6>Добавить еще категорию...</h6>
      </div>

      <p>visibleCaption:{{visibleCaption}}</p>  
      <p>visibleBlock:{{visibleBlock}}</p>
      <!-- <p>afterText:{{afterText}}</p>
      <p>onClick():{{onClick()}}</p> -->
      
    </div>
<!-- <input type="text"> -->
  </div>
</template>

<script>
export default {
  name: 'app',
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

<style>

body {
  font-family: Arial;
}

.category-caption {
  background: #f8f9fa;
  border-color: #f8f9fa;
  color: #212529;
  width: 30%;
  display: block;
  cursor: pointer;
  padding: 1.2em;
}

.category-block {
  background: #f8f9fa;
  border-color: #f8f9fa;
  color: #212529;
  width: 30%;
  display: block;
  cursor: pointer;
  padding: 1.2em;
}

.category-caption:hover {
  color: #212529;
  background-color: #dae0e5;
  border-color: #d3d9df;
}

</style>
