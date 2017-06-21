---
title: Home
description: If we lived here you'd be home by now.
image: /whitebalanced-klaus-voormann-sketch-of-john.jpg
social: yes
---

## Welcome

John Dylan is a DIY-core musician from San Francisco.

<script type="text/javascript" src="http://johndylanaudio.tumblr.com/api/read/json"></script>
<script language="javascript">
$(document).ready(function(){
  var output = new Array();
  var postLimit = (tumblr_api_read['posts'].length > 25) ? 25 : tumblr_api_read['posts'].length;
  for(i=0;i<postLimit;i++){
    var doFooter=false;
    output.push('<h4><a href="' + tumblr_api_read['posts'][i]['url-with-slug'] + '">' + tumblr_api_read['posts'][i]['date'] + '</a></h4>');
    if (tumblr_api_read['posts'][i]["type"]=="video")
    {
      // video post
      if (tumblr_api_read['posts'][i]['video-caption'].indexOf("blockquote") < 0)
      {
        output.push(tumblr_api_read['posts'][i]['video-player']);
        output.push(tumblr_api_read['posts'][i]['video-caption']);
        doFooter=true;
      }
    }
    else if (tumblr_api_read['posts'][i]["type"]=="photo")
    {
      // photo post
      if (tumblr_api_read['posts'][i]['photo-caption'].indexOf("blockquote") < 0)
      {
        output.push('<h3><a href="' + tumblr_api_read['posts'][i]['url-with-slug'] + '">' + tumblr_api_read['posts'][i]['photo-caption'].replace("<p>","").replace("</p>","") + '</a></h3>');
        output.push('<a href="' + tumblr_api_read['posts'][i]['url-with-slug'] + '"><img src="' + tumblr_api_read['posts'][i]['photo-url-400'] + '" border="0"></a>');
        doFooter=true;
      }
    }
    else if (tumblr_api_read['posts'][i]["type"]=="audio")
    {
      // audio post
      if (tumblr_api_read['posts'][i]['audio-caption'].indexOf("blockquote") < 0)
      {
        output.push(tumblr_api_read['posts'][i]['audio-player']);
        doFooter=true;
      }
    }
    else if (tumblr_api_read['posts'][i]["type"]=="link")
    {
      // audio post
      if (tumblr_api_read['posts'][i]['link-text'].indexOf("blockquote") < 0)
      {
        output.push("<a href=" + tumblr_api_read['posts'][i]['link-url'] + ">" + tumblr_api_read['posts'][i]['link-text'] + "</a>");
        output.push(tumblr_api_read['posts'][i]['link-description']);
        doFooter=true;
      }
    }
    else
    {
      // te post
      if (tumblr_api_read['posts'][i]['regular-body'].indexOf("blockquote")<0)
      {
        output.push('<h3><a href="' + tumblr_api_read['posts'][i]['url-with-slug'] + '">' + tumblr_api_read['posts'][i]['regular-title'] + '</a></h3>');
        output.push(tumblr_api_read['posts'][i]['regular-body']);
        doFooter=true;
      }
    }
    if (doFooter)
    {
      output.push('<p style="font-size: 12px">Posted to <a href="http://johndylanaudio.tumblr.com">johndylanaudio.tumblr.com</a> | <a href="http://www.tumblr.com/follow/johndylanaudio">Follow</a> | <a href="https://www.tumblr.com/reblog/' + tumblr_api_read['posts'][i]['id'] + '/' + tumblr_api_read['posts'][i]['reblog-key'] + '?redirect_to=%2Fblog%2Fjohndylanaudio">Reblog</a> | <a href="https://johndylanaudio.tumblr.com/submit">Submit Post</a></p>')
    }
  }
  $("#blogdiv").html(output.join("\n"));
});
</script>
<div id="blogdiv"></div>
