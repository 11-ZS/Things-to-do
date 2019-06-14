<template>
  <div class="body">
    <div class="container">
      <div class="type">
        <div class="buttons">
          <d-button type="top-label" @click="clickk">一般事务</d-button>
          <d-button type="top-label" go="/tomorrow">明日事务</d-button>
        </div>
        <div class="content">
          <router-view/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import dButton from "../components/d-button.vue";
export default {
  name: "HelloWorld",
  components: {
    dButton
  },
  props: {
    msg: String
  },
  methods:{
	  clickk(){
		  console.log('click....');
	  }
  }
};
</script>
 
<style >
body,
html {
  height: 100%;
  border: 1px solid black;
}
.body {
  position: relative;
  width: 100%;
  height: 100%;
  border: 1px solid blue;
}
.container {
  position: relative;
  border: 1px solid red;
  width: 800px;
  margin: 0px auto;
}

.content {
  height: 100px;
  border: 1px solid pink;
  margin-top: -1px;
}
</style>
