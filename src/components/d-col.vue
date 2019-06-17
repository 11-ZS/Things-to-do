<template>
	<div ref='col' class="d-col">
		<slot></slot>
	</div>
</template>

<script>
export default {
	name:"d-col",
	props:{
		sw:{
			type:Number
		},
		mw:{
			type:Number
		},
		lm:{
			type:Number
		},
		xlm:{
			type:Number
		},
		span:{
			type:Number
		}
	},
	data(){
		return {
			 spanLimit:24
		}
	},
	methods:{
		init(info){
			for(var key in info){
				var value = info[key]
					console.log(typeof(typeof value))
				if(typeof value==="number"){
					// this.$refs.col.style[key]=info[key]/24*this.span+'px';
					this.$refs.col.style[key]=100+'px';
				}else{
					// this.$refs.col.style[key]=info[key]/24*this.span;
					this.$refs.col.style[key]=100

				}
				 
			}	
		}
	}
}
</script>

<style>
.d-col{
	display:  inline-block;
}
</style>
