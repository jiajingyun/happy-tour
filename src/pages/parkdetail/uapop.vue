<template>	
	<a class="download" :style="this.deltaY?'display:none':'display:inline-block'" @click="downloadapp"></a>	
</template>

<script>
	import detect from '../../brower-version/browVersion.js'
	export default {
		data () {
			return {				
			}		
		},
		props:["deltaY"],
		methods:{
			downloadapp: function(){
				console.log(detect.os);
				if( detect.os == 'iOS'){
        			window.open("https://itunes.apple.com/cn/app/id395096736");
      			}else if(detect.os == 'Android'){
        			window.open("https://play.google.com/store/apps/details?id=com.Qunar&hl=zh", "_self");
      			}else if(detect.os != 'iOS' || 'Android'){
        			window.open("http://app.qunar.com/");
     		 	}
    		}			
		}		
	}
</script>

<style scoped>
.download {
    display: none;
    position: fixed;
    top: 7.5rem;
    left: 0;
    width: 1.36rem;
    height: 1.15rem;
    z-index: 98;
    background: url(data:image/png;base64,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);
    background-size: 1.36rem 1.15rem;
}
</style>