<template>
  <!--обёртка для всего содержимого, чтобы прижать footer к нижней части-->
  <div class="wrapper wrapper-forcontent">
      <!--Содержимое сайта без подвала (нужно для прижатия подвала к нижней части)-->
      <div class="content-without-footer">

          <!--Шапка сайта-->
          <header>
              <MenuRouting />
          </header>

          <!--Основная часть-->
          <main>
              <!--Первая секция основной части-->
              <section>
                <Hello/>
              </section>
              <!--Вторая секция-->
              <section>

              </section>
          </main>
      </div>

      <!--Подвал сайта-->
      <footer>
        Версия: 0.0.0
      </footer>
  </div>
</template>

<script>

import MenuRouting from '../components/MenuRouting.vue'
import Hello from '../components/Hello.vue'

export default {
  name: 'HomeView',

  components: {
    MenuRouting,
    Hello
  }
}
</script>

<style src="../scss/style.scss" lang="scss" scoped/>
