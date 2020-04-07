<template>
  <div>
    <h1>Profile</h1>
    <CRow>
      <div id="circle"></div>
      <Ccol class="aline-center">
        <h1>Name:</h1>
        <strong>User ID:</strong>
      </Ccol>
    </CRow>
    <CRow>
      <CCol sm="4">
        <CInput v-model="name" label="Name" />
      </CCol>
      <CCol sm="4">
        <CInput v-model="surname" label="Surname" />
      </CCol>
      <CCol sm="2">
        <CSelect v-model="gender" label="Gender" :options="['Male','Famale']" />
      </CCol>
    </CRow>
    <CRow>
      <CCol style="margin-left:15px" sm="1.5">
        <CSelect
          v-model="birthday"
          placeholder="DD"
          label="Birthday"
          :options="[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31]"
        />
      </CCol>

      <CCol style="margin-left:15px" sm="1.5">
        <CSelect
          v-model="MM"
          style="color:white"
          placeholder="MM"
          label="."
          :options="[1,2,3,4,5,6,7,8,9,10,11,12]"
        />
      </CCol>
      <CCol style="margin-left:15px" sm="1.5">
        <CSelect
          v-model="YYYY"
          style="color:white"
          placeholder="YYYY"
          label="."
          :options="[1997,1998]"
        />
      </CCol>
      <CCol sm="2" style="margin-left:90px">
        <p>Age</p>
        <p>00</p>
      </CCol>
      <CCol sm="4">
        <CInput v-model="phoneNumber" label="Phone number" />
      </CCol>
    </CRow>
    <CRow>
      <CCol sm="8">
        <CSelect v-model="country" placeholder=" " label="Country" :options="['Thai']" />
      </CCol>
    </CRow>
    <CRow>
      <CCol sm="4">
        <CInput v-model="zipcode" label="Zipcode" />
      </CCol>
      <CCol sm="4">
        <CSelect v-model="provinceState" placeholder=" " label="Province/State" :options="['Test']" />
      </CCol>
    </CRow>
    <cRow>
      <CCol sm="4">
        <CSelect v-model="district" placeholder=" " label="District" :options="['Test']" />
      </CCol>
      <CCol sm="4">
        <CSelect v-model="subDistrict" placeholder=" " label="Sub-District" :options="['Test']" />
      </CCol>
    </cRow>
    <cRow>
      <CCol sm="8">
        <CInput v-model="address" label="Address" placeholder />
      </CCol>
    </cRow>
    <cRow>
      <CCol sm="8">
        <CSelect v-model="occupation" placeholder=" " label="Occupation" :options="['Student']" />
      </CCol>
    </cRow>
    <cRow>
      <CCol sm="4">
        <CInput v-model="university" label="University" placeholder />
      </CCol>
      <CCol sm="4">
        <CSelect v-model="facultySchool" placeholder=" " label="Faculty/School" :options="['test']" />
      </CCol>
    </cRow>
    <cRow>
      <CCol sm="8">
        <CInput v-model="major" label="Major" placeholder />
      </CCol>
    </cRow>
    <cRow>
      <CCol>
        <Button class="facebookButton">Facebook</Button>
      </CCol>
    </cRow>
    <cRow>
      <CCol>
        <Button class="googleButton">Google</Button>
      </CCol>
    </cRow>
    <cRow>
      <CCol>
        <div style="text-align: right;">
          <Button @click="this.onRegister" class="updateButton">Update</Button>
          <Button class="cancelButton">Cancel</Button>
        </div>
      </CCol>
    </cRow>
  </div>
</template>

<script>
export default {
  name: "Form",

  userInfo() {
    return {
      name: "",
      surname: "",
      gender: "",
      phoneNumber: "",
      country: "",
      zipcode: "",
      provinceState: "",
      district: "",
      subDistrict: "",
      address: "",
      occupation: "",
      university: "",
      facultySchool: "",
      major: "",
      birthday:"",
      MM:"",
      YYYY:""

    };
  },
  methods: {
    onRegister() {
      var data = {};
      data.name = this.name;
      data.surname = this.surname;
      data.gender = this.gender;
      data.phoneNumber = this.phoneNumber;
      data.country = this.country;
      data.zipcode = this.zipcode;
      data.provinceState = this.provinceState;
      data.subDistrict = this.subDistrict;
      data.address = this.address;
      data.occupation = this.occupation;
      data.university = this.university;
      data.facultySchool = this.facultySchool;
      data.major = this.major;
      data.district = this.district;
       data.birthday = this.birthday;
        data.MM = this.MM;
         data.YYYY = this.YYYY;

      console.log(data);
    }
  }
};
</script>
<style scoped>
#circle {
  width: 140px;
  height: 140px;
  background: white;

  -webkit-border-radius: 70px;
  border-radius: 70px;
  border: black;
  border-style: solid;
  border-width: medium;
}
.aline-center {
  margin-left: 110px;
}
.facebookButton {
  background-color: white;
  color: #182ff4;
  border: 2px solid #182ff4;
  height: 35px;
  width: 200px;
}
.googleButton {
  background-color: white;
  color: orange;
  border: 2px solid red;
  height: 35px;
  width: 200px;
  margin-top: 20px;
}
.updateButton {
  background-color: rgb(37, 145, 172);
  border-radius: 8px;
  color: white;
  height: 35px;
}
.cancelButton {
  background-color: rgba(140, 142, 145, 0.993);
  border-radius: 8px;
  color: white;
  height: 35px;
  margin-left: 10px;
}
</style>



