<template>
    <div class="login-container">
      <div class="login-box">
        <h1>K-MUTTRACK</h1>
        <form @submit.prevent="handleLogin">
          <div class="input-group">
            <label for="username">Username</label>
            <input
              type="text"
              id="username"
              v-model="username"
              required
            />
          </div>
  
          <div class="input-group">
            <label for="password">Password</label>
            <input
              type="password"
              id="password"
              v-model="password"
              required
            />
          </div>
  
          <button type="submit" class="login-button">Login</button>
          <p><router-link to="/signup">Sign Up</router-link></p>
        </form>
      </div>
    </div>
</template>
  
<script>
  export default {
    name: 'Login'
  }
</script>

<style scoped>
html, body, #app {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background-color: #ffe5b4;
  overflow: hidden;
}

.login-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #ffe5b4;
}

.login-box {
  background-color: #fff;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  width: 100%; 
  max-width: 400px; 
  font-family: 'Arial', sans-serif;
}

h1 {
  color: #ff6600;
  margin-bottom: 2rem;
}

.input-group {
  display: flex;
  align-items: center;
  margin-bottom: 25px;
}

label {
  width: 100px;
  text-align: right;
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

.login-button {
  width: 100px;
  padding: 0.75rem;
  background-color: #ff6600;
  color: white;
  border: none;
  border-radius: 25px;
  font-size: 1.2rem;
  cursor: pointer;
}

.login-button:hover {
  background-color: #e65c00;
} 
</style>