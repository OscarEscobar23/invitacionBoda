<script>
    const days= document.getElementById('days'),
    hours= document.getElementById('hours'),
    minutes= document.getElementById('minutes'),
    seconds= document.getElementById('seconds'),
    finalMessage = document.querySelector('.final-sms');

	   //fecha futuro

	const countDownDate= new Date('Oct 16, 2022 18:00:00').getTime();

let interval = setInterval(function(){

	//Obtener fecha actual y milisegundos
	const now= new Date().getTime();

	//obtenemos la distancia entre ambas fechas

	let distance = countDownDate - now;

	//calculos a dias horas minutos y segundos

	let day= Math.floor( distance / (1000 * 60 * 60 * 24));
    
	let hour= Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
   
	let minute= Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    
	let second= Math.floor((distance % (1000 * 60)) / (1000));
    

	//Resultados

	document.getElementById('days').innerHTML=day;
	document.getElementById('hours').innerHTML=hour;
    document.getElementById('minutes').innerHTML=minute;
	document.getElementById('seconds').innerHTML=('0'+second).slice(-2);


    if (distance < 0){
        clearInterval(interval);
        finalMessage.style.transform = 'traslateY(0)';
    }


}


,1000);

 
   
</script>

<section class="contenedorCount">
    <div class="countdown">
        <div class="sec">
            <p id="days">00</p>
            <span>Dias</span>
        </div>
        <div class="sec">
            <p id="hours">00</p>
            <span>Horas</span>
        </div>
        <div class="sec">
            <p id="minutes">00</p>
            <span>Minutos</span>
        </div>
        <div class="sec">
            <p id="seconds">00</p>
            <span>Segundos</span>
        </div>
    </div>

</section>



<style>
    .contenedorCount{
        width: 100%;
        min-height:20vh;
        display:flex;
        align-items:center;
        justify-content:center;
        flex-direction:column;
        background-color: rgba(9,150, 148, 0.6);
        margin:10px 0;

    }
    .countdown{
        display:flex;
        justify-content:space-evenly;
        width: 50%;
        flex-wrap: wrap;

    }
    .sec{
        display:grid;
        place-items: center;
        padding:10px;
    }
    p{
        display:grid;
        place-items: center;
        /*border:solid 1px #fff;*/
        height:50px;
        width: 50px;
        border-radius:50%;
        color:#fff;
        font-size:2rem;
        font-weight:bold;
        /*background-color:rgba(200, 7, 7, 0.6);*/
    }
    span{
        display:block;
        padding:10px;
        text-align: center;
        font-size:1.6rem;
        font-weight: 400;
        font-family: 'Cormorant', serif;
    }

    @media (max-width:500px){
        span{
            font-size:1rem;
            padding:2px;
        }
        p{
            font-size:1.2rem;
        }
        .sec{
        display:grid;
        place-items: center;
        padding:5px;
        }
        .countdown{
        display:flex;
        justify-content:center;
        width: 100%!important;
        flex-wrap: wrap;

        }
        .contenedorCount{
        min-height: 10vh;
        }
    }
</style>