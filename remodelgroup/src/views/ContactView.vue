<template>
  <div class="container">
    <div class="image">
      <img v-bind:src="Banner_image" width="1300" height="450" />
    </div>
    <div class="flexclass">
      <div class="twoContent">
        <div>
          <div class="Silicon">{{ companyname }}</div>
          <h1 class="contact">Contact</h1>
        </div>
        <h2>ContactDetails</h2>
        <p>
          <strong>Company ABCD</strong>
          <br />{{ Address.address.door_no }}<br />Pincode :
          {{ Address.address.pincode }}<br />{{ Address.address.country }}
        </p>
        <p>{{ Address.address.telephone }}</p>
        <p>
          <a href="#">{{ relatedurls.url1 }}</a
          ><br />
          <a href="#">{{ relatedurls.url2 }}</a>
        </p>
      </div>

      <div class="threeContent">
        <h2>SEND EMAIL</h2>
        <div class="nameTag">Name</div>
        <input type="text" class="input" />
        <div class="nameTag">Email</div>
        <input type="text" class="input" />
        <div class="nameTag">Contact</div>
        <input type="text" class="input" />
        <div class="nameTag">Comment</div>
        <textarea
          id="w3review"
          name="w3review"
          rows="5"
          cols="40"
          class="textarea"
        ></textarea
        >
        <div class="buttonClass">
          <button type="button">Submit</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { Contacts } from "@/lib/staticData";
export default {
  name: "ContactView",
  data() {
    return {
      Banner_image: require("../assets/contact/contact_banner.jpg"),
      companyname: Contacts.contact_details[0].title,
      Address: Contacts.contact_details[0],
      relatedurls: Contacts.contact_details[0].relatedurls,
    };
  },
};
</script>
<style scoped>
.flexclass {
  padding-top: 40px;
  width: 100%;
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  margin: auto;
  width: 1300px;
  text-align: left;
}
.threeContent {
  margin-left: auto;
}
.Silicon {
  margin-top: 30px;
  font-weight: 600;
  color: rgb(22, 21, 21);
}
.contact {
  color: #101010;
  line-height: 42px;
  margin-bottom: 50px;
}
.twoContent h2 {
  font-size: 18px;
  font-weight: 700;
  color: #101010;
}
.twoContent p {
  line-height: 24px;
}
.input {
  padding: 10px 12px;
}
button {
  margin-top: 35px;
  color: brown;
  background-color: bisque;
  width: 100px;
  height: 35px;
  font-size: 18px;
}

.nameTag {
  font-size: 18px;
  font-weight: 700;
}
</style>
