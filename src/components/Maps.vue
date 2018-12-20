<template>
  <section id="maps">
    <mdb-row>
      <mdb-col md="6">
        <mdb-card cascade narrow class="mt-5">
          <mdb-view class="gradient-card-header blue darken-2">
            <h4 class="h4-responsive text-white">
              Regular map
            </h4>
          </mdb-view>
          <mdb-card-body class="text-center">
            <GmapMap
              :center="{lat:10, lng:10}"
              :zoom="7"
              style="width: 100%; height: 300px"
            >
            </GmapMap>
          </mdb-card-body>
        </mdb-card>
      </mdb-col>
      <mdb-col md="6">
        <mdb-card cascade narrow class="mt-5">
          <mdb-view class="gradient-card-header blue darken-2">
            <h4 class="h4-responsive text-white">
              Hybrid map
            </h4>
          </mdb-view>
          <mdb-card-body class="text-center">
            <GmapMap
              :center="{lat:10, lng:10}"
              :zoom="7"
              map-type-id="hybrid"
              style="width: 100%; height: 300px"
            >
            </GmapMap>
          </mdb-card-body>
        </mdb-card>
      </mdb-col>
    </mdb-row>
    <mdb-row>
      <mdb-col md="6">
        <mdb-card cascade narrow class="mt-5">
          <mdb-view class="gradient-card-header blue darken-2">
            <h4 class="h4-responsive text-white">
              Satellite map
            </h4>
          </mdb-view>
          <mdb-card-body class="text-center">
            <GmapMap
              :center="{lat:10, lng:10}"
              :zoom="7"
              map-type-id="satellite"
              style="width: 100%; height: 300px"
            >
            </GmapMap>
          </mdb-card-body>
        </mdb-card>
      </mdb-col>
      <mdb-col md="6">
        <mdb-card cascade narrow class="mt-5">
          <mdb-view class="gradient-card-header blue darken-2">
            <h4 class="h4-responsive text-white">
              Terrain map
            </h4>
          </mdb-view>
          <mdb-card-body class="text-center">
            <GmapMap
              :center="{lat:10, lng:10}"
              :zoom="7"
              map-type-id="terrain"
              style="width: 100%; height: 300px"
            >
            </GmapMap>
          </mdb-card-body>
        </mdb-card>
      </mdb-col>
    </mdb-row>
  </section>
</template>

<script>
import { mdbRow, mdbCol, mdbCard, mdbView, mdbCardBody } from 'mdbvue'

export default {
  name: 'Maps',
  components: {
    mdbRow,
    mdbCol,
    mdbCard,
    mdbView,
    mdbCardBody
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card.card-cascade .view.gradient-card-header {
  padding: 1rem 1rem;
  text-align: center;
}
.card.card-cascade h3, .card.card-cascade h4 {
  margin-bottom: 0px;
}
</style>
