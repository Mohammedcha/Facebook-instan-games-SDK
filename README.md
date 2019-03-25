# Facebook-instan-games-SDK
Learn how to integrate games built with JavaScript and HTML5 with Facebook instant games SDK

<strong>1.</strong> You need to start creating your game client. The game client needs to have an <code>index.html</code> file in the root directory. Start by importing the Instant Games SDK by adding this line in the head of your game before the <code></ head></code> Tag.

<pre>
<script src="https://connect.facebook.net/en_US/fbinstant.6.2.js"></script>
</pre>


<strong>2.</strong> Start loading game assets by adding this <code>Script</code> in the body of your game after the <code>< body></code> Tag.

<pre>
<script>
  FBInstant.initializeAsync().then(function() {
    FBInstant.setLoadingProgress(100);
  });
  FBInstant.startGameAsync().then(function() {
    game.start();
  })
</script>
</pre>

<strong>3.</strong> You need to create a new file named <code>fbapp-config.json</code> and place the following code in it

<pre>
{
  "instant_games": {
    "orientation": "PORTRAIT", 
    "navigation_menu_version": "NAV_FLOATING"
  }
}
</pre>

The <code>fbapp-config.json</code> file should be saved in the main folder of the game <strong>(the same folder that contains index.html)</strong>

You can now compress the whole folder in <code>zip</code> format and upload it to Facebook.
