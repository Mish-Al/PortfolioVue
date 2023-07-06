<template>
  <div>
    <div
      class="animate__animated animate__animated animate__zoomIn animate__delay-1s 1s"
    >
      <h1 class="mt-2">Contact</h1>
    </div>
  </div>

  <br />
  <div class="container">
    <div class="row">
      <div class="col">
        <div
          class="form animate__animated animate__animated animate__fadeInDown animate__delay-2s 2s"
        >
          <form
            class="p-5"
            action="https://formspree.io/f/xqkonyvj"
            method="POST"
          >
            <div>
              <label for="exampleFormControlInput1" class="form-label"
                >First Name
              </label>
              <input
                name="firstname"
                type="text"
                class="form-control"
                id="exampleFormControlInput1"
                required
              />
            </div>
            <div>
              <label for="exampleFormControlInput1" class="form-label"
                >Surname</label
              >
              <input
                name="surname"
                type="text"
                class="form-control"
                id="exampleFormControlInput1"
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
                required
              />
            </div>
            <label for="exampleFormControlTextarea1" class="form-label"
              >Comment or Message</label
            >
            <textarea
              name="message"
              class="form-control text-center"
              id="exampleFormControlTextarea1"
              rows="4"
            ></textarea>
            <br />
            <div class="middle d-flex justify-content-center">
              <button type="submit" class="btn">Submit</button>
              <button type="reset" class="btn">Clear</button>
            </div>
          </form>
          <div class="details pb-5">
          <h2>Contact Details</h2>
          <h4 class="phone"><i class="bi bi-telephone"></i>Phone : +27 65 859 9211</h4>
          <h4 class="mail"><i class="bi bi-envelope-at"></i>mtaliep.lifechoices@gmail.com</h4>
          <h4 class="place"><i class="bi bi-envelope-at"></i>Address : 310 Imam Haron Road, Lansdowne Cape Town 7780</h4>
        </div>
      </div>
        </div>
      </div>
    </div>
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
.btn:hover {
  background-color: #62b6cb;
  color: #1b4965;
  border: 1px solid #bee9e8;
}
.container {
  text-align: center;
}
.form {
  background-color: #1b4965;
  color: #62b6cb;
  border-radius: 20px;
  margin-bottom: 1rem;
  box-shadow: 0 6px 10px rgba(119, 34, 34, 0.08), 0 0 6px rgba(0, 0, 0, 0.05);
  transition: 0.3s transform cubic-bezier(0.155, 1.105, 0.295, 1.12),
    0.3s box-shadow,
    0.3s -webkit-transform cubic-bezier(0.155, 1.105, 0.295, 1.12);
  cursor: pointer;
}
.form:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12), 0 4px 8px rgba(0, 0, 0, 0.06);
}
.details {
  border-radius: 20px;
  margin-bottom: 1rem;
  box-shadow: 0 6px 10px rgba(119, 34, 34, 0.08), 0 0 6px rgba(0, 0, 0, 0.05);
  transition: 0.3s transform cubic-bezier(0.155, 1.105, 0.295, 1.12),
    0.3s box-shadow;
}
.details:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12), 0 4px 8px rgba(0, 0, 0, 0.06);
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
@media screen and (max-width: 500) {
  .details {
    display: grid;
    justify-content: last baseline;
  }
  .conform {
    display: grid;
    justify-content: first baseline;
  }
}


</style>