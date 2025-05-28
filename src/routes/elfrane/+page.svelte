<script>
    let currentOutfit = "el.png";
    let warriorOutfit = "el_dress.png";
    
    function warrior(){
        currentOutfit = warriorOutfit;
    }
    
    function normal() {
        currentOutfit = "el.png";

    }

</script>

<main>
    <fieldset>
        <legend> Elfrane </legend>
            <ul> 
                <li><b>Name:</b> Elfrane</li>
                <li><b>Last name:</b> Everya</li>
                <li><b>Age:</b> 18</li>
                <li><b>Genre:</b> Fantasy</li>
                <li><b>Species:</b> Elf</li>
                <li><b>Details: How I got my scars?</b> Stupid question I have too many to tell you about. Fineeee *Insert eye roll* You wanna know about all of them or just the one on my nose??  
                    <br> All of them?! Are you crazy I litterally just told you I have to many to even count. I will tell you about the one on my nose. Hmph, *crossing arms and shighing* 
                    <br> I fought against a super strong bird. A falcon bird human or something. She had very big claws and used feathers as swords. If a little blue birdy hadn't interfered I would have won.
                    <br> Or rather if my brother, Arathorn and the blue birdy had not interfered she would have been dead. *Evil laugh* But anyway, she took that feather of hers and sliced it across my poor nose. 
                    <br> Not that it matters, my skin is already coverd in scars.
                    <br> Next question. <b>You heard that Arathorn had a moose and you want to know how mine look and what name it has?</b> Alrighty. I gave my moose the name Chayveon. I don't know what it means though. Her fur is silver and white.
                    <br> She lights up in the moonlight, which looks cool and all, but it's not very effective when we want to blend in with the shadow. HEHE...</li>
            </ul>
    </fieldset>
    
    <div>
        <img src={currentOutfit} alt="Elfrane" >
    </div>
    {#if currentOutfit === "el.png"}
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
        height: 400px;
        overflow-y: scroll;
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