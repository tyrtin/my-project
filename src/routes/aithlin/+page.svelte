<script>
    let clicked = true
    let buttonClicked = true;
    let currentOutfit = "ait.png";
    let warriorOutfit = "https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/6c3d567d-af2b-469e-b10c-d5b135964ab2/dg06u31-77d706fb-6721-4a63-9fa3-a41bd55079d2.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzZjM2Q1NjdkLWFmMmItNDY5ZS1iMTBjLWQ1YjEzNTk2NGFiMlwvZGcwNnUzMS03N2Q3MDZmYi02NzIxLTRhNjMtOWZhMy1hNDFiZDU1MDc5ZDIucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.EXnghx51urbcBm27EHJRC3axl7pbHfeIBFiepzjWphQ"
    
    function warrior(){
        currentOutfit = warriorOutfit;
        buttonClicked = false;
    }
    
    function normal() {
        currentOutfit = "ait.png";
        clicked = false;
    }

</script>

<main>
    <fieldset>
        <legend></legend>
            <ul> 
                <li><b>Name:</b> Aithlin</li>
                <li><b>Last name:</b> Cinderleaf</li>
                <li><b>Age:</b> 40</li>
                <li><b>Genre:</b> Fantasy</li>
                <li><b>Species:</b> Elf</li>
                <li><b>Details: How I got my scar?</b> Long story short: When i was fleeing the fire the warrior elfs started. You want more details? Fine. Elfrane and her army was hunting us through the forest, and of course, they were faster then us.
                    <br> So I made a stupid plan on the spot. I hastly told it to the oldest of us and then I started counting down. I screamed and we all halted suddenly. We took the warriors by suprise with this move so they abruply came to a stop. 
                    <br> I thought foolishly that with our magic we would be able to stop them long enough so the youngsters could escape. But I was wrong. Even with veins and threes attacking them they made it to us in seconds. 
                    <br> I still remember the horrifying screams of my comrads when the warriors plunged their swords into them. Elfrane personally came to me. I helplessly fought with my leaf coverd veins but she sliced me right across the face. 
                    <br> I don't even know how I surrvived...
                    <br><b> Of course you would want to know if the others surrvived.</b> Not many but some of the more experienced ones did. Most of the youngsters were able to escape but unfortunately not all of them. We lost many in the fire too. 
                    <br> All thogheter we lost too many... We should have cooperated with the politic elves earlier. They too lost many elves. 
                    <br><b> Do we have animals?</b>Yes. My companion is a deer, a very small one with a light brown fur. But we help every animal in the forest. So we usualy get company from very many diffrent animal...Exept the mooses.  </li>
            </ul>
    </fieldset>
    
    <h1>Karkatär: </h1>
    <div>
        <img src={currentOutfit} alt="Elfrane" >
    </div>
    {#if currentOutfit === "ait.png"}
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