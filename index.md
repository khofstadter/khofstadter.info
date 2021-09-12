---
title: tEdör aka Krisztián Hofstädter
layout: default
---

Hello! My name is Krisztián Hofstädter, aka tEdör. I am a creative technologist working as a researcher, lecturer, freelancer and artist. This website informs you about my work. My cv is [here](https://khofstadter.com/assets/doc/KHofstader-CV.pdf).

<div class="tab">
  organised
  
  <button class="tablinks" onclick="openCity(event, 'categories')">by main theme</button>
  or 
  <button class="tablinks" onclick="openCity(event, 'time')" id="defaultOpen" >chronologically</button> 
  
  <!--
  or 
  <button class="tablinks" onclick="openCity(event, 'tags')">by tags</button>
  -->
  
</div>

<div id="time" class="tabcontent">
  <h3>ongoing</h3>
  {% include index-cron-ongoing.html %}
  <h3>past</h3>
  {% include index-cron.html %}
</div>

<div id="categories" class="tabcontent">
  {% include index-cat.html %}
</div>


<br>

Contact me on kris[at]khofstadter[dot]com.

<br>

<script>
function openCity(evt, cityName) {
    var i, tabcontent, tablinks;
    tabcontent = document.getElementsByClassName("tabcontent");
    for (i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
    }
    tablinks = document.getElementsByClassName("tablinks");
    for (i = 0; i < tablinks.length; i++) {
        tablinks[i].className = tablinks[i].className.replace(" active", "");
    }
    document.getElementById(cityName).style.display = "block";
    evt.currentTarget.className += " active";
}

// Get the element with id="defaultOpen" and click on it
document.getElementById("defaultOpen").click();
</script>
