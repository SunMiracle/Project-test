<template>
	<div class="HomeList">
		<div class="HomeListTab">
			<h3 id="HomeListTabTitle">{{title}}</h3>
		</div>	
	</div>	
</template>

<script type="text/javascript">
	export default{
		name: 'Home',
		data(){
			return{
				title: '产品列表',
				detail:[
					{
						title: '手游产品'
					}
				]
			}
		}
	}
	function s(argument) {
		// body...
	}
</script>
<style type="text/css">
	#HomeListTabTitle{
		font-size: 28px;
	    color: #282a29;
	    display: flex;
	    align-items: center;
	}
	#HomeListTabTitle:before{
		content: ' ';
	    background: red;
	    width: 5px;
	    height: 25px;
	    display: block;	
	    float: left;
	    margin-right: 10px;
	    align-items: center;
	}
	.HomeList{
		padding: 20px 20px;
	}
</style>



