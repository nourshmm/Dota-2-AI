# Dota-2-AI
Ce projet est un script Dota2 Bot basé sur les scripts LUA fourni par le jeux. 
Tout le code avait été écrit sous forme d’actions prédéfinies pour tous les bots. La complexité de Dota a rendu de plus en plus difficile de séparer les actions à entreprendre et le moment. Faut-il se battre dans ce cas, ou s’enfuir ? Lors de la modification des comportements du script, il est devenu impossible de séparer proprement quand il effectuerait des actions. Ils étaient si étroitement liés que l’ajustement de l’un affecterait les performances de l’autre, et aucun des comportements ne fonctionnait particulièrement bien. Nous n’avons pas non plus été en mesure d’inclure davantage de comportements sans perturber d’autres parties du code. En se basant sur l’état du jeu, nous avons pu séparer chaque comportement, en utilisant des moyennes pondérées pour décider lequel serait le plus optimal dans n’importe quelle instance du jeu. Le code du bot est exécuté à chaque trame, permettant des calculs constants et donnant à chaque comportement une valeur en tant que poids. On s’est inspiré par d’autres exemples de code qui utilisent la même logique, nous avons pu séparer chaque comportement en son propre code distinct, divisé en composants et conditions. Les composants sont des informations qui sont toujours nécessaires pour calculer un comportement, tandis que les conditions ne s’ajouteraient ou ne soustrairaient du poids que dans des circonstances spécifiques. La séparation du code nous a permis d’améliorer chaque comportement - auparavant, chaque comportement dépendait d’un autre, mais en utilisant l’état du jeu, nous n’exécutions que les parties du code dont nous avions besoin et seulement quand nous en avions besoin. L’un des avantages de se baser sur l’état du jeu était la modularité du système.
