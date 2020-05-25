<template>
  <div class="tabar">
    <item txt="首页" mask="home" :currChild="curr" @change="getval">
      <img slot="img1" src="./../assets/images/ic_tab_home_normal.png" alt />
      <img slot="img2" src="./../assets/images/ic_tab_home_active.png" alt />
    </item>
    <item txt="书影音" mask="audio" :currChild="curr" @change="getval">
      <img slot="img1" src="./../assets/images/ic_tab_subject_normal.png" alt />
      <img slot="img2" src="./../assets/images/ic_tab_subject_active.png" alt />
    </item>
    <item txt="广播" mask="broadcast" :currChild="curr" @change="getval">
      <img slot="img1" src="./../assets/images/ic_tab_status_normal.png" alt />
      <img slot="img2" src="./../assets/images/ic_tab_status_active.png" alt />
    </item>
    <item txt="小组" mask="group" :currChild="curr" @change="getval">
      <img slot="img1" src="./../assets/images/ic_tab_group_normal.png" alt />
      <img slot="img2" src="./../assets/images/ic_tab_group_active.png" alt />
    </item>
    <item txt="我的" mask="mine" :currChild="curr" @change="getval">
      <img slot="img1" src="./../assets/images/ic_tab_profile_normal.png" alt />
      <img slot="img2" src="./../assets/images/ic_tab_profile_active.png" alt />
    </item>
  </div>
</template>

<script type="text/ecmascript-6">
import item from "./item";
export default {
  name: "tabar",
  data() {
    return {
      curr: "home"
    };
  },
  components: {
    item
  },
  methods: {
    getval(val) {
      console.log(val);
      this.curr = val;
    }
  }
};
</script>

<style scoped lang="less">
.tabar {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #fff;
  position: fixed;
  bottom: 0;
  left: 0;
  border-top: 1px solid #ccc;
  img {
    height: 70/100rem;
  }
}
</style>
