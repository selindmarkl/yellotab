yellotab
========

### Metod 2 Framset redirect
 Hur du genom att lägga en ram kan visa en annan sida på din domän. 
 

     
    <!DOCTYPE HTML>  
    <html>
     <head>
     <title> Yellotab.se </TITLE>
    </head>
       <frameset cols ="100%,*" border="0" framespacing="0">
       <frame src=" http://yellotab.com">
       </frameset>
    <body>
     <noframes>
       <a href=" http://yellotab.com "> http://yellotab.com </a>
      </noframes>
      </body>
      </html>

### Metod 2 http redirect
Skickar iväg dig till den adress som anges genom url, efter antal sekuder som anges som content

    <meta http-equiv="refresh" content="0; url=http://example.com/"> 




###Metod 3 server Javascript
Use of meta refresh is discouraged by the World Wide Web Consortium (W3C). Ref: en.wikipedia.org/wiki/Meta_refresh. So it is reccomended to use server redirect instead. JavaScript redirects may not work on all the mobile phones as JavaScript might be disabled.
I would use both meta, and javascript, and have a link just in case. Also, I think it is a good idea to set the meta rate to 1 for occasional circumstances where the browser ignores 0 value meta refresh.

    <!DOCTYPE HTML>
      <html lang="en-US">
      <head>
        <meta charset="UTF-8">
        <meta http-equiv="refresh" content="1;url=http://example.com">
        <script type="text/javascript">
            window.location.href = "http://example.com"
        </script>
        <title>Page Redirection</title>
      </head>
      <body>
        <!-- Note: don't tell people to `click` the link, just tell them that it is a link. -->
        If you are not redirected automatically, follow the <a href='http://example.com'>link to example</a>
      </body>
    </html>
