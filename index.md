<html>
	<head><meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1"></head>
  <body>
    <script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
			
			embeddedservice_bootstrap.init(
    '00Daj00000FxKbb',
    'ESA_Web_Deployment',
    'https://daj00000fxkbbeaf-dev-ed.develop.my.site.com/ESWESAWebDeployment1724800920657',
    {
        scrt2URL: 'https://daj00000fxkbbeaf-dev-ed.develop.my.salesforce-scrt.com',
        onMessageReceived: function(message) {
	console.log('hiiii');
            // Vérifiez si le message contient une balise <a>
            if (message.text && message.text.includes('<a href=')) {
                // Remplacez ou injectez le contenu HTML dans le DOM
                var container = document.querySelector('.embedded-chat-container'); // Adaptez ce sélecteur
                var link = document.createElement('a');
                link.href = message.text.match(/href="([^"]+)"/)[1]; // Extraction du lien
                link.target = '_blank';
                link.innerText = message.text.match(/>([^<]+)<\/a>/)[1]; // Extraction du texte du lien
                container.appendChild(link);
            } else {
                // Si le message ne contient pas de lien, vous l'affichez normalement
                var messageElement = document.createElement('p');
                messageElement.innerHTML = message.text;
                container.appendChild(messageElement);
            }
        }
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
