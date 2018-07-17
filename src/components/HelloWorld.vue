<template>
  <div class="tab-container">
    <div class="login-tab">
      <ul class="tab-list">
        <li class="list-item list-item-qq current" data-type="qq">
          <a class="tab-item tab-item-qq">
            <i class="ico-loginqq"></i>
            <span class="item-inner">QQ账号登录</span>
          </a>
        </li>
        <li class="list-item list-item-wx" data-type="wx">
          <a class="tab-item tab-item-wx">
            <i class="ico-loginwx"></i>
            <span class="item-inner">微信账号登录</span>
          </a>
        </li>
      </ul>
    </div>
    <div class="login_tips">
      <div class="tips_txt">微信和QQ是两个独立账号，账号信息不互通</div>
      <div class="tips_notes">登录后高清播放更流畅</div>
    </div>
    <div class="login_cont">
      <div class="cont_inner cont_inner_qq">
        <div class="login_iframe login_iframe_qq">
          <iframe name="_login_frame_quick_" id="_login_frame_quick_" frameborder="no" scrolling="no" style="width:626px; height:370px;" src=""></iframe>
        </div>
      </div>
      <div class="cont_inner cont_inner_wx">
        <div class="login_iframe login_iframe_wx">
          <label class="iframe_title">安全登录，防止被盗</label>
          <iframe name="_login_frame_wechat_" id="_login_frame_wechat_" frameborder="no" scrolling="no" style="width:100%; height:215px;" src=""></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import request from "axios"
import Tab from './tab.js'

export default {
  name: 'LoginTab'
}
</script>

<style scoped>
  
</style>
