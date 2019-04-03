<template>
    <div class="main">
        <h1 class="title">{{ title }}</h1>
        <form @submit.prevent="submitForm" class="form">
            <div>
            <label for="name">Име:</label><br>
            <input id="name" type="text" v-model="name" required/>
            </div>
            <div>
            <label for="email">Email:</label><br>
            <input id="email" type="email" v-model="email" required/>
            </div>
            <div>
            <label for="caps">Съобщение:</label><br>
            <textarea id="caps" v-model="caps" required></textarea>
            </div>
            <button :class="[name ? activeClass : '']" type="submit">Изпрати</button>
            
        </form>
        <div class="map">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d184.88632399517704!2d24.747716829550797!3d42.
        146409487643865!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14acd1a90b212041%3A0x568acea8e94ec600!2z0LHR
        g9C7LiDigJ7QpdGA0LjRgdGC0L4g0JHQvtGC0LXQsuKAnCA5MSwgNDAwMCBLYW1lbml0c2EgMSwgUGxvdmRpdg!5e0!3m2!1sen!2sbg!4v1554308114078!5m2!1sen!2sbg"
         width="100%" height="400"  frameborder="0" style="border:0" allowfullscreen></iframe>

        </div>
        
    </div>    
</template>

<script>
export default {
    data(){
        return {
            title: 'Свържете се с мен',
            userID: 1,
            name: '',
            email: '',
            caps: '',
            response: '',
            activeClass: 'active'
        }
    }
}
</script>

<style lang="scss" scoped>
$primary: #5968d7;

#app {
  display: flex;
  justify-content: center;
  font-family: 'Work Sans', sans-serif;
}

form {
  width: 300px;
  padding: 10px 40px;
  label {
    text-transform: uppercase;
    font-size: 13px;
    letter-spacing: 0.03em;
    font-weight: bold;
  }
  input, textarea {
    border: 1px solid #ccc;
    color: #333;
    width: calc(100% - 30px);
  }
  input, textarea, button {
    border-radius: 4px;
    padding: 8px 15px;
    font-family: 'Work Sans', sans-serif;
    font-weight: 300;
  }
  div {
    margin: 20px 0;
  }
}

button {
  color: white;
  border: none;
  width: 100%;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  background: #ccc;
  cursor: pointer;
  box-shadow: 0px 2px 3px rgba(0, 0, 0, 0.3);
  transition: 0.25s all ease;
  &:hover {
    transform: translateY(2px);
  }
}

.active {
  background: $primary;
}

pre-content {
  width: 300px;
}
.map{
  width: 55%;
  float: right;
  margin-top: 40px;

}
.form{
  width: 40%;
  float: left;
  margin-top: 40px;

}
.main{
      display: inline; 

}
.title{
  text-align: center
}
</style>
