<template>
  <section id="maps">
    <row>
      <column md="6">
        <card cascade narrow class="mt-5">
          <view-wrapper class="gradient-card-header blue darken-2">
            <h4 class="h4-responsive text-white">
              Regular map
            </h4>
          </view-wrapper>
          <card-body class="text-center">
            <GmapMap
              :center="{lat:10, lng:10}"
              :zoom="7"
              style="width: 100%; height: 300px"
            >
            </GmapMap>
          </card-body>
        </card>
      </column>
      <column md="6">
        <card cascade narrow class="mt-5">
          <view-wrapper class="gradient-card-header blue darken-2">
            <h4 class="h4-responsive text-white">
              Hybrid map
            </h4>
          </view-wrapper>
          <card-body class="text-center">
            <GmapMap
              :center="{lat:10, lng:10}"
              :zoom="7"
              map-type-id="hybrid"
              style="width: 100%; height: 300px"
            >
            </GmapMap>
          </card-body>
        </card>
      </column>
    </row>
    <row>
      <column md="6">
        <card cascade narrow class="mt-5">
          <view-wrapper class="gradient-card-header blue darken-2">
            <h4 class="h4-responsive text-white">
              Satellite map
            </h4>
          </view-wrapper>
          <card-body class="text-center">
            <GmapMap
              :center="{lat:10, lng:10}"
              :zoom="7"
              map-type-id="satellite"
              style="width: 100%; height: 300px"
            >
            </GmapMap>
          </card-body>
        </card>
      </column>
      <column md="6">
        <card cascade narrow class="mt-5">
          <view-wrapper class="gradient-card-header blue darken-2">
            <h4 class="h4-responsive text-white">
              Terrain map
            </h4>
          </view-wrapper>
          <card-body class="text-center">
            <GmapMap
              :center="{lat:10, lng:10}"
              :zoom="7"
              map-type-id="terrain"
              style="width: 100%; height: 300px"
            >
            </GmapMap>
          </card-body>
        </card>
      </column>
    </row>
  </section>
</template>

<script>
import { Row, Column, Card, ViewWrapper, CardBody } from 'mdbvue'

export default {
  name: 'Maps',
  components: {
    Row,
    Column,
    Card,
    ViewWrapper,
    CardBody
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
