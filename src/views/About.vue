<template>
  <div class="about">
    <h1 class="h">This is an about page</h1>
  </div>
</template>
<style lang="scss">
@import "../assets/css/about.scss"; //scss引入
	.about{
		background: #eee;
		height: 60px;
		line-height: 60px;
		.h{
			color: $color;
			font-weight: bold;
			font-size: 20px;
			font: $font-stack;
		}
	}
</style>