<template>
  <div class="relative h-full w-full">
    <div class="bubble-wrap --top-left">
      <bubble />
    </div>
    <div class="bubble-wrap --top-right">
      <bubble />
    </div>
    <div class="bubble-wrap --bottom-left">
      <bubble />
    </div>
    <div class="bubble-wrap --bottom-right">
      <bubble />
    </div>
  </div>
</template>
<style>
.bubble-wrap{
  position: absolute;
  z-index: -1;
  opacity: 40%;
  height: 200px;
  width: 200px;
}
.bubble-wrap.--top-left{
  top: -150px;
  left: -20px;
}
.bubble-wrap.--top-right{
  top: -115px;
  right: -5px;
}
.bubble-wrap.--bottom-left{
  bottom: -100px;
  left: -100px;
}
.bubble-wrap.--bottom-right{
  bottom: -100px;
  right: -50px;
}
</style>
