---
title: "欢迎来到我的生活与技术世界"
description: "分享我的生活点滴与计算机专业知识"
---


<div class="hero min-h-screen bg-cover bg-center text-white" style="background-image: url('/images/hero-background.jpg');">
  <div class="hero-overlay bg-opacity-60"></div>
  <div class="hero-content text-center">
    <div class="max-w-md">
      <h1 class="mb-5 text-5xl font-bold">欢迎来到我的数字生活与技术世界</h1>
      <p class="mb-5">探索我的生活故事和技术见解</p>
    </div>
  </div>
</div>

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; background: #000;">
    <iframe id="bilibili-player" src="//player.bilibili.com/player.html?isOutside=true&aid=1806321469&bvid=BV1Pb421J71K&cid=1639292682&p=1" 
            style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
            frameborder="no" 
            allowfullscreen="true">
    </iframe>
    <div id="video-overlay" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0);"></div>
</div>

<script>
    document.getElementById('video-overlay').addEventListener('click', function(event) {
        // 捕获点击事件
        event.stopPropagation();
        event.preventDefault();
        
        // 如果是播放事件，执行播放操作
        var iframe = document.getElementById('bilibili-player');
        iframe.contentWindow.postMessage({ method: 'play' }, '*');

        // 根据具体逻辑判断是否为跳转事件
        // 例如：你可以判断用户是否点击了视频播放器的特定区域
        var isJumpEvent = false; // 根据实际逻辑修改
        
        if (!isJumpEvent) {
            this.style.display = 'none';  // 如果不是跳转事件，隐藏覆盖层以允许正常操作
        } else {
            // 如果是跳转事件，你可以阻止跳转或显示警告
            console.log("阻止跳转事件");
        }
    });
</script>


