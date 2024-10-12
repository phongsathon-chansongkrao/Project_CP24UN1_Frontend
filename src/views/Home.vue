<template>
    <Navbar class="nav"/>
    <div class="app">
        <div class="button-container">
            <button class="large-button">ใบคำร้องขอลากิจ/ลาป่วย</button>
            <button class="large-button">แบบขออนุมัติการจัดกิจกรรม</button>
        </div>
    </div>
</template>
  
<script>
import Navbar from '@/components/Navbar.vue';
  export default {
    name: 'Home',
    components: {
        Navbar
    },
  }
</script>

<style scoped>
.nav{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  height: 4vh;
  padding: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.app {
  /* margin-left: 50px; */
  margin-top: 60px;
  width: 100%;
  height: 80vh;
  background-color: #ffe5b4;
  display: flex;
  justify-content: center;
  align-items: center;
}

.button-container {
  display: flex;
  justify-content: space-between;
  width: 80%;
  max-width: 800px;
}

.large-button {
  font-family: 'Arial', sans-serif;
  width: 100%;
  padding: 2rem;
  font-size: 1.5rem;
  background-color: white; /* สีพื้นหลังของปุ่ม */
  color: black; /* สีฟอนต์ในปุ่ม */
  border: 4px solid #cc5200; /* สีขอบของปุ่ม */
  font-weight: bold;
  border-radius: 40px;
  cursor: pointer;
  transition: background-color 0.3s;
  margin: 20px;
}

.large-button:hover {
  background-color: #dfab89;
}
</style>
  