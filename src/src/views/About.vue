<template>
	<div>
		<div class="about">
		  <h1 class="h">This is an about page</h1>
		</div>
		<div class="box">hello world</div>
		<div class="message">message</div>
		<div class="error">error</div>
		<div class="warning">warning</div>
		<div class="main">
			<a href="/">hello world</a>
		</div>
		<div class="width">width</div>
		<div class="width">width</div>
	</div>
</template>
<style lang="scss">
@import "../assets/css/about.scss"; //scss引入
	.about{ // 嵌套
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
	@mixin transform($property) { // 混入
		-webkit-transform: $property;
		-ms-transform: $property;
		transform: $property;
	}
	.box { @include transform(rotate(30deg)); }
	
	
    .message { // 继承
		@extend %message-shared;
}

   .success {
	   @extend %message-shared;
	   border-color: green;
}

   .error {
       @extend %message-shared;
	   border-color: red;
}

  .warning {
       @extend %message-shared;
       border-color: yellow;
}	
   .main{
	  @extend %main-shared;
	  a{
		text-decoration: none;
		font-size: 18px;
		color: $color;
		&:hover{ // &引用父级选择器的关键字
			color:red;
		}
	}
}
	.width{
	  //font-size: 10px/8px;             // 纯 CSS，不是除法运算
	  width: $width/2.5;            // 使用了变量，是除法运算
	  //width: round($width)/2;        // 使用了函数 变量，是除法运算
	  height: (500px/2);          // 使用了圆括号，是除法运算
	  margin: 4px + 8px/2px 0; // 使用了加（+）号，是除法运算
	  float: left;
	  line-height: 250px;
	  background-color: #eee;
	  margin: 5%;
}
</style>