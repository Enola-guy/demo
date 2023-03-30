<template>
  <div class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0">
    <div class="max-w-4xl mx-auto sm:px-6 lg:px-8">
      <div class="mt-8 bg-white overflow-hidden shadow sm:rounded-lg p-6">
        <h2 class="text-2xl leading-7 font-semibold">
          Welcome to my bug
        </h2>
        <p class="mt-3 text-gray-600">
        <span id="foobar">Hover me and bye bye</span>
          <b-tooltip
            target='foobar'
            triggers="hover"
          >
            <ToolTipLink
              :path="mylinks"
            />
          </b-tooltip>
        </p>
        <p>
          BUG with bootstrap-vue@2.23.0
          NO BUG with bootstrap-vue@2.22.0
        </p>
      </div>
    </div>
  </div>
</template>


<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage',

  data() {
    return {
      mylinks: [{name:"one",id:1},{name:"two", id:2}]
    }
  },
})
</script>
