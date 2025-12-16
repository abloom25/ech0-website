<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <main>
    <section class="section-1 section-flex-row">
      <div>
        <h1 class="mono">{{ t('home.title') }}</h1>
        <ins>{{ t('home.subtitle') }}</ins>
        <nav>
          <!-- <a>{{ t('home.docs') }}</a> -->
          <a href="https://github.com/lin-snow/Ech0">Github</a>
        </nav>
      </div>
      <img :alt="t('home.screenshotAlt')" src="/screenshot.png" />
    </section>
    <section class="section-2 section-flex-row">
      <div>
        <h1>开源</h1>
      </div>
      <div>
        <ul>
          <li>免费自由</li>
          <li>代码公开</li>
          <li>易于自托管</li>

        </ul>
      </div>
    </section>
    <section class="section-3 section-flex-row">
      <figure onclick="window.location.href='https://qm.qq.com/q/xIW8t1vVVm'">
        <img alt="QQ群二维码" src="/qq.png" />
        <figcaption>
          <b>扫码</b>或<b>点击</b>加入Ech0官方QQ交流群
        </figcaption>
      </figure>
      <div>
        <h1>社区</h1>
        <ins>我们有很成熟的社区，可以为您提供帮助。</ins>
      </div>
    </section>
    <!-- <section class="section-3 section-flex-row">
      <h1>用户评价</h1>
      <div></div>
    </section> -->
  </main>
</template>

<style lang="scss" scoped>
main,
section {
  width: 100%;
}

main {
  overflow-y: auto;
  height: 100%;
}

section {
  padding: 2rem;
  height: 100vh;
  h1 {
      font-size: 6rem;
      font-weight: 800;
  }
}

.section-flex-row {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 2rem;
}

.section-flex-column {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.section-1 {
  justify-content: space-between;

  div {
    h1 {
      color: #f43900;
    }

    ins {
      font-style: normal;
      font-size: 1.25rem;
    }

    nav {
      padding-top: .75rem;

      a {
        padding-right: .5rem;
        font-weight: bold;
      }
    }
  }

  img {
    transform: perspective(400px) rotate3d(1, -1, 0, 6deg);
    width: 50vw;
    z-index: -1;
    margin-right: 2rem;
    border-radius: 1rem;
  }
}

.section-2 {
  justify-content: space-around;

  div {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  h1 {
    text-align: end;
  }

  ul {
    font-size: 2rem;
    font-weight: 600;
  }
}
}

.section-3 {
  justify-content: space-around;

  div {
    flex: 1;
  }

  figure {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    cursor: pointer;
  }
}
</style>
