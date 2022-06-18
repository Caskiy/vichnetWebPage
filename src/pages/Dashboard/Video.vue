<template>
  <div>
<!--    <h2 id="title">人手防护安全预警系统</h2>-->
<!--    <img src="img/vichnetlog.png" id="log"/>-->
    <img src="img/videoImg.png" id="vid"/>

<!--    <SelectLanguage id="lang"></SelectLanguage>-->
    <Time id="time"></Time>

  </div>
</template>

<script>
import SelectLanguage from "@/pages/Dashboard/SelectLanguage";
import Time from "@/pages/Dashboard/Time";

export default {
  name: "Video",
  components:{
    SelectLanguage,
    Time
  }
}

</script>

<style scoped>

#vid{
  position: relative;
  top: 15px;
  width: 480px;
  height: 270px;
}

#time{
  position: relative;
  top: 17px;
  left: 40px;
  transform:scale(1.2);
  font-size: 10px;


  background-color: burlywood;
  width: 400px;
}

</style>
