<script>
    let currentOutfit = "toya.png";
    let warriorOutfit = "https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/6c3d567d-af2b-469e-b10c-d5b135964ab2/dg06u31-77d706fb-6721-4a63-9fa3-a41bd55079d2.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzZjM2Q1NjdkLWFmMmItNDY5ZS1iMTBjLWQ1YjEzNTk2NGFiMlwvZGcwNnUzMS03N2Q3MDZmYi02NzIxLTRhNjMtOWZhMy1hNDFiZDU1MDc5ZDIucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.EXnghx51urbcBm27EHJRC3axl7pbHfeIBFiepzjWphQ"
    
    function warrior(){
        currentOutfit = warriorOutfit;
 
    }
    
    function normal() {
        currentOutfit = "toya.png";

    }

</script>

<main>
    <fieldset>
        <legend>Toya </legend>
            <ul> 
                <li><b>Name:</b> Toya</li>
                <li><b>Last name:</b> Kuroko</li>
                <li><b>Age:</b> 16</li>
                <li><b>Genre:</b> Fantasy</li>
                <li><b>Species:</b> Samurai</li>
                <li><b>Story:</b> Why would one need eyes? One might be blind but ones other senses are hightned. 
                    <br> How it happend? One cut out ones eyes as proof of ones loyalty. 
                    <br> To whom? That one can not tell...</li>
            </ul>
    </fieldset>
    
    <h1>Karkatär: </h1>
    <div>
        <img src={currentOutfit} alt="Toya" >
    </div>
    {#if currentOutfit === "toya.png"}
        <button class="warriorOutfit" on:click={(warrior)}></button>
    {:else}
        <button class= "normal" on:click={(normal)}></button>
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