<template>
  <section id="profile">
    <row>
      <column md="3">
        <card cascade narrow>
          <view-wrapper>
            <img src="https://mdbootstrap.com/img/Photos/Horizontal/People/6-col/img%20%283%29.jpg" alt="Project" class="img-fluid"/>
            <md-mask overlay="white-slight" waves/>
          </view-wrapper>
          <card-body class="text-center">
            <card-title class="font-bold mb-2">
              <strong>Alice Mayer</strong>
            </card-title>
            <h5 class="indigo-text">
              <strong>Photographer</strong>
            </h5>
            <h6 class="text-justify">
              <strong>About:</strong>
            </h6>
            <p class="text-justify">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ratione perferendis quod animi dignissimos consectetur quibusdam numquam laboriosam, minus, provident...</p>
            <div class="text-right">
              <btn outline="primary" rounded size="sm">More...</btn>
            </div>
          </card-body>
        </card>
      </column>
      <column md="9">
        <section class="text-center pb-3">
          <row class="d-flex justify-content-center">
            <column lg="6" xl="5" class="mb-3">
              <card cascade narrow class="d-flex mb-5">
                <view-wrapper>
                  <img src="https://mdbootstrap.com/img/Mockups/Horizontal/6-col/pro-profile-page.jpg" alt="Project" class="img-fluid"/>
                  <md-mask overlay="white-slight" waves/>
                </view-wrapper>
                <card-body>
                  <card-title class="font-bold mb-3">
                    <strong>Project name</strong>
                  </card-title>
                  <card-text>Some quick example text to build on the card title and make up the bulk of the card's content.</card-text>
                </card-body>
                <card-footer class="links-light profile-card-footer">
                  <span class="right">
                    <a class="p-2" href="#profile">
                      Live Preview
                      <fa icon="photo" class="ml-1"/>
                    </a>
                  </span>
                </card-footer>
              </card>
            </column>
            <column lg="6" xl="5" class="mb-3">
              <card cascade narrow class="d-flex mb-5">
                <view-wrapper>
                  <img src="https://mdbootstrap.com/img/Mockups/Horizontal/6-col/pro-signup.jpg" alt="Project" class="img-fluid"/>
                  <md-mask overlay="white-slight" waves/>
                </view-wrapper>
                <card-body>
                  <card-title class="font-bold mb-3">
                    <strong>Project name</strong>
                  </card-title>
                  <card-text>Some quick example text to build on the card title and make up the bulk of the card's content.</card-text>
                </card-body>
                <card-footer class="links-light profile-card-footer">
                  <span class="right">
                    <a class="p-2" href="#profile">
                      Live Preview
                      <fa icon="photo" class="ml-1"/>
                    </a>
                  </span>
                </card-footer>
              </card>
            </column>
          </row>
          <row class="d-flex justify-content-center">
            <column lg="6" xl="5" class="mb-3">
              <card cascade narrow class="d-flex mb-5">
                <view-wrapper>
                  <img src="https://mdbootstrap.com/img/Mockups/Horizontal/6-col/pro-pricing.jpg" alt="Project" class="img-fluid"/>
                  <md-mask overlay="white-slight" waves/>
                </view-wrapper>
                <card-body>
                  <card-title class="font-bold mb-3">
                    <strong>Project name</strong>
                  </card-title>
                  <card-text>Some quick example text to build on the card title and make up the bulk of the card's content.</card-text>
                </card-body>
                <card-footer class="links-light profile-card-footer">
                  <span class="right">
                    <a class="p-2" href="#profile">
                      Live Preview
                      <fa icon="photo" class="ml-1"/>
                    </a>
                  </span>
                </card-footer>
              </card>
            </column>
            <column lg="6" xl="5" class="mb-3">
              <card cascade narrow class="d-flex mb-5">
                <view-wrapper>
                  <img src="https://mdbootstrap.com/img/Mockups/Horizontal/6-col/pro-landing.jpg" alt="Project" class="img-fluid"/>
                  <md-mask overlay="white-slight" waves/>
                </view-wrapper>
                <card-body>
                  <card-title class="font-bold mb-3">
                    <strong>Project name</strong>
                  </card-title>
                  <card-text>Some quick example text to build on the card title and make up the bulk of the card's content.</card-text>
                </card-body>
                <card-footer class="links-light profile-card-footer">
                  <span class="right">
                    <a class="p-2" href="#profile">
                      Live Preview
                      <fa icon="photo" class="ml-1"/>
                    </a>
                  </span>
                </card-footer>
              </card>
            </column>
            <column lg="12">
              <div class="text-center">
                <pagination circle color="blue">
                  <page-item disabled>First</page-item>
                  <page-nav prev></page-nav>
                  <page-item active>1</page-item>
                  <page-item>2</page-item>
                  <page-item>3</page-item>
                  <page-item>4</page-item>
                  <page-item>5</page-item>
                  <page-nav next></page-nav>
                  <page-item disabled>Last</page-item>
                </pagination>
              </div>
            </column>
          </row>
        </section>
      </column>
    </row>
    <row>

    </row>
  </section>
</template>

<script>
import { Row, Column, Card, CardBody, ViewWrapper, MdMask, CardTitle, CardText, CardFooter, Fa, Btn, Pagination, PageNav, PageItem } from 'mdbvue'

export default {
  name: 'Profile',
  components: {
    Row,
    Column,
    Card,
    CardBody,
    ViewWrapper,
    MdMask,
    CardTitle,
    CardText,
    CardFooter,
    Fa,
    Btn,
    Pagination,
    PageNav,
    PageItem
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.profile-card-footer {
  background-color: #F7F7F7 !important;
  padding: 1.25rem;
}
.card.card-cascade .view {
  box-shadow: 0 3px 10px 0 rgba(0, 0, 0, 0.15), 0 3px 12px 0 rgba(0, 0, 0, 0.15);
}
</style>
