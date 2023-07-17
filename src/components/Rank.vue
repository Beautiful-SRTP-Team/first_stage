<template>
  <v-container class="rank">
    <v-dialog
      v-model="open"
      fullscreen
      :scrim="false"
      transition="dialog-bottom-transition"
    >
      <template v-slot:activator="{ props }">
        <div>
            <embed src="../../排行榜.svg" type="image/svg+xml"/>
            <v-btn
            color="primary"
            dark
            v-bind="props"
            class="rankText"
            >
            排行榜
            </v-btn>
      </div >

      </template>
      <v-card>
        <v-toolbar
          dark
          color="primary"
        >
          <v-btn
            icon
            dark
            @click="clickMe"
          >
            <v-icon>mdi-close</v-icon>
          </v-btn>
          <v-toolbar-title>排行榜</v-toolbar-title>
<!--          <v-spacer></v-spacer>-->
<!--          <v-toolbar-items>-->
<!--            <v-btn-->
<!--              variant="text"-->
<!--              @click="refresh"-->
<!--            >-->
<!--              刷新榜单-->
<!--            </v-btn>-->
<!--          </v-toolbar-items>-->
        </v-toolbar>
        <v-list
          lines="two"
          subheader
        >
          <v-list-subheader>User Controls</v-list-subheader>
          <v-list-item title="Content filtering"
                       subtitle="Set the content filtering level to restrict apps that can be downloaded"></v-list-item>
          <v-list-item title="Password"
                       subtitle="Require password for purchase or use password to restrict purchase"></v-list-item>
        </v-list>
        <v-divider></v-divider>
        <v-list :items="tops"
                item-value="order"
                item-title="msg"
        ></v-list>
        <!--以上的list就是我们的排行榜数据-->
      </v-card>
    </v-dialog>
  </v-container>
</template>

<script setup>

import {ref} from "vue";

const tops = [
  {
    order: 1,
    name: "A", score: 11
  },
  {
    order: 2,
    name: "B", score: 1
  },
].map((v) => {
  return {msg: `姓名：${v.name} 分数：${v.score}`, order: v.order}
})

const open = ref(false)
const clickMe = () => {
  open.value = !open.value
}
// const refresh = () => {
//
// }


</script>

<style scoped>
    .rank{
        float: left;
        width: 12.5vw;
        margin-left: 0vw;
    }
    .rank embed{
        margin-left: -1vw;
        margin-top: 0vh;
        height: 18.5vh;
    }
    .rank .rankText{
        text-align: center;
        font-size: 2.55vh;
        font-family: 黑体;
        font-weight: 900;
    }
</style>
