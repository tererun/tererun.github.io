<template>
	<div id="app">
		<div class="wrapper">
			<div class="container">
				<div class="icon-gif">
					<img src="./assets/eyes.gif" alt="eyes" id="icon-eyes">
					<img src="./assets/tererun.png" alt="tererun" id="icon-tererun">
				</div>
				<div class="links">
					<a href="https://twitter.com/tererun1" target="_blank"><fa-icon :icon="['fab', 'twitter']" /></a>
					<a href="https://www.youtube.com/channel/UCli9iNco_SDFNRJz1DjkTNQ" target="_blank"><fa-icon :icon="['fab', 'youtube']" /></a>
					<a href="https://github.com/tererun" target="_blank"><fa-icon :icon="['fab', 'github']" /></a>
				</div>
			</div>
		</div>		
	</div>
</template>

<script>
export default {
	name: 'App',
	mounted() {
		document.body.addEventListener('mousemove', e => {
			const windowHalfWidth = window.innerWidth / 2;
			const windowHalfHeight = window.innerHeight / 2;
			const icon = document.getElementById("icon-eyes");
			const calcedX = ((e.x / windowHalfWidth) - 1) * 3;
			const calcedY = ((e.y / windowHalfHeight) - 1) * 3;
			icon.style.left = calcedX + "px";
			icon.style.top = calcedY + "px";
		});
	}
}
</script>

<style>
body {
	margin: 0;
	font-family: 'Noto Sans JP', sans-serif;
	user-select: none;
	background-color: #8fc5a2;
	overflow: hidden;
}

a {
    text-decoration: none;
    color: white;
}

img {
    -webkit-user-drag: none;
}

.wrapper {
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.container {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.icon-gif {
	position: relative;
}

img#icon-tererun {
    width: 200px;
    display: inline-block;
}

img#icon-eyes {
	width: 200px;
	position: absolute;
}

.links {
    color: white;
    font-size: 150%;
    margin-top: 5px;
}

.links a {
    margin: 0% 10px;
}
</style>
