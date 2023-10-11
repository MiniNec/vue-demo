<script setup lang="ts">
import { ref, reactive, nextTick } from 'vue';
import glass from '@/components/Glass.vue';
import lGlass from '@/components/LGlass.vue';
import chance from '@/components/Chance.vue';
import lChance from '@/components/LChance.vue';
import lBank from '@/components/LBank.vue';
import square from '@/components/Square.vue';
import player from '@/components/Player.vue';
import player1 from '@/components/player/Player1.vue';

const player1_pos = ref(0);
const player1_x = ref(1620);
const player1_y = ref(1620);

const showBtnThrow = ref(true);

const pos0 = ref<any>();
const pos1 = ref<any>();
const pos2 = ref<any>();
const pos3 = ref<any>();
const pos4 = ref<any>();
const pos5 = ref<any>();
const pos6 = ref<any>();
const pos7 = ref<any>();
const pos8 = ref<any>();
const pos9 = ref<any>();
const pos10 = ref<any>();
const pos11 = ref<any>();
const pos12 = ref<any>();
const pos13 = ref<any>();
const pos14 = ref<any>();
const pos15 = ref<any>();
const pos16 = ref<any>();
const pos17 = ref<any>();
const pos18 = ref<any>();
const pos19 = ref<any>();
const pos20 = ref<any>();
const pos21 = ref<any>();
const pos22 = ref<any>();
const pos23 = ref<any>();
const pos24 = ref<any>();
const pos25 = ref<any>();
const pos26 = ref<any>();
const pos27 = ref<any>();
const pos28 = ref<any>();
const pos29 = ref<any>();
const pos30 = ref<any>();
const pos31 = ref<any>();

nextTick(() => {});

const pos_list = ref([
  pos0,
  pos1,
  pos2,
  pos3,
  pos4,
  pos5,
  pos6,
  pos7,
  pos8,
  pos9,
  pos10,
  pos11,
  pos12,
  pos13,
  pos14,
  pos15,
  pos16,
  pos17,
  pos18,
  pos19,
  pos20,
  pos21,
  pos22,
  pos23,
  pos24,
  pos25,
  pos26,
  pos27,
  pos28,
  pos29,
  pos30,
  pos31,
]);

// 掷色子调用的函数
const btnThrowDice = async () => {
  // step1:隐藏掷色子
  showBtnThrow.value = false;
  // step2:移动到指定位置
  movePlayer1();
  await sleep(250);
  // step3:判断角色是罚款还是购买还是特殊
  if (player1_pos.value == 0) {
    // 回到起点,移动时已经增加钱了，不需要操作
  } else if (player1_pos.value in []) {
  }
  showBtnThrow.value = true;
};

const showHouseTest = () => {
  pos_list.value[0].value.showHouse(1);
  pos_list.value[1].value.showHouse(2);
};

const setMultipleTest = () => {
  pos_list.value[0].value.setMultiple('X3');
};

const movePlayer1 = () => {
  var now_pos = player1_pos.value;
  var dice = Math.floor(Math.random() * 11) + 2;
  player1_pos.value = player1_pos.value + dice;
  player1_pos.value = player1_pos.value % 32;
  if (now_pos > player1_pos.value) {
    // console.log(player1_data.value.money);
    player1_data.value.money = player1_data.value.money + 500;
  }
  console.log('原来:' + now_pos, '筛子:' + dice, '现在:' + player1_pos.value);
  player1_x.value = pos_center_list.value[player1_pos.value][0];
  player1_y.value = pos_center_list.value[player1_pos.value][1];
};

const player1_data = ref({
  player_id: 1,
  name: '玩家1',
  money: 2000,
  player_owner: [],
});

const sleep = (ms) => {
  return new Promise((resolve) => setTimeout(resolve, ms));
};

