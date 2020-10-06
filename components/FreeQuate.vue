<template>
  <div class="freeQuate bgColorDark">
      <b-container fluid="sm">
        <div class="text-center hedlineContent pb-5">
          <h2>Send a Message</h2>
          <p>Interested in getting started?  Have a question?  We’re just an email away!</p>
        </div>
        <b-row class="justify-content-center no-gutters">
        <b-col md="10" lg="10">
          <div class="messageContent">
            <div class="input-group flex-nowrap mt-4">
              <div class="w-100">
                <div>
                    <h5> Name *</h5>
                    <b-form-input class="mb-3 inputStyle"  size="lg"></b-form-input>
                </div>
                <div>
                    <h5> Business Name</h5>
                    <b-form-input class="mb-3 inputStyle"  size="lg"></b-form-input>
                </div>
                <div>
                    <h5> Email Address *</h5>
                    <b-form-input class="mb-3 inputStyle"  size="lg"></b-form-input>
                </div>
                <div>
                    <h5> Phone</h5>
                    <b-form-input class="mb-3 inputStyle"  size="lg"></b-form-input>
                </div>
                <div>
                    <h5> Do you currently have a website? *</h5>
                    <b-form-select size="lg"
                    v-model="selected"
                    :options="options"
                    class="mb-3 inputStyle"
                    value-field="item"
                    text-field="name"
                    disabled-field="notEnabled"
                    ></b-form-select>
                </div>
                <div>
                    <h5> Link to current website (if applicable)</h5>
                    <b-form-input class="mb-3 inputStyle"  size="lg"></b-form-input>
                </div>
                <div>
                    <h5> Which services are you interested in?</h5>
                    <b-form-select size="lg"
                    v-model="selected2"
                    :options="options2"
                    class="mb-3 inputStyle"
                    value-field="item"
                    text-field="name"
                    disabled-field="notEnabled"
                    >
                     <template v-slot:first>
                        <b-form-select-option :value="null" disabled>-- Please select an Option --</b-form-select-option>
                    </template>
                    </b-form-select>
                </div>
                <div>
                    <h5>What else would you like us to know?</h5>
                    <b-form-textarea
                        id="textarea"
                        v-model="text"
                        placeholder="Enter something..."
                        rows="3 "
                        size="lg"
                        class="inputStyle mb-3"
                        ></b-form-textarea>

                </div>
              </div>
            </div>
            <b-button
              class="submitBtn"
              block
              squared
            >submit</b-button>
          </div>
        </b-col>
      </b-row>
      </b-container>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        selected: 'A',
        selected2: 'null',
        options: [
          { item: 'A', name: 'Yes' },
          { item: 'B', name: 'No' },
        ],
        options2: [
          { item: '1', name: ' Brand Development' },
          { item: '2', name: ' Website Design' },
          { item: '3', name: ' SEO' },
          { item: '4', name: ' Email/SMS Marketing' },
          { item: '5', name: ' Copywriting' },
          { item: '6', name: ' Social Media Management' },
          { item: '7', name: ' Website Maintenance' },
          { item: '8', name: ' Audience Analytics' },
        ]
      }
    }
  }
</script>

<style scoped>
.freeQuate {
  padding: 70px 0px;
}

.messageContent {
  background:white;
  padding: 8px 24px 24px 24px;
  height: 100%;
  box-shadow: 0 3px 12.35px 0.65px rgba(0, 0, 0, 0.1);
}
.inputStyle {
  border-radius: 0;
  color: black;
  /* border-color: black; */
}

.submitBtn{
  background: #056676;
  font-size: 1.25rem;
  padding: 0.6rem 1rem;
  border-color: #056676;
  text-transform: uppercase;
  font-weight: 500;
}

</style>