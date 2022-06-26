<script>
    let novio ='Oscar'
    let novia = 'Anaid'
    let fecha='16/10/2022'

</script>

<div class="principal" >
    <div class="novios">
        <h1>{novia} & {novio}</h1>
    </div>
    <br>
   
    <p>{fecha}</p>

</div>

<style>
.principal{
    width: 100%;
    height: 20rem;
    align-items: center;
    align-content: center;
    background-color:rgba(9,150, 148, 0.6);
    margin-top:50px;
    display:flex;
    flex-direction: column;
}
.novios{
    border: 3px solid white;
    width: 70%;
    height: 12rem;
    text-align: center;
    display: flex;
    justify-content: center;
    margin: auto;
    align-items: center;
    
}
.novios h1{
 
    font-size:5em;
    text-shadow: 5px 1px 1px rgba(158, 158, 158, 0.5);
}
div>p{
    position:bottom;
    font-size: 2.5rem;
    text-shadow: 3px 1px 1px rgba(158,158,158,0.5);
    text-align: center;
}



@media (max-width:500px){
    .novios h1{
        font-size:2rem;
    }
    div>p{
        font-size:1rem;
    }
}
</style>