const pos_center_list = ref([
  [1620, 1620],
  [1410, 1620],
  [1230, 1620],
  [1050, 1620],
  [870, 1620],
  [690, 1620],
  [510, 1620],
  [330, 1620],
  [120, 1620],
  [120, 1410],
  [120, 1230],
  [120, 1050],
  [120, 870],
  [120, 690],
  [120, 510],
  [120, 330],
  [120, 120],
  [330, 120],
  [510, 120],
  [690, 120],
  [870, 120],
  [1050, 120],
  [1230, 120],
  [1410, 120],
  [1620, 120],
  [1620, 330],
  [1620, 510],
  [1620, 690],
  [1620, 870],
  [1620, 1050],
  [1620, 1230],
  [1620, 1410],
]);

const pos_data_list = ref([
  {
    id: 0,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 1,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 2,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 3,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 4,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 5,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 6,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 7,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 8,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 9,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 10,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 11,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 12,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 13,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 14,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 15,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 16,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 17,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 18,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 19,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 20,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 21,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 22,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 23,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 24,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 25,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 26,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 27,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 28,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 29,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 30,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
  {
    id: 31,
    owner: 0,
    level: 0,
    need_money: [100, 200, 300, 400],
  },
]);
</script>

<template>
  <div class="gameScreen">
    <div class="container">
      <square
        ref="pos16"
        style="position: absolute; top: 0px; left: 0px"
        rDeg="0"
        text="世界杯"
        color="pink"
      ></square>
      <glass
        ref="pos15"
        style="position: absolute; top: 0px; left: 240px"
        rDeg="0"
        text="布拉格"
        color="#DE4BF4"
      ></glass>
      <glass
        ref="pos14"
        style="position: absolute; top: 0px; left: 420px"
        rDeg="0"
        text="普吉岛"
        color="#8AE2D5"
      ></glass>
      <glass
        ref="pos13"
        style="position: absolute; top: 0px; left: 600px"
        rDeg="0"
        text="柏林"
        color="#DE4BF4"
      ></glass>
      <chance
        ref="pos12"
        style="position: absolute; top: 0px; left: 780px"
        rDeg="0"
        text="机会"
        color="#E8EDE8"
      ></chance>
      <glass
        ref="pos11"
        style="position: absolute; top: 0px; left: 960px"
        rDeg="0"
        text="莫斯科"
        color="#9603AD"
      ></glass>
      <glass
        ref="pos10"
        style="position: absolute; top: 0px; left: 1140px"
        rDeg="0"
        text="日内瓦"
        color="#9603AD"
      ></glass>
      <glass
        ref="pos9"
        style="position: absolute; top: 0px; left: 1320px"
        rDeg="0"
        text="罗马"
        color="#9603AD"
      ></glass>
      <square
        ref="pos8"
        style="position: absolute; top: 0px; left: 1500px"
        rDeg="0"
        text="世界旅游"
        color="pink"
      ></square>
      <lGlass
        ref="pos17"
        style="position: absolute; top: 240px; left: 0px"
        text="圣保罗"
        color="blue"
      ></lGlass>
      <lGlass
        ref="pos18"
        style="position: absolute; top: 420px; left: 0px"
        text="夏威夷"
        color="#8AE2D5"
      ></lGlass>
      <lGlass
        ref="pos19"
        style="position: absolute; top: 600px; left: 0px"
        text="魁北克"
        color="blue"
      ></lGlass>
      <lChance
        ref="pos20"
        style="position: absolute; top: 780px; left: 0px"
        text="机会"
        color="#E8EDE8"
      ></lChance>
      <lGlass
        ref="pos21"
        style="position: absolute; top: 960px; left: 0px"
        text="悉尼"
        color="#3498DB"
      ></lGlass>
      <lGlass
        ref="pos22"
        style="position: absolute; top: 1140px; left: 0px"
        text="东京"
        color="#3498DB"
      ></lGlass>
      <lGlass
        ref="pos23"
        style="position: absolute; top: 1320px; left: 0px"
        text="巴厘岛"
        color="#8AE2D5"
      ></lGlass>
      <lGlass
        ref="pos7"
        style="position: absolute; top: 240px; left: 1500px"
        text="塔希提岛"
        color="#8AE2D5"
      ></lGlass>
      <lGlass
        ref="pos6"
        style="position: absolute; top: 420px; left: 1500px"
        text="伦敦"
        color="#ED954E"
      ></lGlass>
      <lGlass
        ref="pos5"
        style="position: absolute; top: 600px; left: 1500px"
        text="巴黎"
        color="#ED954E"
      ></lGlass>
      <lChance
        ref="pos4"
        style="position: absolute; top: 780px; left: 1500px"
        text="机会"
        color="#E8EDE8"
      ></lChance>
      <lGlass
        ref="pos3"
        style="position: absolute; top: 960px; left: 1500px"
        text="纽约"
        color="#ED1717"
      ></lGlass>
      <lBank
        ref="pos2"
        style="position: absolute; top: 1140px; left: 1500px"
        text="国税局"
        color="#E8EDE8"
      ></lBank>
      <lGlass
        ref="pos1"
        style="position: absolute; top: 1320px; left: 1500px"
        text="北京"
        color="#ED1717"
      ></lGlass>
      <square
        ref="pos24"
        style="position: absolute; top: 1500px; left: 0px"
        rDeg="0"
        text="无人岛"
        color="pink"
      ></square>
      <glass
        ref="pos25"
        style="position: absolute; top: 1500px; left: 240px"
        rDeg="0"
        text="开罗"
        color="#2EC12E"
      ></glass>
      <glass
        ref="pos26"
        style="position: absolute; top: 1500px; left: 420px"
        rDeg="0"
        text="迪拜"
        color="#2EC12E"
      ></glass>
      <glass
        ref="pos27"
        style="position: absolute; top: 1500px; left: 600px"
        rDeg="0"
        text="新德里"
        color="#2EC12E"
      ></glass>
      <glass
        ref="pos28"
        style="position: absolute; top: 1500px; left: 780px"
        rDeg="0"
        text="马尔代夫"
        color="#8AE2D5"
      ></glass>
      <glass
        ref="pos29"
        style="position: absolute; top: 1500px; left: 960px"
        rDeg="0"
        text="首尔"
        color="#00FF00"
      ></glass>
      <chance
        ref="pos30"
        style="position: absolute; top: 1500px; left: 1140px"
        rDeg="0"
        text="奖励"
        color="#E8EDE8"
      ></chance>
      <glass
        ref="pos31"
        style="position: absolute; top: 1500px; left: 1320px"
        rDeg="0"
        text="曼谷"
        color="#00FF00"
      ></glass>
      <square
        ref="pos0"
        style="position: absolute; top: 1500px; left: 1500px"
        rDeg="0"
        text="起点"
        color="pink"
      ></square>
      <player1 class="player_style1"></player1>
      <div class="player_card1">
        <div>玩家昵称: {{ player1_data.name }}</div>
        <div>金币: {{ player1_data.money }}</div>
      </div>
      <el-button v-if="showBtnThrow" class="btnThrow" @click="btnThrowDice"
        >测试</el-button
      >
    </div>
  </div>
</template>

<style scoped>
.gameScreen {
  display: flex;
  position: absolute;
  width: 1740px;
  height: 1740px;
  top: -500px;
  left: -200px;
  scale: 0.4;
}
.container {
  display: flex;
  position: absolute;
  /* justify-content: center; */
  /* align-items: center; */
  /* scale: 0.8; */
  width: 1740px;
  height: 1740px;
  top: 0px;
  left: 0px;
}
.player_style1 {
  position: absolute;
  width: 120px;
  height: 120px;
  top: v-bind(player1_x + 'px');
  left: v-bind(player1_y + 'px');
  transition: 0.25s linear 0s;
  font-size: 40px;
  background-color: #000;
  color: #fff;
  justify-content: center;
  align-items: center;
}
.btnThrow {
  position: absolute;
  width: 140px;
  height: 140px;
  top: 1700px;
  left: 1900px;
  background-color: #1fefff;
  color: #fff;
  font-size: 40px;
}
.player_card1 {
  position: absolute;
  width: 500px;
  height: 200px;
  top: 1700px;
  left: -550px;
  background-color: #123321;
  font-size: 50px;
  color: #fff;
}
</style>
