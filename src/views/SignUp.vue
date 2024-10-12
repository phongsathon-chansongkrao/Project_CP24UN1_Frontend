<template>
    <div class="signup-container">
        <div class="signup-box">
            <h1>Sign Up</h1>
            <form @submit.prevent="handleSignup">
            <div class="name-surname-group">
                <div id="input-th-name" class="input-group">
                    <label for="name">ชื่อ</label>
                    <input
                    type="text"
                    id="th-name"
                    v-model="thname"
                    required
                    />
                </div>
                <div id="input-th-surname" class="input-group">
                    <label for="name">นามสกุล</label>
                    <input
                    type="text"
                    id="th-surname"
                    v-model="thsurname"
                    required
                    />
                </div>
            </div>

            <div class="name-surname-group">
                <div id="input-eng-name" class="input-group">
                    <label for="name">Firstname</label>
                    <input
                    type="text"
                    id="eng-name"
                    v-model="engname"
                    required
                    />
                </div>
                <div id="input-eng-surname" class="input-group">
                    <label for="name">Lastname</label>
                    <input
                    type="text"
                    id="eng-surname"
                    v-model="engsurname"
                    required
                    />
                </div>
            </div>

            <div class="input-group">
                <div class="input-group">
                    <label for="year">ระดับการศึกษา</label>
                    <select id="year" v-model="selectedYear">
                        <option value="" disabled>กรุณาเลือก</option>
                        <option v-for="year in years" :key="year" :value="year">{{ year }}</option>
                    </select>
                </div>    

                <div id="input-email" class="input-group">
                <label for="name">Email สำรอง</label>
                <input
                    type="text"
                    id="eng-surname"
                    v-model="engsurname"
                    required
                    />
                </div>    
            </div>

            <div class="input-group">
                <div class="input-group">
                    <label for="faculty">คณะ</label>
                    <select id="faculty" v-model="selectedfaculty">
                        <option value="" disabled>กรุณาเลือก</option>
                        <option v-for="faculty in faculties" :key="faculty" :value="faculty">{{ faculty }}</option>
                    </select>
                </div>    

                <div class="input-group">
                    <label for="department">ภาควิชา/สาขาวิชา</label>
                    <select id="department" v-model="selecteddepartment">
                        <option value="" disabled>กรุณาเลือก</option>
                        <option v-for="department in departments" :key="department" :value="department">{{ department }}</option>
                    </select>
                </div>       
            </div>

            <div id="input-username" class="input-group">
                <label for="username">Username</label>
                <input
                type="text"
                id="username"
                v-model="username"
                required
                />
            </div>
            <div id="input-passwd" class="input-group">
                <label for="password">Password</label>
                <input
                type="password"
                id="password"
                v-model="password"
                required
                />
            </div>

            <div id="input-cfpassw" class="input-group">
                <label for="password">Confirm Password</label>
                <input
                type="password"
                id="confirm-password"
                v-model="password"
                required
                />
            </div>
            <button type="submit" class="signup-button">Sign Up</button>
            <p><router-link to="/login">Back to login page</router-link></p>
            </form>
        </div>
    </div>
</template>
  
<script>
  export default {
    name: 'SignUp',
    data() {
    return {
      selectedYear: '', // เก็บค่าที่เลือกจาก dropdown
      years: ['ปริญญาตรี ปี1', 'ปริญญาตรี ปี2', 'ปริญญาตรี ปี3', 'ปริญญาตรี ปี4'], // ตัวเลือกใน dropdown
      selectedFaculty: '', // เก็บค่าคณะที่เลือก
      faculties: [
        'คณะวิศวกรรมศาสตร์',
        'คณะวิทยาศาสตร์',
        'คณะครุศาสตร์อุตสาหกรรมและเทคโนโลยี',
        'คณะเทคโนโลยีสารสนเทศ',
        'คณะสถาปัตยกรรมศาสตร์และการออกแบบ',
        'คณะพลังงานสิ่งแวดล้อมและวัสดุ',
        'คณะทรัพยากรชีวภาพและเทคโนโลยี',
        'คณะศิลปศาสตร์'
      ],  
    };}
  }
</script>

<style scoped>
.name-surname-group {
  display: flex;
  justify-content: space-between;
  gap: 20px; /* เพิ่มช่องว่างระหว่างช่องชื่อและนามสกุล */
}
.input-group {
    flex: 1;
  display: flex;
  align-items: center;
  margin-bottom: 25px;
}
select {
  width: 70%;
  padding: 0.75rem;
  border: 1px solid #ddd;
  border-radius: 25px;
  font-size: 1rem;
}
label {
  width: 80px; /* ปรับขนาด label ให้พอดีกับพื้นที่ */
  text-align: left;
  margin-right: 10px;
  color: black;
}

input {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid #ddd;
  border-radius: 25px;
  font-size: 1rem;
}
/* label {
  width: 100px;
  text-align: left;
  margin-right: 30px;
  color: black;
}
input {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid #ddd;
  border-radius: 25px;
  font-size: 1rem;
} */
.signup-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #ffe5b4;
}
.signup-box {
  background-color: #fff;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  width: 700px; 
  font-family: 'Arial', sans-serif;
}
h1{
    color: #ff6600;
}
.signup-button {
  width: 100px;
  padding: 0.75rem;
  background-color: #ff6600;
  color: white;
  border: none;
  border-radius: 25px;
  font-size: 1.2rem;
  cursor: pointer;
}

.signup-button:hover {
  background-color: #e65c00;
} 
</style>
  