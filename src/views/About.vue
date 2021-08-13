<template>
  <div class="about">
    <div class="about-title">
      <h1 class="about-me-shadow">About me</h1>
      <h1 class="about-me-title">About me</h1>
    </div>
    <div class="contents">
      <h2>「てれるん」とは</h2>
      <div class="about-tererun-description">
        <span>
          "やりたいことを実現"させるために、気ままにプログラムを書いている高校生です。
          <br />
          JavaでSpigotプラグインを作っていたり、最近はUnityやFlutterなどにも手を出し始めています。
        </span>
      </div>

      <h2></h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<style>
.about-title {
  position: relative;
  height: 16vw;
}

.about-me-title {
  position: absolute;
  animation-duration: 3s;
  animation-name: slidein;
  margin-top: 6.45vw;
  font-size: 10vw;
}

.about-me-shadow {
  position: absolute;
  top: -8vw;
  animation-duration: 3.5s;
  animation-name: slide;
  margin: 0px 40px;
  font-size: 25vw;
  overflow-x: hidden;
  overflow-y: hidden;
  white-space: nowrap;
  color: #84af95;
}

h1 {
  font-family: "Montserrat";
  font-style: italic;
  font-weight: 800;
  font-size: 100px;
  margin: 20px;
}

h2 {
  font-size: 30px;
  margin-bottom: 10px;
}

span {
  font-size: 16px;
}

.contents {
  animation-delay: 3.5s;
  animation-fill-mode: backwards;
  animation-duration: 3s;
  animation-name: visible;
  padding: 20px;
  text-align: center;
}

.about-tererun-description {
  display: flex;
  justify-content: center;
  align-items: center;
}

@keyframes slidein {
  from {
    margin-left: 100%;
    width: 300%;
  }

  to {
    margin-left: 20px;
    width: 100%;
  }
}

@keyframes slide {
  from {
    margin-left: 100%;
    width: 300%;
  }

  to {
    margin-left: 40px;
    width: 120%;
  }
}

@keyframes visible {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}
</style>