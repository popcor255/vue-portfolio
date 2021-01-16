<template>
    <div class="wrapper">
        <div class="typing-demo">
            <h4>Napoleon Santana</h4>
        </div>
        <div class="typing-second-linedemo">
            <h6> Software Engineer at IBM</h6>
        </div>
    </div>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono&display=swap');
.wrapper {
  color: #FFFFFF;
  position: relative;
  /*This part is important for centering*/
  width: 255px;
  display: block;
  align-items: center;
  justify-content: center;
  margin: 15px auto;
  text-align: center;
}

.typing-demo {
  width: 250px;
  animation: typing 2s steps(22), blink .5s step-end infinite alternate;
  white-space: nowrap;
  overflow: hidden;
  border-right: 0px solid;
  font-family: monospace;
  font-size: 2em;
}

.typing-second-linedemo {
  width: 250px;
  animation: typing 2s steps(22) forwards, blink .5s step-end alternate;
  white-space: nowrap;
  overflow: hidden;
  border-right: 3px solid;
  font-family: monospace;
  font-size: 2em;
  animation-delay: 2s;
  opacity: 0%;
}

@keyframes typing {
  0% {
    width: 0px;
    opacity: 100%;
    border-right: 3px solid;
  }
  99% {
    border-right: 3px solid;
  }
  100% {
    opacity: 100%;
    border-right: 0px solid;
  }
}
    
@keyframes blink {
  50% {
    border-color: transparent
  }
}
</style>