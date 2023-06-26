<template>
  <div>
<h1>Home</h1>
<div id="content"></div>

<Footer/>
  </div>
</template>

<script>
import Footer from '../components/Footer';
        export default{
            components:{
                  Footer
            },};

      async function getNames(){
      const data = await fetch('https://laiquah.github.io/jsonserver/server.json')
      const formatData = await data.json()

     let fetchingdata = formatData.students

      const display = document.querySelector('#content')
      fetchingdata.forEach(students =>{
      display.innerHTML += `
      <div class="card">
          <div class="card-body">
            <h3 class="card-title">${students.first_name} ${students.last_name}</h3>
            <p class="card-text">${students.email}</p>
          </div>
        </div>
    `
  })
  }
    getNames()






</script>

<style scoped>

</style>