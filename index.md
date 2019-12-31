---
title: Home
---
<table class="schedule">
    <thead>
        <tr>
            <th>DATE</th>
            <th>TOPIC</th>
            <th>READING</th>
        </tr>
    </thead>
    <tbody>
		{% assign date_format = site.minima.date_format | default: "%a, %h %d" %}
        {% assign schedule = site.data.schedule %}
        {% for meeting in schedule %}
            <tr>
                <td>{{ meeting.date | date: "%a, %h %d" }}<br/>{{ meeting.meeting }}</td>
                <td>{{ meeting.topic | markdownify }}
                    {{ meeting.notes | markdownify }}</td>
                <td>{{ meeting.reading | markdownify }}</td>
            </tr>
        {% endfor %}

    </tbody>
</table>

Please refer to the [Syllabus](syllabus.html) for more details on the course, grading, schedule, etc.. This page is meant only as a summary and quick-reference.

## Reference Links

* [The Swift Programming Language](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/), 
[iBook version](https://itunes.apple.com/us/book/swift-programming-language/id881256329?mt=11)
* [Apple Developer Portal](http://developer.apple.com)
* [Android Developer Home](https://developer.android.com/)

<hr/>
