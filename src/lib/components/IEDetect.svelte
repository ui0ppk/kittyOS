<noscript>
  <meta http-equiv="refresh" content="0; url=/njs/">
</noscript>	
<svelte:head>
  <script>
    function detectIE() {
      var ua = window.navigator.userAgent;

      var msie = ua.indexOf('MSIE ');
      if (msie > 0) {
        // IE 10 or older => return version number
        return parseInt(ua.substring(msie + 5, ua.indexOf('.', msie)), 10);
      }

      var trident = ua.indexOf('Trident/');
      if (trident > 0) {
        // IE 11 => return version number
        var rv = ua.indexOf('rv:');
        return parseInt(ua.substring(rv + 3, ua.indexOf('.', rv)), 10);
      }

      // other browser
      return false;
    }
  
    if(detectIE()) {
      window.location.href = "/njs";
    }
  </script>
</svelte:head>