<template>
   <div class="sticky-container">
      <ul class="sticky">
        <li>
          <img width="32" height="32"  src="telegram.png" />

        </li>
        <li>
          <img width="32" height="32"  src="discord.png" />

        </li>
        <li>
          <img width="32" height="32"  src="Twitter.png" />

        </li>
        <li>
          <img width="32" height="32"  src="fb.png" />

        </li>
        <li>
          <img width="32" height="32"  src="youtube.png" />
        </li>
         <li>
          <img width="32" height="32"  src="tik.png" />
        </li>
         <li>
          <img width="32" height="32"  src="medium.png" />
        </li>
      </ul>
    </div>
<!--Right Side Buttons End-->
</template>
<style>
	body{
		font-family: "Lato";
    background-image: linear-gradient( to left, #ad5389, #3c1053);
	}

/*Right Side Buttons Start*/
	.sticky-container{
		padding: 0px;
		margin: 0px;
		position: fixed;
		top: 50vh;
		width: 50px;
	}

  .sticky{
    border-radius: 20px;
     background-color: #ff6e00;
     margin-left: 30px;
     position: absolute;
     padding: 30px;
     padding: 10px 12px;
    -webkit-border-radius: 30px;
    border-radius: 30px;
  }

	.sticky li{
		list-style-type: none;
		color: #efefef;
		height: 43px;
		cursor: pointer;


	}

/*Right Side Buttons End*/

</style>

<script>
export default {
  name: "Social",
};
</script>
