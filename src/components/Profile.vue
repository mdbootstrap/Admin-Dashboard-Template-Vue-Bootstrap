<template>
  <section id="profile">
    <mdb-row>
      <mdb-col md="3">
        <mdb-card cascade narrow>
          <mdb-view>
            <img src="https://mdbootstrap.com/img/Photos/Horizontal/People/6-col/img%20%283%29.jpg" alt="Project" class="img-fluid"/>
            <mdb-mask overlay="white-slight" waves/>
          </mdb-view>
          <mdb-card-body class="text-center">
            <mdb-card-title class="font-bold mb-2">
              <strong>Alice Mayer</strong>
            </mdb-card-title>
            <h5 class="indigo-text">
              <strong>Photographer</strong>
            </h5>
            <h6 class="text-justify">
              <strong>About:</strong>
            </h6>
            <p class="text-justify">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ratione perferendis quod animi dignissimos consectetur quibusdam numquam laboriosam, minus, provident...</p>
            <div class="text-right">
              <mdb-btn outline="primary" rounded size="sm">More...</mdb-btn>
            </div>
          </mdb-card-body>
        </mdb-card>
      </mdb-col>
      <mdb-col md="9">
        <section class="text-center pb-3">
          <mdb-row class="d-flex justify-content-center">
            <mdb-col lg="6" xl="5" class="mb-3">
              <mdb-card cascade narrow class="d-flex mb-5">
                <mdb-view>
                  <img src="https://mdbootstrap.com/img/Mockups/Horizontal/6-col/pro-profile-page.jpg" alt="Project" class="img-fluid"/>
                  <mdb-mask overlay="white-slight" waves/>
                </mdb-view>
                <mdb-card-body>
                  <mdb-card-title class="font-bold mb-3">
                    <strong>Project name</strong>
                  </mdb-card-title>
                  <mdb-card-text>Some quick example text to build on the card title and make up the bulk of the card's content.</mdb-card-text>
                </mdb-card-body>
                <mdb-card-footer class="links-light profile-card-footer">
                  <span class="right">
                    <a class="p-2" href="#profile">
                      Live Preview
                      <mdb-icon icon="photo" class="ml-1"/>
                    </a>
                  </span>
                </mdb-card-footer>
              </mdb-card>
            </mdb-col>
            <mdb-col lg="6" xl="5" class="mb-3">
              <mdb-card cascade narrow class="d-flex mb-5">
                <mdb-view>
                  <img src="https://mdbootstrap.com/img/Mockups/Horizontal/6-col/pro-signup.jpg" alt="Project" class="img-fluid"/>
                  <mdb-mask overlay="white-slight" waves/>
                </mdb-view>
                <mdb-card-body>
                  <mdb-card-title class="font-bold mb-3">
                    <strong>Project name</strong>
                  </mdb-card-title>
                  <mdb-card-text>Some quick example text to build on the card title and make up the bulk of the card's content.</mdb-card-text>
                </mdb-card-body>
                <mdb-card-footer class="links-light profile-card-footer">
                  <span class="right">
                    <a class="p-2" href="#profile">
                      Live Preview
                      <mdb-icon icon="photo" class="ml-1"/>
                    </a>
                  </span>
                </mdb-card-footer>
              </mdb-card>
            </mdb-col>
          </mdb-row>
          <mdb-row class="d-flex justify-content-center">
            <mdb-col lg="6" xl="5" class="mb-3">
              <mdb-card cascade narrow class="d-flex mb-5">
                <mdb-view>
                  <img src="https://mdbootstrap.com/img/Mockups/Horizontal/6-col/pro-pricing.jpg" alt="Project" class="img-fluid"/>
                  <mask overlay="white-slight" waves/>
                </mdb-view>
                <mdb-card-body>
                  <mdb-card-title class="font-bold mb-3">
                    <strong>Project name</strong>
                  </mdb-card-title>
                  <mdb-card-text>Some quick example text to build on the card title and make up the bulk of the card's content.</mdb-card-text>
                </mdb-card-body>
                <mdb-card-footer class="links-light profile-card-footer">
                  <span class="right">
                    <a class="p-2" href="#profile">
                      Live Preview
                      <mdb-icon icon="photo" class="ml-1"/>
                    </a>
                  </span>
                </mdb-card-footer>
              </mdb-card>
            </mdb-col>
            <mdb-col lg="6" xl="5" class="mb-3">
              <mdb-card cascade narrow class="d-flex mb-5">
                <mdb-view>
                  <img src="https://mdbootstrap.com/img/Mockups/Horizontal/6-col/pro-landing.jpg" alt="Project" class="img-fluid"/>
                  <mask overlay="white-slight" waves/>
                </mdb-view>
                <mdb-card-body>
                  <mdb-card-title class="font-bold mb-3">
                    <strong>Project name</strong>
                  </mdb-card-title>
                  <mdb-card-text>Some quick example text to build on the card title and make up the bulk of the card's content.</mdb-card-text>
                </mdb-card-body>
                <mdb-card-footer class="links-light profile-card-footer">
                  <span class="right">
                    <a class="p-2" href="#profile">
                      Live Preview
                      <mdb-icon icon="photo" class="ml-1"/>
                    </a>
                  </span>
                </mdb-card-footer>
              </mdb-card>
            </mdb-col>
            <mdb-col lg="12">
              <div class="text-center">
                <mdb-pagination circle color="blue">
                  <mdb-page-item disabled>First</mdb-page-item>
                  <mdb-page-nav prev></mdb-page-nav>
                  <mdb-page-item active>1</mdb-page-item>
                  <mdb-page-item>2</mdb-page-item>
                  <mdb-page-item>3</mdb-page-item>
                  <mdb-page-item>4</mdb-page-item>
                  <mdb-page-item>5</mdb-page-item>
                  <mdb-page-nav next></mdb-page-nav>
                  <mdb-page-item disabled>Last</mdb-page-item>
                </mdb-pagination>
              </div>
            </mdb-col>
          </mdb-row>
        </section>
      </mdb-col>
    </mdb-row>
  </section>
</template>

<script>
import { mdbRow, mdbCol, mdbCard, mdbCardBody, mdbView, mdbMask, mdbCardTitle, mdbCardText, mdbCardFooter, mdbIcon, mdbBtn, mdbPagination, mdbPageNav, mdbPageItem } from 'mdbvue'

export default {
  name: 'Profile',
  components: {
    mdbRow,
    mdbCol,
    mdbCard,
    mdbCardBody,
    mdbView,
    mdbMask,
    mdbCardTitle,
    mdbCardText,
    mdbCardFooter,
    mdbIcon,
    mdbBtn,
    mdbPagination,
    mdbPageNav,
    mdbPageItem
  },
  data () {
    return {
    }
  }
}
</script>

<style scoped>
.profile-card-footer {
  background-color: #F7F7F7 !important;
  padding: 1.25rem;
}
.card.card-cascade .view {
  box-shadow: 0 3px 10px 0 rgba(0, 0, 0, 0.15), 0 3px 12px 0 rgba(0, 0, 0, 0.15);
}
</style>
