<template>
 <div class="main">
  <h1 class="mainTitle">TODOS</h1>

  <section class="section">
    <div id="app1">
      {{ message }}
    </div>
  </section>

  <section class="section">
    <div id="app2">
      <span v-bind:title="message" :class="classObject">
        この文字にマウスホバーすると画面を表示した日付が出る
      </span>
    </div>
  </section>

  <section class="section">
    <div id="app3">
      <span v-if="isShow">v-ifを使って、domの表示非表示が簡単に出来る。非表示だとDOM自体なくなるので注意！</span>
    </div>
  </section>

  <section class="section">
    <div id="app4">
      <ol>
        <!-- <li v-for="todo in todos">
          {{ todo.text }}
        </li> -->
      </ol>
    </div>
  </section>

  <section class="section">
    <div id="app5">
      <p>{{ message }}</p>
      <button v-on:click="changeMessage">メッセージを変える</button>
    </div>
  </section>

  <section class="section">
    <div id="app6">
      <p>{{ message }}</p>
      <input type="text" v-model="message">
    </div>
  </section>

</div>


</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

