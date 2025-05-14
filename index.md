<html>
	<head><meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1"></head>
  <body>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'fr'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DAU000008ECCo',
				'Agent_Web_Deployment',
				'https://euryale--chatbot.sandbox.my.site.com/ESWAgentWebDeployment1734949607268',
				{
					scrt2URL: 'https://euryale--chatbot.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://euryale--chatbot.sandbox.my.site.com/ESWAgentWebDeployment1734949607268/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>


  </body>
</html>
