---
layout: page
title: Talks
permalink: /talks/
---

<!-- .schedule -->
<div class="schedule">

    <p>You are viewing the demo for a <a href="http://github.com/fourkitchens/jekyll-schedule">Jekyll-powered event schedule</a>.</p>
    <p><a href="http://fourkitchens.com/blog/2013/07/10/jekyll-event-schedule">Read more about how it was built</a> or <a href="http://2013.drupalcampaustin.org/schedule/">see a finished, branded version</a>.</p>
    <p>Feel free to use it for your conference!</p>

    <section id="monday" class="day">
        <header>
            <h2>Monday</h2>
            <span data-room="room-1">Room 1</span>
            <span data-room="room-2">Room 2</span>
        </header>

        {% for post in site.categories.talk reversed %}
            {% capture day %}{{ post.date | date: "%A" }}{% endcapture %}
            {% if day == 'Monday' %}
                {% include talks-schedule-day.html %}
            {% endif %}
        {% endfor %}
    </section>

    <hr>

    <section id="tuesday" class="day">
        <header>
            <h2>Tuesday</h2>
            <span data-room="room-1">Room 1</span>
            <span data-room="room-2">Room 2</span>
        </header>

        {% for post in site.categories.talk reversed %}
            {% capture day %}{{ post.date | date: "%A" }}{% endcapture %}
            {% if day == 'Tuesday' %}
                {% include talks-schedule-day.html %}
            {% endif %}
        {% endfor %}
    </section>

    <hr>

    <section id="wednesday" class="day">
        <header>
            <h2>Wednesday</h2>
            <span data-room="room-1">Room 1</span>
            <span data-room="room-2">Room 2</span>
        </header>

        {% for post in site.categories.talk reversed %}
            {% capture day %}{{ post.date | date: "%A" }}{% endcapture %}
            {% if day == 'Wednesday' %}
                {% include talks-schedule-day.html %}
            {% endif %}
        {% endfor %}
    </section>
</div>
<!-- .schedule -->
