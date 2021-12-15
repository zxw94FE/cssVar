<template>
	<div class="index-page">
		<header>
			<h1>CSS 变量</h1>
		</header>
		<main>
			<div class="flex-ct-x">
				<strip-loading></strip-loading>
			</div>
			<div class="flex-ct-x">
				<heart-loading></heart-loading>
			</div>
			<div class="flex-ct-x">
				<tab-navbar></tab-navbar>
			</div>
			<div class="flex-ct-x">
				<track-btn></track-btn>
			</div>
			<div class="flex-ct-x">
				<parallax-btn></parallax-btn>
			</div>
			<div class="flex-ct-x">
				<like-btn></like-btn>
			</div>
		</main>
	</div>
</template>

<style lang="scss">
.index-page {
	display: flex;
	overflow: hidden;
	flex-direction: column;
	height: 100vh;
	background-color: #282c34;
	transform: perspective(800px);
	header {
		height: 100px;
		line-height: 100px;
		text-align: center;
		h1 {
			background-image: linear-gradient(92deg, #f66 0%, #f90 100%);
			background-clip: text;
			font-size: 50px;
			color: #f66;
			animation: hue 60s infinite linear;
			-webkit-text-fill-color: transparent;
		}
	}
	main {
		$width: calc(100% / 3);
		display: grid;
		flex: 1;
		grid-template-columns: $width $width $width;
		grid-template-rows: 50% 50%;
		padding: 20px;
		> div {
			overflow: hidden;
			border: 1px solid #fff;
		}
	}
}
@keyframes hue {
	from {
		filter: hue-rotate(0);
	}
	to {
		filter: hue-rotate(-360deg);
	}
}
</style>

<script>
import HeartLoading from "./components/heart-loading";
import LikeBtn from "./components/like-btn";
import ParallaxBtn from "./components/parallax-btn";
import StripLoading from "./components/strip-loading";
import TabNavbar from "./components/tab-navbar";
import TrackBtn from "./components/track-btn";

export default {
	components: {
		HeartLoading,
		LikeBtn,
		ParallaxBtn,
		StripLoading,
		TabNavbar,
		TrackBtn
	}
};
</script>