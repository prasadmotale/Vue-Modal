<template>
    <form>
        <div class="container">
        <input type="text" placeholder="Name" name="name" required>

        <input type="email" placeholder="Email" name="email" required>
            
        <input type="text" placeholder="Contact Number" name="phone_num" required>
        <br>
        <label>
        <input type="checkbox" checked="checked" name="remember"> May we contact you?
        </label>
  </div>
    </form>
</template>

<script>
export default {
    
}
</script>
<style scoped>
.container{
    margin: auto;
    padding: 10px;
}
 input[type=text], input[type=email] {
  width: 80%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  box-sizing: border-box;
  border: none;
  outline: none;
  border-bottom: 1px solid #B1B1B1;
}
input:focus {
  outline: none;
  opacity: 1;
}
button {
  background-color: #4CAF50;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  cursor: pointer;
  width: 100%;
}

button:hover {
  opacity: 0.8;
}

</style>