<script>
    let currentOutfit = "a.png";
    let warriorOutfit = "https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/6c3d567d-af2b-469e-b10c-d5b135964ab2/dg06u31-77d706fb-6721-4a63-9fa3-a41bd55079d2.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzZjM2Q1NjdkLWFmMmItNDY5ZS1iMTBjLWQ1YjEzNTk2NGFiMlwvZGcwNnUzMS03N2Q3MDZmYi02NzIxLTRhNjMtOWZhMy1hNDFiZDU1MDc5ZDIucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.EXnghx51urbcBm27EHJRC3axl7pbHfeIBFiepzjWphQ"
    
    function warrior(){
        currentOutfit = warriorOutfit;

    }
    
    function normal() {
        currentOutfit = "a.png";

    }

</script>

<main>
    <fieldset>
        <legend> Arathorn </legend>
            <ul> 
                <li><b>Name:</b> Arathorn</li>
                <li><b>Last name:</b> Aewynn</li>
                <li><b>Age:</b> 19</li>
                <li><b>Genre:</b> Fantasy</li>
                <li><b>Species:</b> Elf</li>
                <li><b>Details: How I got my scars?</b> Well I was fighting Filvendore. He may be a politic elf, but give him a sword and he goes crazy.
                    <br>I mean it do not give him a sword. He would have shopped my head of if I haden't dodged.  
                    <br>I still got the scar you see though. But not to worry I gave him one right back. I have many more but lets not talk about them. 
                    <br><b>If I have any relatives?</b> No... But I have my right hand man Evindal and his sister Elfrane. They are the only ones I trust.
                    <br><b>Why I wear horns?</b> Becaues I am the leader of the warrior elves. The moose is the king of the forest, just like I am the "king" of the warrior elves.
                    <br>Who are the elves of the mountains so I guess it is not the best symbol... But on the other hand we ride on mooses so...  
                    <br>Of course you would ask the about the name of my moose. I gave it the name Ziethionth which means the taker of life. 
                    <br>He is very tall and elegant. He is the color of the darkest night and has the most beautiful antlers.
                    </li>
            </ul>
    </fieldset>
    
    <h1>Karkatär: Arathorn</h1>
    <div>
        <img src={currentOutfit} alt="Elfrane" >
    </div>
    {#if currentOutfit === "a.png"}
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
        height: 600px;
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