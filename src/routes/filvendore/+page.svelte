<script>
    let currentOutfit = "f.png";
    let warriorOutfit = "https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/6c3d567d-af2b-469e-b10c-d5b135964ab2/dg06u31-77d706fb-6721-4a63-9fa3-a41bd55079d2.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzZjM2Q1NjdkLWFmMmItNDY5ZS1iMTBjLWQ1YjEzNTk2NGFiMlwvZGcwNnUzMS03N2Q3MDZmYi02NzIxLTRhNjMtOWZhMy1hNDFiZDU1MDc5ZDIucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.EXnghx51urbcBm27EHJRC3axl7pbHfeIBFiepzjWphQ"
    
    function warrior(){
        currentOutfit = warriorOutfit;

    }
    
    function normal() {
        currentOutfit = "f.png";

    }

</script>

<main>
    <section>
    <div class="flower"></div>
        <fieldset>
            <legend> Filvendore </legend>
                <ul> 
                    <li><b>Name:</b> Filvendore</li>
                    <li><b>Last name:</b> Lockridge</li>
                    <li><b>Age:</b> 45</li>
                    <li><b>Genre:</b> Fantasy</li>
                    <li><b>Species:</b> Elf</li>
                    <li><b>Details: How I got my scar?</b> I was fighting Arathorn. He was young but albeit very experienced.
                        <br>I knew I had the disadvantage. But my subordinates were all afraid of him. So I had to be the one to fight him.
                        <br>I did it for Theodluin, my adoptive son. I can still hear his scearms eco in my ears when one of them shot him in the eye. 
                        <br>He surrvived but barly. I remember attacking Arathorn in a misserble attempet to distract him. Then I ran and scooped a crying Theodluin in my arms.
                        <br>But Arathorn had caught up to me and he wasted not even a second to strike. His sword stiked me over my cheek and throat. There you have it, how I got my scar. One of many. But I do not want to talk about the rest.
                        <br><b>You want the story of Theodluin?</b> That is not my story to tell. You will have to ask him, although I am not sure he wants to talk about it.
                        <br>I can say this much. I took him to Aithlin since we cooperated when the warriors attacked our territories.
                        <br><b>If we have any special animals...</b> Hmm, ah yes we usualy ride </li>
                </ul>
        </fieldset>
    </section>

    
    <h1>Karkatär: Filvendore</h1>
    <div>
        <img src={currentOutfit} alt="Filvendore" >
    </div>
    {#if currentOutfit === "f.png"}
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

    h1{
        width: 100px;
    }
    .flower{
        height: 200px;
        width: 460px;
        background-image: url("https://static.vecteezy.com/system/resources/thumbnails/048/725/761/small_2x/graphic-with-a-black-white-and-pink-elegant-plant-flower-sakura-ornament-on-an-isolated-background-png.png");
        background-size: cover;
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
        width: 500px;
        height: 700px;
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