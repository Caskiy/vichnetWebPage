<template>


  <div  class="op-box" :class="{'alert':alertColor}">
    <div id="roof">
      <SelectLanguage id="lang"></SelectLanguage>
      <h1 id="title">人手防护安全预警系统</h1>
      <img src="img/vichnetlog.png" id="log"/>
    </div>
      <card id="cardID">
        <FunctionButton></FunctionButton>
      </card>
  </div>

</template>

<script>
  import alertNote from './Notifications/alertNotification';
  import { BaseAlert } from '@/components';
  import FunctionButton from "@/pages/Dashboard/FunctionButton";

  import SelectLanguage from "@/pages/Dashboard/SelectLanguage";

  require('../assets/css/roof.css')


  export default {
    components: {
      FunctionButton,

      BaseAlert,
      SelectLanguage

    },
    data() {
      return {
        alertColor: false,
        type: ["", "info", "success", "warning", "danger"],
        notifications: {
          topCenter: false
        }
      };
    },
    methods: {
      notifyVue(verticalAlign, horizontalAlign) {
        const color = Math.floor(Math.random() * 4 + 1);
        this.$notify({
          component: alertNote,
          icon: "tim-icons icon-bell-55",
          horizontalAlign: horizontalAlign,
          verticalAlign: verticalAlign,
          type: this.type[color],
          timeout: 0
        });
      },
      alertbtn() {
        this.alertColor = true;
      }
    }
  };
</script>

<style scoped type="text/scss">
  @import "../assets/sass/Dashboard/videoBoard.scss";

  #cardID{
    width: 100%;
    margin:0;

    transform:scale(1.05);

    position: relative;
    top: -50px;
    height: 430px;
    background-color: #444647;
  }


</style>
