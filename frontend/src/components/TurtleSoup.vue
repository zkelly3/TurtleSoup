<template>
  <div class="container">
    <div class="part">
      <tabs>
        <tab name="題目" class="question">
          {{question}}
        </tab>
      </tabs>
    </div>
    <div class="part">
      <tabs>
        <tab name="提問" class="guesses">
          <div class="guess">
            船長喝到的真的是海龜湯嗎？
          </div>
        </tab>
        <tab name="解答" class="answer">
          {{answer}}
        </tab>
      </tabs>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TurtleSoup',
  data() {
    return {
      question: "有一位船長喝了一碗湯，感覺味道有點奇怪，就問店家這是什麼湯？店家告訴他：「這是用海龜肉做的湯」，船長便沉思了一下，然後痛哭了起來，接著就自殺了。請問為什麼呢？".repeat(10),
      answer: "船長以前出海的時候，遇上暴風雨，船故障在海上漂了很久，而且大家都沒東西吃，有些船員甚至因為暴風雨離世了，於是就有船員為了讓船長活下去，將已經死亡船員的肉，煮成湯給船長喝，騙他是海龜肉，船長就活下來了。多年後船長在店家吃到真正的海龜肉，終於明白當時的事情，傷心之下選擇自殺。".repeat(10),
    }
  }
}
</script>

<style lang="scss">
@use '../styles/colors.scss';

$grid: 8px;

.container {
  margin-left: auto;
  margin-right: auto;
  max-width: 1024px;
  display: flex;
}

.part {
  flex: 1;
  height: 500px;
}

.question {
}

.answer {
}

.guesses {
}

.guess {
  padding: $grid;
  background-color: colors.color(grey-200);
}

.tabs-component {
  height:100%;
  display: flex;
  flex-direction: column;
}

.tabs-component-tabs {
  padding: 0;
  margin: 0;
  display: flex;
  flex-wrap: wrap;
}

.tabs-component-tab {
  display: inline-block;
  cursor: pointer;
  &.is-active {
    border-bottom: 2px solid colors.color(green-500);
  }
  a {
    display: block;
    padding: $grid 2 * $grid;
    text-decoration: none;
    color: black;
  }
}

.tabs-component-panels {
  flex: 1 0 auto;
  height: 0;
}

.tabs-component-panel {
  line-height: 1.5;
  box-sizing: border-box;
  height:100%;
  overflow-y: auto;
  padding: 2 * $grid;
}
</style>