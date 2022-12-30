<script>
  let music = new Audio("/src/assets/rickroll.wav")
  let rickRollCount = 0
  function isPlaying(music) {
    return !music.paused
  }
  function countAdd() {
    rickRollCount += 1
  }
  function rickRoll() {
    if (music.paused == false) {
      console.log('music is already playing')
    } else if (rickRollCount > 1) {
      alert("I'M SURPRISED THAT YOU FELL FOR THIS AGAIN (or maybe not)!")
      music.play()
      setTimeout(countAdd, 213000)
    } else {
      alert('YOU FELL FOR MY TRAP, HAHAHAHAHA!')
      music.play()
      setTimeout(countAdd, 213000)
    }

  }
</script>
<h1>Future_Axolotl</h1>
<button on:click={rickRoll} class="pfp"><img src="/src/assets/pfp.png" alt="pfp"></button>
{#if rickRollCount > 0}
  <p>Times obnoxiously Rickrolled: {rickRollCount}</p>
{/if}

<p>
  "Just a random hobby dev and Linux YouTuber."
</p>
<p style="font-size:30px;">
  Whether it be software reviews, rices, coding, gaming, or just whatever the heck I feel like making, I hope you can find something you can enjoy.
</p>

<style>
  .pfp {
    border: none;
    padding: 0;
    background: none;
  }
</style>
