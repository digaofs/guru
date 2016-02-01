var app = angular.module('8ball', ['ionic'])

app.run(function ($ionicPlatform) {
	$ionicPlatform.ready(function () {
		// Hide the accessory bar by default (remove this to show the accessory bar above the keyboard
		// for form inputs)
		if (window.cordova && window.cordova.plugins.Keyboard) {
			cordova.plugins.Keyboard.hideKeyboardAccessoryBar(true);
		}
		if (window.StatusBar) {
			StatusBar.styleDefault();
		}
	});
});


app.controller('PredictionController', function ($scope, $timeout) {

	var predictionList = [
		"Parece que sim",
		"Sim",
		"Tente de novo",
		"Sem dúvida",
		"Minhas fontes dizem não",
		"Ao que me parece, sim",
		"Pode apostar nisso!",
		"Concentre-se e pergunte novamente",
		"Nada bom, nada bom",
		"Certamente",
		"Melhor não te contar agora",
		"Não sei não",
		"Sim - definitivamente",
		"Claro!",
		"Não consigo ver agora",
		"Provável",
		"Pergunte mais tarde",
		"Não, a resposta é não",
		"Booom",
		"Não conte com isso"
	];

	$scope.prediction = "Clique na bola para ter sua resposta";
	
	$scope.answered = true;
	
	$scope.ask = function(){
		$scope.answered = false;
		$scope.prediction = "Consultando o oráculo";
		$timeout(function(){
			$scope.prediction = predictionList[Math.floor(Math.random() * predictionList.length)]
			$scope.answered = true;
		} , 2000);
		
	};
	
});
