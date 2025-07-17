---
layout: about
title: IDA Lab
permalink: /
subtitle: <b>Interdisciplinary Data and Artificial Intelligence Lab</b><br><a href='https://joinville.ufsc.br/'>Joinville Technological Center</a> - <a href='https://ufsc.br'>UFSC</a>.

#profile:
#  align: right
#  image: prof_pic.jpg
#  image_circular: false # crops the image to make it circular
#  more_info: >
#    <p>555 your office number</p>
#    <p>123 your address street</p>
#    <p>Your City, State 12345</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: false # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---


<style>
.news-carousel-container {
  position: relative;
  overflow: hidden;
  margin-bottom: 2rem;
  border-radius: 1rem;
  box-shadow: 0 0 0px rgba(0,0,0,0.05);
  background-color: var(--bg);
  color: var(--fg);
}

.carousel-track {
  display: flex;
  transition: transform 2.0s ease;
}

.carousel-slide {
  min-width: 100%;
  box-sizing: border-box;
  padding: 1rem;
  display: flex;
  gap: 1rem;
  align-items: center;
  background-color: inherit;
  color: inherit;
  text-decoration: none;
}

.carousel-slide:hover {
  background-color: rgba(0, 0, 0, 0.03);
}

.carousel-slide img {
  max-width: 220px;
  max-height: 150px;
  width: auto;
  height: auto;
  object-fit: contain;
  border-radius: 8px;
  flex-shrink: 0;
  box-shadow: 0 0 6px rgba(0,0,0,0.05);
}

.carousel-slide .text {
  flex: 1;
  overflow: hidden;
}

.carousel-slide h3 {
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.carousel-slide p {
  font-size: 1rem;
  color: var(--text-muted);
  margin-bottom: 0.2rem;
}

.carousel-nav {
  position: absolute;
  bottom: 0.75rem;
  right: 0.75rem;
  display: flex;
  gap: 0.5rem;
  z-index: 2;
}

.carousel-button {
  background: rgba(0, 0, 0, 0.1);
  color: #444;
  font-size: 1.2rem;
  border: none;
  padding: 0.4rem 0.6rem;
  border-radius: 6px;
  cursor: pointer;
  transition: background 0.2s ease, color 0.2s ease;
}

.carousel-button:hover {
  background: rgba(0, 0, 0, 0.2);
  color: #000;
}
</style>

<div class="news-carousel-container">
  <div class="carousel-track">
    {% assign news_limit = page.announcements.limit | default: 5 %}
    {% assign news_items = site.news | sort: "date" | reverse | slice: 0, news_limit %}
    {% for item in news_items %}
      {% assign tag = "a" %}
      {% if item.inline %}
        {% assign tag = "div" %}
      {% endif %}

      <{{ tag }}
        {% unless item.inline %}
          href="{{ item.url | relative_url }}"
        {% endunless %}
        class="carousel-slide"
        {% if item.inline %}style="cursor: default;"{% endif %}
      >
        {% if item.image %}
          <img src="{{ item.image | relative_url }}" alt="{{ item.headline }}">
          <div class="text">
            <h3>{{ item.headline | newline_to_br }}</h3>
            <p>{{ item.summary }}</p>
            <p><em>{{ item.date | date: "%B %d, %Y" }}</em></p>
            {% unless item.inline %}
              <p style="font-size: 0.85rem; color: var(--text-muted); margin-top: 0.4rem;"><em>Click to read more →</em></p>
            {% endunless %}
          </div>
        {% else %}
          <div class="text" style="margin-left: 0;">
            <h3>{{ item.headline | newline_to_br }}</h3>
            <p><em>{{ item.date | date: "%B %d, %Y" }}</em></p>
            {% unless item.inline %}
              <p style="font-size: 0.85rem; color: var(--text-muted); margin-top: 0.4rem; text-align: right"><em>Click to read more →</em></p>
            {% endunless %}
          </div>
        {% endif %}
      </{{ tag }}>
    {% endfor %}
  </div>

  <div class="carousel-nav">
    <button class="carousel-button" onclick="carouselPrev()">&#10094;</button>
    <button class="carousel-button" onclick="carouselNext()">&#10095;</button>
  </div>
</div>



<script>
let index = 0;
function updateCarousel() {
  const track = document.querySelector('.carousel-track');
  const width = document.querySelector('.carousel-slide').offsetWidth;
  track.style.transform = `translateX(-${index * width}px)`;
}
function carouselNext() {
  const slides = document.querySelectorAll('.carousel-slide');
  index = (index + 1) % slides.length;
  updateCarousel();
}
function carouselPrev() {
  const slides = document.querySelectorAll('.carousel-slide');
  index = (index - 1 + slides.length) % slides.length;
  updateCarousel();
}
window.addEventListener('resize', updateCarousel);
window.addEventListener('load', updateCarousel);

setInterval(carouselNext, 8000); // auto-advance every 5 seconds
</script>


{: style="font-size: 1.2rem; text-align: justify;" }

The _Interdisciplinary Data and Artificial Intelligence Lab_ (IDA Lab) was established in 2025. It focuses on advancing the state of the art in machine learning, data science, and artificial intelligence through interdisciplinary research and collaboration. Situated within a leading technological center, the lab tackles complex real-world problems by developing innovative AI-driven solutions across multiple domains.

