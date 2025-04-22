<script>
  import { base } from '$app/paths';

  let Elfrane = "elfrane.jpg"
  let Toya = "toya.jpg"
  let kapten = "kapten.jpg"
  let Kuro = "kuro.jpg"
  let kazutora = "https://i.pinimg.com/736x/15/8c/4c/158c4c18da0417aba909d811620b1238.jpg"
  let images = [Elfrane, Toya, kapten, Kuro, kazutora]
  let characters = []
  for(let i = 0; i < 5; i++){
      characters.push({image: images[i % 5]})
  }
</script>

<main>

  <section>
    <div class = "first">
      <button class="button">I'm a cool circle button</button>
      <button class = button_under>Bla</button>
    </div>
    <div class = "second">
      <img src="elfrane.jpg" alt = "Senku">
    </div>
    <div class= "third">
      <img src="https://pm1.aminoapps.com/7423/929f86920bfcef6bf9055e023dcc2a7ad7f3810cr1-1280-1721v2_hq.jpg" alt = "Senku" >
      <div class="tooltip">Information
        <span class="tooltiptext">
          <br> <b>Name: </b>Elfrane
          <br> <b>Age:</b> 18
          <br><b>Gender: </b>Female
          <a href="{base}/info"><br><b>More Information</a>
        </span>
      </div>
    </div>
</section>
	<div class = "container">
      {#each characters as character}
        <img src={character.image} alt = "karaktär" class ="name">
      {/each}
  </div>
</main>


<style>
  .tooltip .tooltiptext {
    visibility: hidden;
    
    cursor: pointer;
  }

  .tooltip{
    margin-left: 10px;
    width: 200px;
  }



  .tooltip:hover .tooltiptext {
    visibility: visible;
  }

  section{
    display: flex;
  }
    .button {
        /* Base styles */
        display: block;
        width: 1440px;
        height: 320px;
        border: none;
        cursor: pointer;
        

        /* Hide button caption text */
        overflow: hidden;
        color: transparent;

        /* The fill animation */
        background-image: url('kazutora.jpg');
        background-size: contain;

        /* Store the SVG in a variable so it's easy to use */
        --svg: url('data:image/svg+xml,\<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="black" fill-opacity="1" d="M0,160L1440,320L1440,0L0,0Z"></path></svg>');
        /* Chrome, still requires prefix in 2022 */
        -webkit-mask: var(--svg);
        mask: var(--svg);
    }
    
    .button_under {
      margin-top: -180px;
        /* Base styles */
        display: block;
        width: 1440px;
        height: 320px;
        border: none;
        cursor: pointer;

        /* Hide button caption text */
        overflow: hidden;
        color: transparent;

        /* The fill animation */
        background-image: url('https://i0.wp.com/senpai.com.mx/wp-content/uploads/2021/01/Dr.-Stone-celebra-el-cumpleanos-de-Senku-Ishigami.jpg?fit=1280%2C720&ssl=1');
        background-size: contain;

        /* Store the SVG in a variable so it's easy to use */
        --svg: url('data:image/svg+xml,\<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="black" fill-opacity="1" d="M0,32L1440,256L1440,320L0,320Z"></path></svg>');        /* Chrome, still requires prefix in 2022 */
        -webkit-mask: var(--svg);
        mask: var(--svg);
    }


    .first{
      width: 40px;
      height: 55vh;
      overflow-x: hidden;
      overflow-y: hidden;
      margin-left: 20px;
      margin-top: 20px;
      flex:1;
      border: solid 5px black;
      margin-bottom: 20px;
    }

    .second{
      width: 300px;
      height: 55vh;
      border: solid 5px black;  
      background-size: contain;
      margin: 20px;

    }

    .third{
      width: 200px;
      height: 55vh;
      border: solid 5px black;  
      background-size: contain;
      margin-top: 20px;
      margin-right: 20px;
    }

  
	main{
		background-color: rgb(255, 249, 242);
		height: 100vh;
		width: 70vw;
		justify-self: center;
    overflow-y: scroll;
    overflow-x: hidden;
    color: black;
}
.container{
  display: grid;
  grid-template-columns: 10fr 10fr 10fr;
  grid-template-rows: 10fr 10fr 10fr;
  gap: 20px;
  width: 1020px;
  justify-self: center;
  grid-column-start: span 2;
  grid-row-start: span 2;
  }

  .name{
    border: solid 5px black;
  }

</style>