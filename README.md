# CSS
in this i am learning CSS concept like flexbox, grid(image gallery), css animation, overflow. all these concepts with bootstrap

Home.js
   import React from 'react'
   import './Home.css';
   function Home() {
  return (
    <div className="container">
      <img src="/images/img1.jpg" alt="Sample photo" />
      <img src="/images/img2.jpg" alt="Sample photo" />
      <img src="/images/img3.jpg" alt="Sample photo" />
      <img src="/images/img4.jpg" alt="Sample photo" />
      <img src="/images/img5.jpg" alt="Sample photo" />
    </div>
     );
    }
export default Home

Note- iske css me maine simply display:grid kar diya aur 3 rows liya equally 1-1-1 fr ke aur same isi tarah 3 columns liya 1-1-1 fr ka. aur image 1 ko maine 1st column me rakha hai so mai simply 1/2 karunga kyuki ye lines ginta hai humne 3 rows banaya hai means isme 1,2,3,4 lines hongi aur same columns ke liye maine 3 columns banaya hai means 1,2,3,4 lines isme bhi honge. so mai chahta hu ki jo img1 hai wo first column me aaye so mai simply  grid-column:1/2 karunga iska matlab ki line1 aur line2 tak rahega ye aur mai chahta hu ki ye image two rows tak fail jaye to mai grid-rows:1/3 means rows line1 se line3 tak chala jayega. same chiz hum sabhi images ke liye karenge

Home.css
    .container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    gap: 10px; /* Adjust the gap as needed */
    width:80%;
    height:60%;
  }
  
  .container img {
    width: 100%;
    height: 100%;
    object-fit: cover; /* Ensure the images cover their grid area */
  }
  
  /* Specific grid areas for each image */
  img:nth-child(1) {
    grid-column: 1 / 2;
    grid-row: 1 / 3;
  }
  
  img:nth-child(2) {
    grid-column: 2 / 4;
    grid-row: 1 / 2;
  }
  
  img:nth-child(3) {
    grid-column: 2 / 3;
    grid-row: 2 / 3;
  }
  
  img:nth-child(4) {
    grid-column: 1 / 3;
    grid-row: 3 / 4;
  }
  
  img:nth-child(5) {
    grid-column: 3 / 4;
    grid-row: 2 / 4;
  }
  
