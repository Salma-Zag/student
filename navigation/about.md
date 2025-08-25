---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

My Favorite Things

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid



    var living_in_the_world = [
        {"flag": "/images/Pics/albion.jpg", "greeting": "Purple", "description": "Favorite color;"},
        {"flag": "/images/Pics/Flag_of_Colorado.png", "greeting": "Colorado", "description": "Where I was born;"},
        {"flag": "/images/Pics/albion.jpg", "greeting": "For Albion SC", "description": "I'm a soccer player;"},
        {"flag": "/images/Pics/nerd.jpg", "greeting": "I love things like Marvel and chess", "description": "I'm a big geek;"},
];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### My journey through Life

Here is what I did at those places

- Born in Colorado, it wasn't long before my family set off and moved to Virginia.
- Living on the east coast, I started playing soccer in Kindergarten.
- Though, only a couple years later my family moved counties within Virginia. I switched both schools and soccer clubs.
- I was living my best life in Loudoun County Virginia before Covid hit- Online school was miserable for me.
- As soon as the pandemic had subsided, my dad landed within the state and we had to switch counties again. It was always tough for me to adjust, but you learn.
- I spent 5th and 6th grade in a county called Ashburn, making even more close friends. They were really starting to add up, and I even got to visit the ones I had moved away from.
-When I had finally began to accept the situation I was in, my family decided to move again. But this time, across the country, to the west coast. To California.
-It was one of the scariest experiences I had ever gone through, but here I am now. After so many adventures throughout the past two years, I'm excited to continue pursuing my education.

### More facts about me

Here are some more random things about me!

- I'm a dog person
- I have always wanted to go to Singapore or Tokyo.
- I'm an Android user (Yes, they're better.)
- I love playing video games.
- I love art and drawing.
- I hate pineapple on pizza.
- Listening to music is one of my favourite hobbies.

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/missionary.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/john_tamara.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/tamara_fam.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/surf.jpg" alt="Image 4">
  <img src="{{site.baseurl}}/images/about/john_lora.jpg" alt="Image 5">
  <img src="{{site.baseurl}}/images/about/lora_fam.jpg" alt="Image 6">
  <img src="{{site.baseurl}}/images/about/lora_fam2.jpg" alt="Image 7">
  <img src="{{site.baseurl}}/images/about/pj_party.jpg" alt="Image 8">
  <img src="{{site.baseurl}}/images/about/trent_family.png" alt="Image 9">
  <img src="{{site.baseurl}}/images/about/claire.jpg" alt="Image 10">
  <img src="{{site.baseurl}}/images/about/grandkids.jpg" alt="Image 11">
  <img src="{{site.baseurl}}/images/about/farm.jpg" alt="Image 12">
</div>
