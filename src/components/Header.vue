<template>
    <div class="wrapper">
        <div class="typing-demo">
            <h4>Napoleon Santana</h4>
        </div>
        <div class="typing-second-linedemo">
            <h6>&nbsp;Software Engineer</h6>
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
    /*This part is important for centering*/
    margin: 15px auto;
    position: fixed;
    top: 0;
    width: 100%;
    text-align: center;
}

.typing-demo {
    width: 250px;
    animation: typing 1.6s steps(22), type .5s step-end alternate;
    white-space: nowrap;
    overflow: hidden;
    border-right: 0px solid;
    font-family: monospace;
    font-size: 2em;
    margin: 8px auto;
}

.typing-second-linedemo {
    width: 250px;
    animation: typingAfter 3.4s steps(22) forwards, type .5s step-end alternate;
    white-space: nowrap;
    overflow: hidden;
    border-right: 3px solid;
    font-family: monospace;
    font-size: 2em;
    margin: 8px auto;
}

@keyframes typingAfter {
  0% {
    opacity: 100% !important;
    border-right: 0px solid;
    width: 0;
  }
  49% {
    opacity: 100% !important;
    border-right: 0px solid;
    width: 0;
  }
  50% {
    opacity: 0% !important;
    border-right: 3px solid; 
  }
  85% {
    border-right: 3px solid; 
  }
  86% {
    border-right: 0px solid;
  }
  99% {
    opacity: 0% !important;
    border-right: 0px solid;
  }
  100% {
    opacity: 0% !important;
    border-right: 0px solid;
  }
}
    

@keyframes typing {
  0% {
    width: 0px;
    border-right: 3px solid; 
  }
  99% {
    border-right: 3px solid;
  }
  100% {
    border-right: 0px solid;
  }
}
    
@keyframes type {
  50% {
    border-color: transparent
  }
}
</style>