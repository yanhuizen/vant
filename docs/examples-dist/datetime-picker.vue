<template><section class="demo-datetime"><h1 class="demo-title">Datetime Picker 时间选择</h1><example-block title="基础用法">
                <van-datetime-picker v-model="currentDate" type="datetime" format="yyyy.mm.dd hh时 mm分" :min-hour="minHour" :max-hour="maxHour" :min-date="minDate" @change="handlePickerChange">  
</van-datetime-picker>



              </example-block><example-block title="选择日期">
                <van-datetime-picker v-model="currentDate" type="date" format="yyyy.mm.dd hh时 mm分" :min-hour="minHour" :max-hour="maxHour" :min-date="minDate" @change="handlePickerChange">  
</van-datetime-picker>

              </example-block><example-block title="选择时间">
                <van-datetime-picker v-model="currentDate" type="time" format="yyyy.mm.dd hh时 mm分" :min-hour="minHour" :max-hour="maxHour" :min-date="minDate" @change="handlePickerChange">  
</van-datetime-picker>

              </example-block></section></template>

<script>
import Vue from "vue";import ExampleBlock from "components/example-block";Vue.component("example-block", ExampleBlock);
export default {
  data() {
    return {
      minHour: 10,
      maxHour: 20,
      minDate: new Date(),
      currentDate: null
    };
  },

  methods: {
    handlePickerChange(picker, values) {
      // picker.setColumnValues(1, citys[values[0]]);
      console.log(values);
    },
    handlePickerCancel() {
      alert('picker cancel');
    },
    handlePickerConfirm() {
      alert('picker confirm');
    }
  }
};
</script>