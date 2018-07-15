<template>
  <div class="terminal">
    <div class="terminal__header">
      <div class="osx-button button-danger"></div>
      <div class="osx-button button-warning"></div>
      <div class="osx-button button-success"></div>
    </div>
    <div class="terminal__body">
      Last login: Sun Jul 15 19:35:26 on ttys000
      <pre class="terminal__code">
      $ sudo killall
      </pre>
    </div>
  </div>
</template>

<script>
export default {
  name: 'vue-terminal',
}
</script>

<style lang="scss">
.terminal {
  font-family: 'Anonymous Pro', monospace;
  border: 1px rgba(0, 0, 0, 0.1) solid;
  border-radius: 6px;
  overflow: hidden;
  font-size: 13px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);

  &__header {
    background: linear-gradient(to bottom, #e5e3e5 0%, #cfcecf 100%);
    border-bottom: 1px #7e7e7e solid;
    overflow: hidden;
    padding: 6px;
    position: relative;

    &:before {
      position: absolute;
      top:0;
      left:0;
      width: 100%;
      height: 1px;
      content: "";
      background: linear-gradient(to bottom, #f4f3f4 0%, transparent 100%);
    }
  }

  &__body {
    padding: 4px;
    height: 300px;
    overflow-y: auto;
  }

  pre {
    margin: 0;
    padding: 0;
    font-family: inherit;
    white-space: pre-line;
  }
}

.osx-button {
  width: 9px;
  height: 9px;
  border-radius: 50%;
  display: block;
  float: left;
  background: yellow;
  border: 1px transparent solid;

  + .osx-button {
    margin-left: 6px;
  }

  &.button-danger {
    background: #fc625d;
    border-color: #de4846;
  }

  &.button-warning {
    background: #fdbc40;
    border-color: #de9b2b;
  }

  &.button-success {
    background: #34c84a;
    border-color: #26a934;
  }
}
</style>
