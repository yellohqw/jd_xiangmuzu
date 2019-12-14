<template>
    <span>{{countDown(endDate)}}</span>
</template>
<script>
import moment from "moment";
export default {
  data() {
    return {
      now: moment(),
      endDate: "2019-12-17 08:00:00"
    };
  },
  mounted() {
    //定时更新当前时间
    setInterval(() => {
      this.now = moment();
    }, 1000);
    //数字前补 0
    // num传入的数字，n需要的字符长度
  },
  methods: {
    PrefixInteger(num, n) {
      return (Array(n).join(0) + num).slice(-n);
    }
  },
  computed: {
    //计算属性，返回剩余时间
    countDown() {
      return function(endDate) {
        let m1 = this.now;
        let m2 = moment(endDate);
        var du = moment.duration(m2 - m1, "ms"),
          hours = du.get("hours"),
          mins = du.get("minutes"),
          ss = du.get("seconds");
        if (hours <= 0 && mins <= 0 && ss <= 0) {
          return "已超时";
        } else {
          return (
            this.PrefixInteger(hours, 2) +
            ":" +
            this.PrefixInteger(mins, 2) +
            ":" +
            this.PrefixInteger(ss, 2)
          );
        }
      };
    }
  }
};
</script>
<style>
</style>
