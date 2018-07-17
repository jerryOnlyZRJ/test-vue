<template>
  <div class="container">
    <div class="drop-menu" style="position: relative;" @click="clickHandler"> </div>
    <div class="drop-menu" style="position: relative;" @click="clickHandler"> </div>
    <div class="drop-menu" style="position: relative;" @click="clickHandler"> </div>
  </div>
</template>

<script>
function dropMenuCreator(content, translateX) {
  translateX = translateX || ''
  return function(e) {
      removeDropMenu()
      const target = e.target
      const targetHeight = e.target.offsetHeight
      const dropMenu = `<div class="menu_bd" style="position: absolute;z-index: 1121;top:${targetHeight}px;transform: translateX(${translateX});">${content}</div>`
      target.innerHTML += dropMenu
  }
}
function removeDropMenu() {
    const lastDropMenu = document.querySelector('.menu_bd')
    if (lastDropMenu) lastDropMenu.parentNode.removeChild(lastDropMenu)
    return this
}
const dropMenuClickEventHandler = dropMenuCreator('<div style="padding: 0 14px 0 16px;">test<div>')
export default {
  name: 'DropMenu',
  methods: {
    clickHandler: dropMenuClickEventHandler
  }
}
</script>

<style>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    height: 500px;
}
.drop-menu {
  height: 10px;
  width: 10px;
  background: red;
}
.menu_bd {
  background: #fff;
  padding: 4px 0;
  border: 1px solid #a0a0a0;
  border-radius: 3px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.3);
}
</style>
