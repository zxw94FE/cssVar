<template>
	<div class="tab-navbar">
		<nav>
			<a v-for="(v, i) in list" :key="v" :class="{ active: index === i }" @click="select(i)">标题{{i + 1}}</a>
		</nav>
		<div>
			<ul ref="tabs" :style="`--tab-count: ${list.length}`">
				<li v-for="(v, i) in list" :key="v" :style="`--bg-color: ${v}`">内容{{i + 1}}</li>
			</ul>
		</div>
	</div>
</template>

<style lang="scss">
.tab-navbar {
	display: flex;
	overflow: hidden;
	flex-direction: column-reverse;
	border-radius: 10px;
	width: 300px;
	height: 400px;
	nav {
		display: flex;
		height: 40px;
		background-color: #f0f0f0;
		line-height: 40px;
		text-align: center;
		a {
			flex: 1;
			cursor: pointer;
			transition: all 300ms;
			&.active {
				background-color: #66f;
				font-weight: bold;
				color: #fff;
			}
		}
	}
	div {
		flex: 1;
		ul {
			--tab-index: 0;
			--tab-width: calc(var(--tab-count) * 100%);
			--tab-move: calc(var(--tab-index) / var(--tab-count) * -100%);
			display: flex;
			flex-wrap: nowrap;
			width: var(--tab-width);
			height: 100%;
			transform: translate3d(var(--tab-move), 0, 0);
			transition: all 300ms;
		}
		li {
			display: flex;
			justify-content: center;
			align-items: center;
			flex: 1;
			background-color: var(--bg-color);
			font-weight: bold;
			font-size: 20px;
			color: #fff;
		}
	}
}
</style>

<script>
export default {
	name: "tab-navbar",
	data() {
		return {
			index: 0,
			list: ["#f66", "#09f", "#3c9"]
		};
	},
	methods: {
		select(i) {
			this.index = i;
			this.$refs.tabs.style.setProperty("--tab-index", i);
		}
	}
};
</script>