# docker-matomo

1.Tracking code for birdrecoveries
<p>
To track your web traffic with Matomo you need to make sure some extra code is added to each of your webpages.
<p>
In most websites, blogs, CMS, etc. you can use a pre-made plugin to do the technical work for you. (See our list of plugins used to integrate Matomo.) If no plugin exists you can edit your website templates and add the JavaScript tracking code to the </head> tag which is often defined in a 'header.php', 'header.tpl' or similar template file.
JavaScript Tracking Code
<p>
Make sure this code is on every page of your website. We recommend pasting it immediately before the closing </head> tag.
<p>
  
```
<!-- Matomo -->
<script type="text/javascript">
  var _paq = window._paq || [];
  /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
  _paq.push(['trackPageView']);
  _paq.push(['enableLinkTracking']);
  (function() {
    var u="//172.31.0.2/";
    _paq.push(['setTrackerUrl', u+'matomo.php']);
    _paq.push(['setSiteId', '1']);
    var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
    g.type='text/javascript'; g.async=true; g.defer=true; g.src=u+'matomo.js'; s.parentNode.insertBefore(g,s);
  })();
</script>
<!-- End Matomo Code -->
```

# Warning when installing

```
Warning: You are now accessing Matomo from http://127.0.0.1:8080/index.php, but Matomo has been configured to run at this address: http://127.0.0.1/index.php.

Click here to access Matomo safely and remove this warning. You may also want to contact your Matomo administrator and notify them about this issue ().

How do I fix this problem and how do I login again?
The Matomo Super User can manually edit the file piwik/config/config.ini.php and add the following lines:

[General]
trusted_hosts[] = "127.0.0.1:8080"

After making the change, you will be able to login again.

You may also disable this security feature (not recommended). To do so edit config/config.ini.php and add:

[General]
enable_trusted_host_check=0

```
