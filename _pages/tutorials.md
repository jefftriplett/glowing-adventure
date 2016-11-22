---
layout: page
title: Tutorials
permalink: /tutorials/
---

<div class="schedule">
    <h1 class="title">{{ page.title }}</h1>

    <p>You are viewing the demo for a <a href="http://github.com/fourkitchens/jekyll-schedule">Jekyll-powered event schedule</a>.</p>
    <p><a href="http://fourkitchens.com/blog/2013/07/10/jekyll-event-schedule">Read more about how it was built</a> or <a href="http://2013.drupalcampaustin.org/schedule/">see a finished, branded version</a>.</p>
    <p>Feel free to use it for your conference!</p>

    <section id="sunday" class="day">
        <header>
            <h2>Sunday</h2>
            <span data-room="room-1">Room 1</span>
            <span data-room="room-2">Room 2</span>
            <span data-room="room-3">Room 3</span>
        </header>

        {% for post in site.categories.tutorial reversed %}
            {% capture day %}{{ post.date | date: "%A" }}{% endcapture %}
            {% if day == 'Sunday' %}
                {% include schedule-day.html %}
            {% endif %}
        {% endfor %}
    </section>
</div>
<!-- .schedule -->
