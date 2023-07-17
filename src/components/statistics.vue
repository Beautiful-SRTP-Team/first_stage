<template>
    <v-row justify="space-around" class="count">
      <v-col cols="auto">
  <!-- 弹出对话框 -->
        <v-dialog
          transition="dialog-bottom-transition"
          width="auto"
        >
  <!-- 按钮 -->
          <template v-slot:activator="{ props }">
            <div >
            <embed src="../../统计管理.svg" type="image/svg+xml">
            <v-btn
              color="primary"
              v-bind="props"
              class="countText"
            >统计管理</v-btn>
            </div>

          </template>
  <!-- 弹出的页面 -->
          <template v-slot:default="{ isActive }">
            <v-card>
                <v-card-title class="headline">统计正确率情况</v-card-title>
                <v-list>
                    <v-list-item v-for="(item, index) in leaderboard" :key="index">
                        <v-list-item-content>
                            <v-list-item-title>{{ item.name }}</v-list-item-title>
                            <v-list-item-subtitle>{{ item.score }}</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>
                <v-btn
                variant="text"
                @click="isActive.value = false"
              >details</v-btn>
            </v-card>
          </template>

        </v-dialog>
      </v-col>
    </v-row>

  </template>

  <script>
  export default {
    data() {
      return {
        leaderboard: [
          { name: '难度1', score: 100 },
          { name: '难度2', score: 90 },
          { name: '难度3', score: 80 },
          { name: '难度4', score: 70 },
          { name: '难度5', score: 60 },
        ]
      };
    },
  };
  </script>

  <style scoped>
    .count{
        float: right;
        width: 12vw;
        margin-right: 0vw;
    }
    .count embed{
        margin-left: -1vw;
        margin-top: 1.8vh;
        height: 19vh;
    }
    .count .countText{
        text-align: right;
        margin-right: 4vw;
        font-size: 2.55vh;
        font-family: 黑体;
        font-weight: 900;
    }
  </style>
