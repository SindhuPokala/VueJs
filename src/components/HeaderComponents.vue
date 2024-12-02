<template>
  <header>
   <img class="logo" src="@/assets/logo-travel.png" alt="Travel company logo">


    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Blogs</a></li>
        <li><a href="#">Best Places</a></li>
        <li><a href="#">About</a></li> 
        <li><a href="#">Quick Links</a></li>
      </ul>
    </nav>

    <button class="book-now-button">Book Now</button>
  </header>
</template>

<script>
export default {
  name: "HeaderComponents",  // Ensure this matches the file name
};
</script>

<style>
header {
  display: grid;
  grid-template-columns: auto 1fr auto; /* Three columns for logo, navigation, and button */
  gap: 20px; /* Space between elements */
  align-items: center; /* Vertically align items in the center */
  background-color: #f4f4f4;
  padding: 10px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

/* Logo styling */
.logo {
  height: 50px; /* Adjust logo size */
  width: auto; /* Maintain aspect ratio */
  margin-left:20px;
}

/* Navigation menu styling */
nav ul {
  display: flex; /* Align navigation links horizontally */
  justify-content: center; /* Center the links horizontally */
  margin: 0;
  padding: 0;
  list-style: none;
}

nav ul li {
  margin: 0 10px; /* Space between list items */
}

nav ul li a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
  padding: 5px 10px; /* Add padding to the links */
}

nav ul li a:hover {
  color: #007bff;
}

/* Book Now button styling */
.book-now-button {
  background-color: skyblue;
  border-radius: 20px;
  padding: 10px 20px;
  font-weight: bold;
  border: none;
  cursor: pointer;
}

.book-now-button:hover {
  background-color: #007bff;
  color: white;
}

@media only screen and (max-width: 676px) {
  header{
    display: flex;
    flex-wrap: wrap;
  }
}



</style>
