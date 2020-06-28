<template>
    <div>
        <h1>
            This is the about page
        </h1>
        <div class="grp">
            <div class="pane">1</div>
            <div class="pane">2</div>
        </div>

    </div>
</template>

<script>
import axios from 'axios'

export default {
    asyncData ({ params, error }) {
    return axios.get(`https://api.catsone.nl/v3/jobs`)
      .then((res) => {
        return { job: res.data }
      })
      .catch((e) => {
        console.log(e)
      })
  },
  data() {
    return {
      
    }
  }

}
</script>