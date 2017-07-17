<!DOCTYPE html>
<html lang="en">
{% include _meta.html %}
  <body class="<%= current.source %> regular">
    {% include _google_tag_manager.html %}
    {% include _header.html %}

    <div class="page-wrapper">
      <div class="container">
         <div class="row">
            <div class="content documentation col-md-7">
              {{content}}
            </div>

            <div class="doc-sidebar col-md-4 col-md-offset-1">
              <h3>Popular Topics</h3>
              <ul id="popular-topics">
                <li><a href="/docs/postman/launching_postman/installation_and_updates">Installing the native app</a></li>
                <li><a href="/docs/postman/collection_runs/command_line_integration_with_newman">Newman - Running collections in the command line</a></li>
                <li><a href="/docs/pro/what_is_pro">Level up with Postman Pro</a></li>
                <li><a href="/docs/postman/collections/creating_collections">Getting started with collections</a></li>
                <li><a href="/docs/postman/environments_and_globals/variables">Setting up an environment with variables</a></li>
                <li><a href="/docs/postman/scripts/test_scripts">Writing tests</a></li>
              </ul>

              <h3>Video Tutorials</h3>
              <ul class="pm-video-list">
                {% for vid in site.data.video_tutorials %}
                <li>
                  <a href="https://www.youtube.com/watch?v={{vid.id}}&list=PLM-7VG-sgbtCJYpjQfmLCcJZ6Yd74oytQ&autoplay=1" target="_blank">{{vid.title}}</a>
                  <a class="pm-yt-thumbnail" href="https://www.youtube.com/watch?v={{vid.id}}&list=PLM-7VG-sgbtCJYpjQfmLCcJZ6Yd74oytQ&autoplay=1" target="_blank">
                    <img src="https://img.youtube.com/vi/{{vid.id}}/mqdefault.jpg">
                  </a>
                </li>
                {% endfor %}
                <li><a href="https://www.youtube.com/playlist?list=PLM-7VG-sgbtCJYpjQfmLCcJZ6Yd74oytQ">Watch Tutorial Playlist</a></li>
              </ul>
            </div>
          </div>
      </div>
    </div>

    {% include _footer.html %}
    {% include _navigation.html %}
    {% include _footer_scripts.html %}
    <!-- <script type="text/javascript" src="{{site.pm.root}}/js/swiftype.pm.js?v={{site.time | date: '%s%N'}}"></script> -->
    <script src="https://cdn.jsdelivr.net/algoliasearch/3/algoliasearch.min.js"></script>
  </body>
</html>
