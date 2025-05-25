<script>
    let currentOutfit = "toya.jpg";
    
    function warrior(){
        currentOutfit = "https://i.pinimg.com/originals/09/51/4f/09514fe23be792caf658f3306987cdd5.png";
    }
</script>

<main>
    <fieldset>
        <legend>Toya</legend>
            <ul> 
                <li><b>Name:</b> Toya</li>
                <li><b>Last name:</b> Seiya</li>
                <li><b>Age:</b> 16</li>
                <li><b>Genre:</b> Fantasy</li>
                <li><b>Species:</b> Samurai</li>
                <li><b>Story:</b> Why would one need eyes? One might be blind but ones other senses are hightned. 
                    <br> How it happend? One cut out ones eyes as proof of ones loyalty. 
                    <br> To whom? That one can not tell...</li>
            </ul>
    </fieldset>
    
    <h1>Karkatär: Toya Seiya</h1>
    <div>
        <img src={currentOutfit} alt="Elfrane" >
    </div>
    <button class="warriorOutfit" on:click={(warrior)}>Warrior outfit</button>

    

</main>


<style>
    .warriorOutfit{
        background-image: url("https://static.vecteezy.com/system/resources/previews/015/724/204/non_2x/simple-black-arrow-for-design-element-png.png");
        background-size: cover;
        width: 100px;
        height: 70px;
        margin-top: 300px;
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