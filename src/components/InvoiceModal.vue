<template>
  <div class="invoice-wrap flex flex-column" @click="checkClick" ref="invoiceWrap">
      <form @submit.prevent="subminForm" class="invoice-content">
          <h1>New Invoice</h1>

          <!-- Bill From -->
          <div class="bill-from flex flex-column">
              <h4>Bill From</h4>
              <div class="input flex flex-column">
                  <label for="billerStreetAddress">Street Address</label>
                  <input type="text" required id="billerStreetAddress" v-model="billerStreetAddress">
              </div>
              <div class="location-details flex">
                <div class="input flex flex-column">
                  <label for="billerCity">City</label>
                  <input type="text" required id="billerStreetAddress" v-model="billerStreetAddress">
                </div>
                <div class="input flex flex-column">
                  <label for="billerZipCode">Zip Code</label>
                  <input type="text" required id="billerZipCode" v-model="billerStreetAddress">
                </div>
                <div class="input flex flex-column">
                  <label for="billerCountry">Country</label>
                  <input type="text" required id="billerCountry" v-model="billerStreetAddress">
                </div>
              </div>
          </div>

          <!-- Bill To -->
            <div class="bill-to flex flex-column">
                <h4>Bill To</h4>
                
            </div>
      </form>
  </div>
</template>

<script>
export default {
    name: "InvoiceModal",
    data() {
        return {
            dateOptions: { year: "numeric", month: "short", day: "numeric" },
            docId: null,
            loading: null,
            billerStreetAddress: null,
            billerCity: null,
            billerZipCode: null,
            billerCountry: null,
            clientName: null,
            clientEmail: null,
            clientStreetAddress: null,
            clientCity: null,
            clientZipCode: null,
            clientCountry: null,
            invoiceDateUnix: null,
            invoiceDate: null,
            paymentTerms: null,
            paymentDueDateUnix: null,
            paymentDueDate: null,
            productDescription: null,
            invoicePending: null,
            invoiceDraft: null,
            invoiceItemList: [],
            invoiceTotal: 0,
        }
    }
}
</script>

<style>

</style>