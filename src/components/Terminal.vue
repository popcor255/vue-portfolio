<template>
  <div>
    <div>
      <div class="terminal-window">
        <header>
          <div class="button green"></div>
          <div class="button yellow"></div>
          <div class="button red"></div>
        </header>
        <section class="terminal">
          <div id="terminal-data">
            <vue-typed-js :strings=commands>
              <p>$&nbsp; <span class="typing"></span></p>
            </vue-typed-js>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Terminal',
  props: {
    msg: String
  },
  data() {
    return {
      commands : getTerminalData()
    }
  }
}

const getTerminalData = () => {
  return  [`^3500 Hello. \`👋👋👋👋\` I hope you are doing well. 😀
  <br />$ kind create cluster
  \`<br /> Creating cluster "kind" ... \`
  \`<br />  <span style="color: green;"> ✓ </span> Ensuring node image (kindest/node:v1.19.1) 🖼 \`
  \`<br />  <span style="color: green;"> ✓ </span> Preparing nodes 📦  \`
  \`<br />  <span style="color: green;"> ✓ </span> Writing configuration 📜 \`
  \`<br />  <span style="color: green;"> ✓ </span> Starting control-plane 🕹️ \`
  \`<br />  <span style="color: green;"> ✓ </span> Installing CNI 🔌 \`
  \`<br />  <span style="color: green;"> ✓ </span> Installing StorageClass 💾 \`
  \`<br />Set kubectl context to "kind-kind" \`
  \`<br />You can now use your cluster with: \`
  \`<br />\`
  \`<br />Not sure what to do next? 😅  Check out https://kind.sigs.k8s.io/docs/user/quick-start/\`
  <br />$ ⏳ Time to install my resume as a kubernetes CRD, but
  <br />$ ... you wouldn't install it without reading it first? 😉
  <br />$ \`<a href="https://raw.githubusercontent.com/popcor255/resume/main/resume.yaml" style="text-decoration: none; color: inherit;">https://git.io/Jtu7M\`</a>`]
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.terminal-window {
  text-align: left;
  width: 600px;
  height: 360px;
  border-radius: 10px;
  margin: 17.5vh auto;
  position: relative;
}

.terminal-window header {
  background: #E0E8F0;
  height: 30px;
  border-radius: 8px 8px 0 0;
  padding-left: 10px;
}

.terminal-window header .button {
  width: 12px;
  height: 12px;
  margin: 10px 4px 0 0;
  display: inline-block;
  border-radius: 8px;
}

.terminal-window header .button.green {
  background: #3BB662;
}

.terminal-window header .button.yellow {
  background: #E5C30F;
}

.terminal-window header .button.red {
  background: #E75448;
}

.terminal-window section.terminal {
  color: white;
  font-family: Menlo, Monaco, "Consolas", "Courier New", "Courier";
  font-size: 11pt;
  background: #30353A;
  padding: 10px;
  box-sizing: border-box;
  position: absolute;
  width: 100%;
  top: 30px;
  bottom: 0;
  overflow: auto;
}

.terminal-window section.terminal .typed-cursor {
    opacity: 1;
    -webkit-animation: blink 0.7s infinite;
    -moz-animation: blink 0.7s infinite;
    animation: blink 0.7s infinite;
}

@keyframes blink{
    0% { opacity:1; }
    50% { opacity:0; }
    100% { opacity:1; }
}
@keyframes blink{
    0% { opacity:1; }
    50% { opacity:0; }
    100% { opacity:1; }
}
@keyframes blink{
    0% { opacity:1; }
    50% { opacity:0; }
    100% { opacity:1; }
}
.terminal-data { display: none; }
.terminal-window .gray { color: gray; }
</style>
