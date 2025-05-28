<script>
  import { base } from '$app/paths';

  let Elfrane = "elfrane.jpg"
  let Toya = "toya.jpg"
  let kapten = "kapten.jpg"
  let Kuro = "kuro.jpg"
  let Yuhara = "Yuhara.jpg"
  let Kawada = "Kawada.jpg"
  let Arathorn = "arathorn.jpg"
  let Evindal = "evindal.jpg"
  let Filvendore = "filvendore.jpg"
  let Aetlin = "aithlin.jpg"
  let fillout = "fillout.jpg"
  let characters = [
    {image: Elfrane, name: "Elfrane", age: 18, gender: "Female",span:3, href: `${base}/elfrane`},
    {image: Toya, name: "Toya", age: 16, gender: "Female", span:6, href: `${base}/toya`},
    {image: kapten, name: "Kapten", age: 19, gender: "Female",span:4, href: `${base}/kapten`},
    {image: Kuro, name: "Kuro", age: 19, gender: "Female", span:5, href: `${base}/kuro`},
    {image: Kawada, name: "Kawada", age: 17, gender: "Female", span:5, href: `${base}/kawada`},
    {image: Yuhara, name: "Yuhara", age: 17, gender: "Female", span:5, href: `${base}/yuhara`},
    {image: fillout, span:2,href: `${base}`},
    {image: Aetlin, name: "Aithlin", age: 40, gender: "Female", href: `${base}/aithlin`},
    {image: Arathorn, name: "Arathorn", age: 19, gender: "male", href: `${base}/arathorn`},
    {image: Filvendore, name: "Filvendore", age: 45, gender: "male", span:1, href: `${base}/filvendore`},
    {image: Evindal, name: "Evindal", age: 19, gender: "male", span: 1, href: `${base}/evindal`},
  ]
</script>

<main>

  <section>
    <div class = "first">
      <div class="button" style="position:relative;">
        <div class="tooltip0">
          <h1>Information</h1>
          <ul class="tooltiptext0" id="kazutora">
            <li> <b>Name: </b> Kazutora</li>
            <li> <b>Age: </b> 18</li>
            <li> <b>Gender: </b> Female</li>
          </ul>
        </div>
      </div>

      <div class = "button_under" style="position:relative;">
        <div class="tooltip1">
          <h1>Information</h1>
          <ul class="tooltiptext1">
            <li> <b>Name: </b> Miko</li>
            <li> <b>Age: </b> 18</li>
            <li> <b>Gender: </b> Female</li>
            </ul>
        </div>
      </div>
    </div>

    <div class = "second" style="position:relative;">
      <img src="elidyr.jpg" alt = "Senku" >
        <div class="tooltip3">
          <h1>Information</h1>
            <ul class="tooltiptext3">
              <li> <b>Name: </b> Elidyr</li>
              <li> <b>Age: </b> 18</li>
              <li> <b>Gender: </b> Female</li>
              <a href="{base}/elidyr"><b>See More</a>
            </ul>
        </div>
    </div>

    <div class= "third">
      <div style="position:relative;">
        <img src="engell.jpg" alt = "Engell">
        <div class="tooltip2" >
          <h1>Information</h1>
          <ul class="tooltiptext2">
            <li> <b>Name: </b> Engell</li>
            <li> <b>Age: </b> Unkown</li>
              <li> <b>Gender: </b> Female</li>
            <nav>
              <a href="{base}/engell"><b>See More</a>
            </nav>
          </ul>
        </div>
      </div>
    </div>
