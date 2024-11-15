<html>
	<head><meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1"></head>
  <body>
    <script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
			window.addEventListener("onEmbeddedMessagingReady", () => {            
				console.log( "Inside Prechat API!!" );
				embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields( { "CustomerId" : "Test123" } );
			});
			embeddedservice_bootstrap.init(
				'00Daj00000FxKbb',
				'ESA_Web_Deployment',
				'https://daj00000fxkbbeaf-dev-ed.develop.my.site.com/ESWESAWebDeployment1724800920657',
				{
					scrt2URL: 'https://daj00000fxkbbeaf-dev-ed.develop.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://daj00000fxkbbeaf-dev-ed.develop.my.site.com/ESWESAWebDeployment1724800920657/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>

  </body>
</html>
