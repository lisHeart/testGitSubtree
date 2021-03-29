<template>
  <div id="app">

    <!--  水平时间线-->
    <div class="demo-row">
      <timeline timeline-theme="#0096F2"
                v-on:nodeClick="nodeClick"
                v-on:picItemClick="picItemClick"
                timeline-direction="row"
                :data-source="dataSource">

      </timeline>
    </div>

    <!--   垂直时间线-->
    <div class="demo-column">
      <!--   时间轴在左边-->
      <timeline style="width: 200px"
                v-on:picItemClick="picItemClick"
                timeline-theme="#0096F2"
                timeline-direction="column-left"
                :data-source="dataSource">
      </timeline>

      <!--      时间轴在右边-->
      <timeline timeline-theme="#0096F2"
                v-on:picItemClick="picItemClick"
                timeline-direction="column-right"
                :data-source="dataSource">
      </timeline>

    </div>

  </div>
</template>

<script>
import { Timeline, TimelineItem, TimelineTitle } from '../YW/YWTimeLine'

export default {
  components: {
    Timeline,
    TimelineItem,
    TimelineTitle
  },
  methods: {
    picItemClick(item) {
      alert('item被点击');
    },
    nodeClick(model) {
      alert('节点被点击')
    }
  },
  data() {
    return {
      dataSource:[{
        time:'2017-2-12',
        name:'33333',
        imgPath: 'https://user-images.githubusercontent.com/12069729/36057805-80cfc3d2-0e4e-11e8-8851-6fda091ff389.png'
      },{
        time:'2017-2-1',
        name:'33333',
        imgPath: 'https://user-images.githubusercontent.com/12069729/36057805-80cfc3d2-0e4e-11e8-8851-6fda091ff389.png'

      },{
        time:'2017-2-1\n2017-2-11',
        name:'333333333333333333333333',
        imgPath: 'https://user-images.githubusercontent.com/12069729/36057805-80cfc3d2-0e4e-11e8-8851-6fda091ff389.png'
      },{
        time:'2017-2-1',
        name:'33333',
        imgPath: 'https://user-images.githubusercontent.com/12069729/36057805-80cfc3d2-0e4e-11e8-8851-6fda091ff389.png'
      },{
        time:'2017-2-1\n2017-2-11',
        name:'33333',
        imgPath: 'https://user-images.githubusercontent.com/12069729/36057805-80cfc3d2-0e4e-11e8-8851-6fda091ff389.png'
      },{
        time:'2017-2-1',
        name:'33333',
        imgPath: 'https://user-images.githubusercontent.com/12069729/36057805-80cfc3d2-0e4e-11e8-8851-6fda091ff389.png'
      },{
        time:'2017-2-1\n2017-2-11',
        name:'33333',
        imgPath: 'https://user-images.githubusercontent.com/12069729/36057805-80cfc3d2-0e4e-11e8-8851-6fda091ff389.png'
      },{
        time:'2017-2-1\n2017-2-11',
        name:'33333',
        imgPath: 'https://user-images.githubusercontent.com/12069729/36057805-80cfc3d2-0e4e-11e8-8851-6fda091ff389.png'
      }],
    }

  }
}
</script>

<style>
.demo-column{
  margin-top: 50px;
  display: flex;
}
.append {
  font-size: .8em;
  margin-top: 3px;
  color: #646C7C;
}

a {
  color: #bf6dcf;
  font-weight: bold;
  text-decoration: none;
}

.icon-heart {
  width: 20px;
}
.demo-them{
  margin-left: 10px;
}
.demo {
  display: grid;
  grid-template-columns: repeat(2, 50%);
  grid-gap: 1rem;
}

.demo-theme.dark {
  background: #3a3939;
}

.github-corner:hover .octo-arm{animation:octocat-wave 560ms ease-in-out}@keyframes octocat-wave{0%,100%{transform:rotate(0)}20%,60%{transform:rotate(-25deg)}40%,80%{transform:rotate(10deg)}}@media (max-width:500px){.github-corner:hover .octo-arm{animation:none}.github-corner .octo-arm{animation:octocat-wave 560ms ease-in-out}}
</style>
