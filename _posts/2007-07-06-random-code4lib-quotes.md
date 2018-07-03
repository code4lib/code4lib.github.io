---
excerpt: "<script type=\"text/javascript\">\r\n\r\nvar Quotes = function(){\r\n\r\n
  \   if (typeof console == 'undefined')\r\n        window.console = { log: function()
  {}, trace: function() {} };\r\n\r\n\r\n    function _injectjQuery(callback)\r\n
  \   {\r\n        console.log(\"loading jQuery\");\r\n        var script = document.createElement('script');\r\n
  \       script.src = 'http://code4lib.org/js/jquery.js';\r\n        script.type
  = 'text/javascript';\r\n        script.defer = 'defer';\r\n\r\n        document.getElementsByTagName('head').item(0).appendChild(script);\r\n\r\n
  \       var poll = window.setInterval(function() {\r\n            if (typeof window.$
  == 'function') {\r"
categories:
- irc
layout: post
title: 'Random #code4lib Quotes'
created: 1183754076
---
<script type="text/javascript">

var Quotes = function(){

    if (typeof console == 'undefined')
        window.console = { log: function() {}, trace: function() {} };


    function _injectjQuery(callback)
    {
        console.log("loading jQuery");
        var script = document.createElement('script');
        script.src = 'http://code4lib.org/js/jquery.js';
        script.type = 'text/javascript';
        script.defer = 'defer';

        document.getElementsByTagName('head').item(0).appendChild(script);

        var poll = window.setInterval(function() {
            if (typeof window.$ == 'function') {
                window.clearInterval(poll);
                if (callback) callback();
            }
        }, 100);
    }

    function _showQuotes(data)
    {
        var quotes = $.grep(data.split("\n"), function(n,i)
        {
            return n.indexOf(',') != -1;
        });

        $("#irc-quotes").empty();

        $.each([0,1,2,3,4], function()
        {
            var qindex = Math.floor(Math.random() * quotes.length);
            var q = quotes[qindex].match(/^(\d+):(\d+)[\d\.,'"]+(.*)/);
            var quote = q[3].replace(/['"]+$/g, '');
            quote = quote.replace(/</g, '&lt;').replace(/>/g, '&gt;');
            var qnum = q[1];
            var qdate = new Date(new Number(q[2]));

            var qDiv = $("<blockquote><div>Quote #" + new Number(qnum) + "</div>'" + quote + "'<span>" + qdate.toUTCString() + "</span></blockquote>");

            $("#irc-quotes").append(qDiv);
        });
    }

    function _fetchQuotes() {
        $.get("/quotes.txt", _showQuotes);
    }

    return { init: function() { _injectjQuery(_fetchQuotes) } };

}();

Quotes.init();

</script>
<style type="text/css">
#irc-quotes blockquote {
    padding: 10px;
    font-style: normal;
    margin: auto;
}

#irc-quotes blockquote div {
    font-size: 1.2em;
    font-weight: bold;
}

#irc-quotes blockquote span {
    font-style: italic;
    display: block;
    text-align: right;
}

#irc-quotes { 
    font-family: verdana,arial;
    padding-bottom: 20px; 
}

</style>

<div id="irc-quotes">
</div>
