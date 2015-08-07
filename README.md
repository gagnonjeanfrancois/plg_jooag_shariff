<h1>Joomla 3.4+ Shariff Plugin</h1>
<h3>The 1-Click-Social-Button with privacy in mind</h3>
This Joomla 3.4+ Plugin utilizes Heise Shariff Library to enable website users to share their favorite content without compromising their privacy.

<b>Required:</b>
PHP 5.4+ and Joomla 3.4+

<b>Plugin features:</b>
* Joomla Update integration
* Use this Plugins in your Modules and Articles via {shariff} shorttag
* Languages: English, German
* Restrict the plugin execution to Menu Items or Content Categories
* Ordering for your Buttons
* Extended Shariff Backend Cache Handler
* Plugin settings for Themes, Orientation, Services and much more...

<b>Shariff Library features:</b>
* Services: Twitter, Facebook, GooglePlus, LinkedIn, Pinterest, Xing, Whatsapp
* Themes: Color, Grey, White
* Orientation: Horizontal, Vertical
* Responsive: Yes
* Shariff Languages: bg, de, en, es, fi, hr, hu, ja, ko, no, pl, pt, ro, ru, sk, sl, sr, sv, tr, zh
* Counter: Shariff Backend PHP integration
 
<b>Future plans:</b>
* More languages maybe through contributors
* Integration for more Componentes
* Use the Shariff Backend OPP style instead of write a json File
* Move assets to Joomla Media Folder

<h2>Update Instructions:</h2>
* V3.0.6 -> V3.1.0
  * Everything fine. Nothing to do!
* Before V3.0.6
  * Plugin Settings need to be revisited. 
* Before V3.0.3
  * Delete this folder joomla-root/plugins/system/jooag_shariff/backend/cache
  * Not so important to delete this folder. It's not needed anymore, because we use the Joomla Core Cache folder.
* Before V3.0.0 Stable
  * Delete the old Plugin and install the new one

<h2>Documentation:</h2>
<h4>Share Counter:</h4>
It's really important for the counter to use the url only with www or non-www.
<h6>To redirect www to non-www do the following steps:</h6>
<ol>
<li>Rename the htaccess.txt in your joomla root folder to .htaccess</li>
<li>Add following lines in the end of the .htaccess file</li>
<pre>
# www to non-www
RewriteBase /
RewriteCond %{HTTP_HOST} ^www\.(.*)$ [NC]
RewriteRule ^(.*)$ http://%1/$1 [R=301,L]
</pre>
or
<pre>
# non-www to www
RewriteCond %{HTTP_HOST} !^www\.
RewriteRule ^(.*)$ http://www.%{HTTP_HOST}/$1 [R=301,L]
</pre>
<li>At least you need to open this plugin and save it again!</li>
</code>
</ol>
</p>

<h4>Use this Plugin as a Shariff Joomla Modul</h4>
You can put into your content or "Custom Html" module the following shortcode: <code>{shariff}</code> and set the Option "Prepare Content" to yes.

<h2>Credits:</h2>
Developed by http://joomla-agentur.de

Thanks to Heise.de for this development https://github.com/heiseonline/shariff

and for Joomla User Group Hamburg http://jug-hamburg.de/ (the main reason for this plugin :-)
