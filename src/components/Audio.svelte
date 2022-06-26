<script>
let isPlaying = 0;
let audio;
console.log("creando audio");
audio = new Audio();
audio.src = "../assets/Ben E. King - Stand By Me (Karaoke Piano).mp3"

function playOrPause() {
  if (audio.readyState < 2 /*HAVE_CURRENT_DATA*/) {
    console.log("no está listo aún");
    if (audio.error) {
      console.log("error : " + audio.error.code + " -> " + audio.error.message);
    }
    return(0);
  }
  isPlaying = isPlaying + 1;
  console.log(isPlaying);
  if (isPlaying == 1) {
    audio.play();
    console.log("playing");
  } else {
    audio.pause();
    console.log("paused");
    isPlaying = 0;
  }
  return(isPlaying);
}

</script>

    <button on:click={playOrPause}>
  
         <i class="bi bi-music-note-beamed">
        
        </i>
  
    </button>

<style>
    button {
        border-radius: 50%;
        width: 50px;
        height: 50px;
        position: fixed;
        background-color:rgba(9,150, 148, 0.6);

    }

</style>