</section>
	<div class = "container">
      {#each characters as character}
        <div class="persona" style="grid-row:span {character.span}">
          <img src={character.image} alt = "karaktär" class ="name" >
          <div class="tooltip">
            <h1>Information</h1>
            <ul class="tooltiptext">
              <li> <b>Name: </b>{character.name}</li>
              <li> <b>Age: </b>{character.age}</li>
              <li> <b>Gender: </b>{character.gender}</li>
              <nav>
                <a href="{character.href}"><b>See More</a>
              </nav>
            </ul>
          </div>
        </div>
      {/each}
  </div>

</main>


<style>
  .persona{
    position: relative;
    width: fit-content;
  }

  .tooltip0 .tooltiptext0 {
    visibility: hidden;
    
    
  }

  .tooltip0{
    margin-left: 10px;
    width: 120px;
    height: 5px;
    cursor: pointer;
    position: absolute;
    top:0%;
  }



  .tooltip0:hover .tooltiptext0 {
    visibility: visible;
    transform: scale(1.1);
    transition: transform 0.1s;
    width: 120px;
    height: 100px;
    background-color: white;
  }

  .tooltip1 .tooltiptext1 {
    visibility: hidden;
    
    
  }

  .tooltip1{
    margin-left: 10px;
    width: 120px;
    height: 5px;
    cursor: pointer;
    position: absolute;
    top:50%;
    left:20%
  }

  .tooltip1:hover .tooltiptext1 {
    visibility: visible;
    transform: scale(1.1);
    transition: transform 0.1s;
    width: 120px;
    height: 100px;
    background-color: white;
  }


  .tooltip .tooltiptext {
    visibility: hidden;
    
    
  }

  .tooltip{
    margin-left: 10px;
    width: 120px;
    height: 5px;
    cursor: pointer;
    position: absolute;
    top:0%;
  }



  .tooltip:hover .tooltiptext {
    visibility: visible;
    transform: scale(1.1);
    transition: transform 0.1s;
    width: 120px;
    height: 100px;
    background-color: white;
  }

  

  .tooltip2 .tooltiptext2 {
    visibility: hidden;
  }

  .tooltip2{
    margin-left: 10px;
    width: 120px;
    height: 5px;
    cursor: pointer;
    position: absolute;
    top:0%;
  }

  .tooltip2:hover .tooltiptext2 {
    visibility: visible;
    transform: scale(1.1);
    transition: transform 0.1s;
    width: 120px;
    height: 100px;
    background-color: white;
  }

  .tooltip3 .tooltiptext3 {
    visibility: hidden;
    
    
  }

  .tooltip3{
    margin-left: 10px;
    width: 120px;
    height: 5px;
    cursor: pointer;
    position: absolute;
    top:0%;
  }



  .tooltip3:hover .tooltiptext3 {
    visibility: visible;
    transform: scale(1.1);
    transition: transform 0.1s;
    width: 120px;
    height: 100px;
    background-color: white;
  }


  section{
    display: flex;
  }
    .button {
        /* Base styles */
        display: block;
        width: 1440px;
        height: 320px;
        
        /* The fill animation */
        background-image: url('kazutora.png');
        background-size: 25%;

        /* Store the SVG in a variable so it's easy to use */
        --svg: url('data:image/svg+xml,\<svg xmlns="http://www.w3.org/2000/svg" viewBox="-0 0 1440 320"><path fill="black" fill-opacity="1" d="M0,160L1440,320L1440,0L0,0Z"></path></svg>');
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

        /* The fill animation */
        background-image: url('miko.jpg');
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
      background-size: cover;
      overflow-y: hidden;
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
    border: solid 5px black;
    font-family:'Times New Roman', Times, serif;

}
.container{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: repeat(auto, 16px);
  gap: 20px;
  width: 1020px;
  justify-self: center;
  }

  .container img{
    width: 100%;
    height: fit-content;
    object-fit: contain;
    border: solid 5px black;

  }

  /* .container img:nth-child(even){
    grid-row: span 2;
  } */
   .container .persona:nth-child(8){
    grid-column: span 3;
    grid-row: span 1;
  }

  .container .persona:nth-child(9){
    grid-column: span 2;
    grid-row: span 12;
  }

  /* .container .persona:active{
    transform: scale(1.1);
    transition: transform 0.1s;
  } */

  @media (max-width: 1300px) {
    .first{
      display: none;
    }
    .second{
      display: none;
    }
    .third{
      display: none;
    }
    .container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      width: 100%;
      gap: 5px;
    }
    .container img {
      margin-top: 5px;
      width: 100%;
      height: auto;
      margin-left: 5px;
      margin-right: 5px;
    }
    .container .persona:nth-child(8) {
      grid-column: span 2;
      grid-row: span 1;
    }
    .container .persona:nth-child(9) {
      grid-column: span 2;
      grid-row: span 12;
    }

  }

</style>