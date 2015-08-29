.. _oembed:

oEmbed
------

Example
+++++++

From https://github.com/guardian/alerta/blob/master/examples/oembed.html

.. code:: html

  <!DOCTYPE html>
  <html lang="en">
  <head>
    <link rel="stylesheet" href="//netdna.bootstrapcdn.com/bootstrap/3.0.0/css/bootstrap.min.css" />
    <link href='http://fonts.googleapis.com/css?family=Sintony:700' rel='stylesheet' type='text/css'>
  </head>
  <body>

  <div class="mobile-alerts">Loading...</div>

  <script src="//ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
  <script src="//netdna.bootstrapcdn.com/bootstrap/3.3.2/js/bootstrap.min.js"></script>
  <script src="http://api.alerta.io/embed.js"></script>
  <script>
  $(function() {

    // $.alerta.defaults.endpoint = 'http://localhost:8080';
    // $.alerta.defaults.key = 'demo-key';
    // or
    $.alerta.defaults = {
        endpoint: 'http://api.alerta.io', // oEmbed endpoint becomes http://api.alerta.io/oembed.json
        key: 'demo-key'
    };

    $('.mobile-alerts').alerta('http://api.alerta.io/alerts/count?service=Mobile&status=open', {title:'Mobile Service'});

  });
  </script>
  </body>
  </html>

HEAD, OPTIONS, GET  /embed.js  embed_js
HEAD, OPTIONS, GET  /oembed.json  oembed

