<script>
    let currentOutfit = "ev.png";
    let warriorOutfit = "evi.png";
    
    function warrior(){
        currentOutfit = warriorOutfit;

    }
    
    function normal() {
        currentOutfit = "ev.png";

    }

</script>

<main>
    <fieldset>
        <legend>Evindal</legend>
            <ul> 
                <li><b>Name:</b> Evindal</li>
                <li><b>Last name:</b> Everya</li>
                <li><b>Age:</b> 19</li>
                <li><b>Genre:</b> Fantasy</li>
                <li><b>Species:</b> Elf</li>
                <li><b>Details: How I got my scar?</b> An arrow to the eye and a sword sliced over my cheek. Yes, that is how it happend. Why? Are you surpriesed? 
                    <br> Oh, the others told you stories about how they got them? Well, I got mine in a fight agianst the politic elves. 
                    <br> </li>
            </ul>
    </fieldset>
    

    <div>
        <img src={currentOutfit} alt="Elfrane" >
    </div>
    {#if currentOutfit === "ev.png"}
        <button class="warriorOutfit" on:click={(warrior)}>Warrior outfit</button>
    {:else}
        <button class= "normal" on:click={(normal)}>Normal outfit</button>
    {/if}
    

</main>


<style>
    .warriorOutfit{
        background-image: url("https://static.vecteezy.com/system/resources/thumbnails/050/573/369/small_2x/a-black-crow-flying-on-a-transparent-background-with-wings-fully-extended-png.png");
        /* background-image: url("https://png.pngtree.com/png-clipart/20230825/original/pngtree-silhouette-of-flying-seagulls-picture-image_8772645.png"); */
        background-size: cover;
        width: 200px;
        height: 200px;
        margin-top: 200px;
        color: white;
    }

    .normal{
        background-image: url("https://png.pngtree.com/png-vector/20231123/ourmid/pngtree-flying-swallow-bird-png-image_10705469.png");
        background-size: cover;
        width: 200px;
        height: 200px;
        margin-top: 200px;
    }


    legend{
        font-size: 20px;
        font-weight: bold;
        color: black;
    }

    fieldset{
        border: 2px solid black;
        padding: 10px;
        margin: 20px;
        justify-self: center;
        align-self: center;
        background-color: whitesmoke;
        width: 400px;
        height: 300px;
    }

    main{
        width: 99.5vw;
        height: 95vh;
        color: black;
        display: flex;
        overflow-x: hidden;
        background-image: url("https://wallpapercave.com/wp/wp13467289.png");
        background-size: cover;
    }
    div{
        display: flex;
        width: auto;
        height: auto;
        margin: 40px;
        justify-self: flex-end;
    }

    @media (max-width: 1200px) {
        main{
            width:  auto;
            height: 95vh;
        }
        div{
            width: max-content;
            height: max-content;
            margin: 100px;
            justify-self: center;
        }
    }

</style>