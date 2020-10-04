<template>
  <div class="container newsl_container">
    <h2>Subscribe to our newsletter</h2>
    <div class="form">
      <input
        type="email"
        name="text"
        value=""
        placeholder="Enter your email address"
        v-model="email"
      />
      <button @click="submitHandler">Subscribe</button>
    </div>
    <div class="error_label">
      <div>{{ error }}</div>
    </div>
    <div class="success_label">
      <div>{{ success }}</div>
    </div>
    <div class="small">
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt eius
        distinctio excepturi reprehenderit nisi quasi quaerat odit voluptatibus
        eligendi fugiat!
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "newsletter",
  data() {
    return {
      email: "",
      error: "",
      success: "",
    };
  },
  methods: {
    //Test - Validate the input (email address)
    validate(email) {
      let re = /\S+@\S+\.\S+/;
      let valid = [true, ""];

      if (!re.test(email)) {
        valid = [false, "Enter a valid email"];
      }

      if (email === "") {
        valid = [false, "It's empty"];
      }

      return valid;
    },
    submitHandler() {
      let valid = this.validate(this.email);
      if (valid[0]) {
        this.error = "";
        // submit email to the database
        this.addEmail(this.email);
      } else {
        this.error = valid[1];
      }
    },
    // Add rule on firebase to enable Get request
    // Post email processor
    addEmail() {
      // Make a GetRequest for email address here
      this.$http
        .get(`users.json?orderBy="email"&&equalTo="${this.email}"`)
        .then((response) => {
          if (Object.getOwnPropertyNames(response.data).length === 0) {
            // Make a PostRequest for email address here
            this.$http
              .post("users.json", { email: this.email })
              // eslint-disable-next-line no-unused-vars
              .then((response) => {
                this.success =
                  "Thank you, successfully added user to the list...";
              });
          } else {
            this.success = "Already exist";
          }
          //   console.log(response);
        });
      this.clearSuccess();
    },
    clearSuccess() {
      setTimeout(() => {
        this.email = "";
        this.success = "";
      }, 3000);
    },
  },
};
</script>

<style scoped></style>
