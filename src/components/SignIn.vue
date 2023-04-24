<template>
  <div>
    <b-button v-b-modal.modal-prevent-closing modal-xl variant></b-button>

    <div class="mt-3">
      <div v-if="submittedNames.length === 0">-</div>
      <ul v-else class="mb-0 pl-3">
        <li  :key="name" v-for="name in submittedNames">{{ name }}</li>
      </ul>
    </div>

    <b-modal
      :no-close-on-esc='true'
      :cancel-disabled='true'
      :no-close-on-backdrop='true'
      :hide-header="true"
      :hide-header-close='true'
      id="modal-prevent-closing"
      ref="modal"
      title="Submit Your Name"
      @show="resetModal"
      @hidden="resetModal"
      @ok="handleOk"
    >
      <form ref="form" @submit.stop.prevent="handleSubmit">
        <b-form-group
          label="Name"
          label-for="name-input"
          invalid-feedback="Name is required"
        >
          <b-form-input
            placeholder="NFT"
            id="name-input"
            v-model="name"
            required
          ></b-form-input>
        </b-form-group>
      </form>
    </b-modal>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        name: '',
        user: '',
        submittedNames: []
      }
    },
    methods: {
      checkFormValidity() {
        const valid = this.$refs.form.checkValidity()
        this.nameState = valid
        return valid
      },
      resetModal() {
        this.name = ''
        this.nameState = null
      },
      handleOk(bvModalEvent) {
        // Prevent modal from closing
        bvModalEvent.preventDefault()
        // Trigger submit handler
        this.handleSubmit()
      },
      handleSubmit() {
        // Exit when the form isn't valid
        if (this.name === '1234123121') {
          console.log('ok')
          this.$nextTick(() => {
          this.$bvModal.hide('modal-prevent-closing')
        })

          return
        }
        console.log('fik')
      },
      showModal() {
        this.$bvModal.show('modal-prevent-closing')
      }
    },
    mounted() {
      this.showModal()
    },
  }
</script>