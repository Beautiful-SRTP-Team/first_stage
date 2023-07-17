<template>
  <v-row justify="space-around" class="wrongProblem">
    <v-col cols="auto">
<!-- 弹出对话框 -->
      <v-dialog
        transition="dialog-bottom-transition"
        width="auto"
      >
<!-- 按钮 -->
        <template v-slot:activator="{ props }">
          <div >
            <embed src="../../错题库.svg" type="image/svg+xml">
            <v-btn
            color="primary"
            v-bind="props"
            class="wrongProblemText"
          >错题集</v-btn>
          </div>
        </template>
<!-- 弹出的页面 -->
        <template v-slot:default="{ isActive }">
          <v-card>
            <v-img height="600" width="600" src="@/assets/wrong.svg" />
            <!-- <v-toolbar
              color="primary"
              title="Opening from the bottom"
            ></v-toolbar>
            <v-card-text>
              <div class="text-h2 pa-12">Hello world!</div>
            </v-card-text> -->
            <v-card-actions class="justify-end">
                <v-btn
                variant="text"
                @click="isActive.value = false"
              >more</v-btn>
                <v-btn
                variant="text"
                @click="isActive.value = false"
                >Close</v-btn>
            </v-card-actions>
          </v-card>
        </template>

      </v-dialog>
    </v-col>

    <!-- <v-col cols="auto">
      <v-dialog
        transition="dialog-top-transition"
        width="auto"
      >
        <template v-slot:activator="{ props }">
          <v-btn
            color="primary"
            v-bind="props"
          >From the top</v-btn>
        </template>
        <template v-slot:default="{ isActive }">
          <v-card>
            <v-toolbar
              color="primary"
              title="Opening from the top"
            ></v-toolbar>
            <v-card-text>
              <div class="text-h2 pa-12">Hello world!</div>
            </v-card-text>
            <v-card-actions class="justify-end">
              <v-btn
                variant="text"
                @click="isActive.value = false"
              >Close</v-btn>
            </v-card-actions>
          </v-card>
        </template>
      </v-dialog>
    </v-col> -->
  </v-row>

</template>

  <script >
    //
  </script>

<style scoped>
  .wrongProblem{
        float: right;
        width: 12vw;
        margin-right: 0vw;
    }
    .wrongProblem embed{
        margin-left:-1.5vw;
        margin-top: 0vh;
        height: 17.5vh;
    }
    .wrongProblem .wrongProblemText{
        text-align: center;
        margin-right: 2vw;
        margin-top: 0.4vh;
        font-size: 2.55vh;
        font-family: 黑体;
        font-weight: 900;
    }
</style>
