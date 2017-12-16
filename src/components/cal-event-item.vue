<template>
  <div class="wrapper">
    <h3 class="title strong">{{event.title}}</h3>
    <div id="event-item-wrapper">
      <div class="desc-wrapper">
        <p class="desc">{{event.desc}}</p>
      </div>
      <div class="time-wrapper">
        <p class="time">{{dateTimeFormatter(Date.parse(new Date(event.date)),i18n[locale].fullFormat)}}</p>
    </div>
    </div>
  </div>
</template>
<script>
import i18n from '../i18n.js'
import { dateTimeFormatter } from '../tools.js'
export default {
  data () {
    return {
      i18n
    }
  },
  props: {
    event: {
      type: Object,
      required: true
    },
    index: {
      type: Number,
      required: true
    },
    locale: {
      type: String,
      required: true
    }
  },
  methods: {
    dateTimeFormatter
  }
}
</script>