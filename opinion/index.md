---
layout: home
---

<div class="index-content opinion">
    <div class="section">
        <ul class="artical-cate">
            <li><a href="/"><span>Blog</span></a></li>
            <li class="on" style="text-align:center"><a href="/opinion"><span>Opinion</span></a></li>
            <li style="text-align:right"><a href="/project"><span>Project</span></a></li>
        </ul>

        <div class="cate-bar"><span id="cateBar"></span></div>

        <ul class="artical-list">
        <li>
            <div class="table-article">
                <div class="col-title">
                    <h2><a href="/Conferences">Coming Conferences and Activities</a></h2>
                </div>
                <div class="col-date">
                    <p class="entry-date">2016-05-09</p>
                </div>
            </div>
            <div class="title-desc">主要整理安全，人工智能，软件工程方向的会议及相关活动</div>
        </li>
        {% for post in site.categories.opinion %}
            {% if {{post.title}} !='Coming Conferences and Activities' %}
            <li>
                <div class="table-article">
                    <div class="col-title">
                        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
                    </div>
                    <div class="col-date">
                        <p class="entry-date">{{ post.date|date:"%Y-%m-%d" }}</p>
                    </div>
                </div>
                <div class="title-desc">{{ post.description }}</div>
            </li>
            {% endif %}
        {% endfor %}
        </ul>


    </div>
    <div class="aside">
    </div>
</div>
