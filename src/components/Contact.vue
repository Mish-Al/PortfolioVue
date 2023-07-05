<template>
  <div>
    <div class="animate__animated details animate__animated animate__zoomIn">
      <h1>Contact</h1>
      <h4>Get in touch with me!</h4>
    </div>
  </div>
  <form class="p-5" action="https://formspree.io/f/xqkonyvj" method="POST">
    <div>
      <label for="exampleFormControlInput1" class="form-label"
        >First Name
      </label>
      <input
        name="firstname"
        type="text"
        class="form-control"
        id="exampleFormControlInput1"
        placeholder="Input First Name"
        required
      />
    </div>
    <div>
      <label for="exampleFormControlInput1" class="form-label">Surname</label>
      <input
        name="surname"
        type="text"
        class="form-control"
        id="exampleFormControlInput1"
        placeholder="Input Surname"
        required
      />
    </div>
    <div>
      <label for="exampleFormControlInput1" class="form-label"
        >Email Address</label
      >
      <input
        name="email"
        type="email"
        class="form-control"
        id="exampleFormControlInput1"
        placeholder="Input Email Address"
        required
      />
    </div>
    <label for="exampleFormControlTextarea1" class="form-label"
      >Comment or Message</label
    >
    <textarea
      name="message"
      class="form-control"
      id="exampleFormControlTextarea1"
      placeholder="Type a message here..."
      rows="4"
    ></textarea>
    <br />
    <div class="middle d-flex justify-content-center">
      <button type="submit" class="btn">Submit</button>
    </div>
  </form>
</template>

<script>
export default {};
</script>

<style scoped>
.btn {
  text-decoration: none;
  color: grey;
  background-color: #bee9e8;
  border: #bee9e8;
  border-radius: 5px;
  height: 3rem;
  margin: 1rem;
}

#exampleFormControlInput1 {
  text-align: center;
}

h1 {
  text-decoration: underline;
  color: #cae9ff;
}
h4 {
  color: #cae9ff;
}
</style>