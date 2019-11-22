<template>
    <mdb-container>
    <mdb-icon icon="cogs" size="2x" class="indigo-text m-1" style="float:right;" @click.native="modal = true"/>
    <mdb-modal v-if="modal" @close="modal = false">
      <mdb-modal-header>
        <mdb-modal-title tag="h4" class="w-100 text-center font-weight-bold">Settings</mdb-modal-title>
      </mdb-modal-header>
      <mdb-modal-body>
        <form class="mx-3 gray-text">
          <mdb-row>
            <mdb-col col="6">
              <mdb-input 
                name="city"
                label="City"
                type="text"
                v-model="city"
              />
            </mdb-col>
            <mdb-col col="6">
              <div class="d-flex justify-content-center">
                <mdb-btn class="m-10" outline="primary">Locate</mdb-btn>
              </div>
            </mdb-col>
          </mdb-row>
          <b-form-radio v-model="temperature" name="setting-temp" value="Ctemp">Celsius</b-form-radio>
          <b-form-radio v-model="temperature" name="setting-temp" value="Btemp">Fahrenheit</b-form-radio>
        </form>
      </mdb-modal-body>
      <mdb-modal-footer>
      </mdb-modal-footer>
    </mdb-modal>
  </mdb-container>
</template>

<script>
import {
  mdbIcon,
  mdbModal,
  mdbContainer,
  mdbInput,
  mdbRow,
  mdbCol,
  mdbBtn,
  mdbModalHeader,
  mdbModalBody,
  mdbModalFooter,
  mdbModalTitle,
} from "mdbvue";
export default {
  name: "Settings",
  components: {
    mdbIcon,
    mdbContainer,
    mdbInput,
    mdbModal,
    mdbRow,
    mdbCol,
    mdbBtn,
    mdbModalBody,
    mdbModalHeader,
    mdbModalFooter,    
    mdbModalTitle,
  },
  data() {
    return{
      modal: false,
      temperature: "Ctemp",
      city: "Warsaw"
    }
  }
}
</script>

<style scoped>

</style>
