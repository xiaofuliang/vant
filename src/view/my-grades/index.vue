<template>
  <div>
    <van-tabs sticky color="#1989fa" animated :offset-top="1" >
      <van-tab title="考试成绩">
          <van-list
            v-model="loading"
            :finished="finished"
            finished-text="没有数据"
            @load="onLoad"
          >
          <van-cell  v-for="item in list" :key="item.id" :value="item.createtime" isLink >
            {{item.name}}
				<div class="van-cell__label">
				<div>
				  科目：{{item.subjectname}}
				</div>
				<div>
				  考试时间：{{item.createtime}}
				</div>
				<div>
				  总分：{{item.totalscore}}&nbsp;&nbsp;考试得分：{{item.score}}
				</div>
            </div>
          </van-cell>
          </van-list>
      </van-tab>
      <van-tab title="考试排行"></van-tab>
    </van-tabs>
	
	
	
  </div>
</template>

<script>
import { Cell, List, PullRefresh, Tab, Tabs,	Tabbar,
		TabbarItem,
		Icon  } from "vant";

export default {
  components: {
    [Cell.name]: Cell,
    [List.name]: List,
    [PullRefresh.name]: PullRefresh,
    [Tab.name]: Tab,
    [Tabs.name]: Tabs,
	[Tabbar.name]: Tabbar,
	[TabbarItem.name]: TabbarItem,
	[Icon.name]: Icon,
	[Tabbar.name]: Tabbar,
	[TabbarItem.name]: TabbarItem,
	[Icon.name]: Icon
  },

  data() {
    return {
      active: 0,
      
      loading: false,
      finished: false,
	  list:[{
		  name:"小学一年级数学期末试卷",
		  subjectname:"数学",
		  createtime:"2019-10-19 09:00:00",
		  totalscore:"100",
		  score:"80"
	  },
	  {
	  		  name:"小学二年级语文期末试卷",
	  		  subjectname:"语文",
	  		  createtime:"2019-12-19 09:00:00",
	  		  totalscore:"100",
	  		  score:"70"
	  },
	  {
	  		  name:"小学二年级语文期末试卷",
	  		  subjectname:"语文",
	  		  createtime:"2019-12-19 09:00:00",
	  		  totalscore:"100",
	  		  score:"70"
	  },
	  {
	  		  name:"小学二年级语文期末试卷",
	  		  subjectname:"语文",
	  		  createtime:"2019-12-19 09:00:00",
	  		  totalscore:"100",
	  		  score:"70"
	  },
	  {
	  		  name:"小学二年级语文期末试卷",
	  		  subjectname:"语文",
	  		  createtime:"2019-12-19 09:00:00",
	  		  totalscore:"100",
	  		  score:"70"
	  },
	  {
	  		  name:"小学二年级语文期末试卷",
	  		  subjectname:"语文",
	  		  createtime:"2019-12-19 09:00:00",
	  		  totalscore:"100",
	  		  score:"70"
	  },
	  {
	  		  name:"小学二年级语文期末试卷",
	  		  subjectname:"语文",
	  		  createtime:"2019-12-19 09:00:00",
	  		  totalscore:"100",
	  		  score:"70"
	  }
	  ]
    };
  },

  methods: {
    onLoad() {
      // 异步更新数据
      this.loadData();
    },
    loadData() {
     
    }
  }
};
</script>

<style lang="less">
</style>
