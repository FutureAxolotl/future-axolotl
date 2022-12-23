<script>
  let music = new Audio("/src/assets/rickroll.wav")
  let rickRollCount = 0
  function isPlaying(music) {
    return !music.paused
  }
  function rickRoll() {
    if (music.paused == false) {
      console.log('music is already playing'  )
    } else if (rickRollCount > 1) {
      alert("I'M SURPRISED THAT YOU FELL FOR THIS AGAIN (or maybe not)!")
      music.play()
      rickRollCount += 1
    } else {
      alert('YOU FELL FOR MY TRAP, HAHAHAHAHA!')
      music.play()
      rickRollCount += 1
    }

  }
</script>
<button on:click={rickRoll} class="pfp"><img src="/src/assets/pfp.png" alt="pfp"></button>
{#if rickRollCount > 0}
  <p>Times obnoxiously Rickrolled: {rickRollCount}</p>
{/if}
<h1>Future_Axolotl</h1>
<p>
  "Just a random hobby dev and Linux YouTuber."
</p>

<style>
  .pfp {
    border: none;
    padding: 0;
    background: none;
  }
</style>
