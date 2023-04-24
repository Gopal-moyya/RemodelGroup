<template>
  <div class="container">
    <div class="wrapper">
      <div class="Banner">
        <div class="Image">
          <img v-bind:src="Banner_image" width="1510" height="496" />
        </div>
      </div>
      <div class="flexclass">
        <div class="contacttwo">
          <div class="twoContent">
            <div>
              <div class="Silicon">{{ companyname }}</div>
              <h1 class="contact">CONTACT</h1>
            </div>
            <h2>ContactDetails</h2>
            <p>
              <strong>Company ABCD</strong>
              <br />{{Address.address.door_no}}<br />Pincode : {{Address.address.pincode }}<br />{{Address.address.country}}
            </p>
            <p>{{Address.address.telephone}}</p>
            <p>
              <a href="#">{{relatedurls.url1}}</a><br />
              <a href="#">{{relatedurls.url2}}</a>
            </p>
          </div>
        </div>
        <div class="contactthree">
          <div class="threeContent">
            <h3>SEND EMAIL</h3>
            <h4 class="name">name</h4>
            <input type="text" class="input" />
            <h4 class="name">Email</h4>
            <input type="text" class="input" />
            <h4 class="name">contact</h4>
            <input type="text" class="input" />
            <h4 class="comment">comment</h4>
            <textarea
              id="w3review"
              name="w3review"
              rows="10"
              cols="40"
              class="textarea"
            ></textarea><br><br>
            <button type="button">Submit</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script >
import { Contacts } from "@/lib/staticData";
export default {
  name: "ContactView",
  data() {
    return {
      Banner_image: require("../assets/contact/contact_banner.jpg"),
      companyname: Contacts.contact_details[0].title,
      Address: Contacts.contact_details[0],
      relatedurls:Contacts.contact_details[0].relatedurls
    };
  },
};
</script>
<style scoped>
.container {
  width: 100%;
  display: flex;
  text-align: center;
  justify-content: center;
}
.textarea{
  margin-left: 100px;
}
.wrapper {
  width: 80%;
  display: flex;
  flex-direction: column;
}

.input {
  padding: 10px 12px;
}

.Banner {
  width: 100%;
  display: flex;
}
button{
  color: brown;
  background-color: bisque;
  margin-left: 120px;
}


.Silicon {
  margin-top: 50px;
  font-weight: 600;
  color: #999;
}
.name{
  margin-left: -150px;
}
.comment{
   margin-left: -130px;
}

.flexclass {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.contact {
  color: #00c858;
  line-height: 42px;
  margin-bottom: 50px;
}

.contacttwo {
  width: 50%;
  display: flex;
}

.twoContent {
  margin-left: 300px;
}

.twoContent h2 {
  font-size: 18px;
  font-weight: 700;
  color: #00c858;
}

.twoContent p {
  line-height: 24px;
}

.contactthree {
  width: 50%;
  display: flex;
}

.threeContent {
  margin-top: 150px;
}
</style>
