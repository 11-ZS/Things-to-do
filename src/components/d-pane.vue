<template>
    <div v-show="show">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: "pane",
    props: {
        label: {
            type: String
        },
        flag: {
            type: [String,Number]
		},
	 
	},
	data(){
		return {
			show:true
		}
	}
};
</script>

<style>
</style>
