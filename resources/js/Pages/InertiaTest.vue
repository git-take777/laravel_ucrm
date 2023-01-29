<script setup>
import { Link } from '@inertiajs/inertia-vue3';
import { ref } from 'vue';
const newTitle = ref('')
const newContent = ref('')
</script>

<template>
inertiaテストです。<br>
<a>aタグのテストです</a> <br>
<Link href="">LINK経由です。</Link> <br>
<Link :href="route('inertia.index')">名前付きのルート</Link>
<Link :href="route('inertia.show', { id:1 })">ルートパラメータテストです</Link>

<div class="mb-8">
  <input type="text" name="newTitle" v-model="newTitle">{{ newTitle }} <br>
  <input type="text" name="newContent" v-model="newContent"> {{ newContent }} <br>
  <Link as="button" method="post" :href="route('inertia.store')"
  :data="{
    title: newTitle,
    content: newContent
  }">DBテスト</Link>
</div>
</template>