---
layout: page
title: Präsentation
group: navigation
---

<script type="text/javascript">
<!--

	function init(){
		removeHuds();	
		forceRedraw();
	}

	function next(){
		links.gShowController.advanceToNextBuild('tapNextButton');
		rechts.gShowController.advanceToNextBuild('tapNextButton');
	}

	function last(){
		links.gShowController.goBackToPreviousSlide("tapPreviousButton");	
		rechts.gShowController.goBackToPreviousSlide("tapPreviousButton");	
	}

	function removeHuds(){
		element = links.document.getElementById("hud");
		element.parentNode.removeChild(element);

		element = rechts.document.getElementById("hud");
		element.parentNode.removeChild(element);

		links.kHeightOfHUD = 0;
		rechts.kHeightOfHUD = 0;
	}
	
	function forceRedraw(){
		var newHeight=$("#links").height()+1;
		$("#links").height(newHeight);
		$("#rechts").height(newHeight);
	}

	$(function() {
			setTimeout(init,1000);
			setTimeout(init,2000);
			setTimeout(init,3000);
			setTimeout(init,4000);
			setTimeout(init,5000);
			//pollForReadySlideshows();
	});
	

	var linksIsDone = false;
	var rechtsIsDone = false;
	function pollForReadySlideshows(){

		if(links && links.$ && links.$("waitingSpinner") && links.$("waitingSpinner").display() != 'none'){
			linksIsDone = true;
		}

		if(rechts && rechts.$ && rechts.$("waitingSpinner") && rechts.$("waitingSpinner").display() != 'none'){
			rechtsIsDone = true;
		}

		if(linksIsDone && rechtsIsDone){
			alert("Hello World");
			init();
		}else{
			setTimeout(pollForReadySlideshows,100);
		}
	}

-->
</script>

<table style="position:relative; left:50%; margin-left:-512px; width:1024px; height:384px">
	<tbody>
		<tr>
			<td width="50%">
				<iframe id="links" width="100%" height="100%" src="/assets/Pseydonym_links/assets/player/KeynoteDHTMLPlayer.html">Test links</iframe>
			</td>
			<td width="50%">
				<iframe id="rechts" width="100%" height="100%" src="/assets/Pseydonym_rechts/assets/player/KeynoteDHTMLPlayer.html">Test rechts</iframe>
			</td>
		</tr>
	</tbody>
</table>

<div class="btn-group" style="left:50%; margin-left: -42px">
<div href="#" id="hudPreviousButton" class="btn btn-large btn-inverse" onClick="javascript:last()"><i class="icon-step-backward icon-white"> </i></div>
<div href="#" id="hudNextButton" class="btn btn-large btn-inverse" onClick="javascript:next()"><i class="icon-step-forward icon-white"> </i></div>
</div>
