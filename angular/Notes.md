#formation angularjs

Code Hoisting: se fait dans la phase d'optim du moteur JS

Ligne déclarative = var , function sont hoisté, c'est à dire placé en haut dans la scope par le moteur d'optim JS

2 scopes en JS: globale + function


2 API très importantes Angular sont ratés Service et Directives
Le controller est un passe-plat: on choisi seulement ce qu'on expose à la View

Un controller est instancié par new (derrière dans Angular)
Dans le controller je décore l'objet $scope

bowerrc : rc = ReConfiguration

Emmet à mettre en avant pour les devs pour tapper moins de HTML

sous modules peuvent être nommés de la sorte : core-directives (avec tiret) se tradit dans le code par coreDirectives

1. Phase de config : Angular vérifie et constate ce qu'il a dans son app
2. phase de run : démarre les modules

Core: on y attache tous ce qui est transverse à l'appli

Faire une tache grunt pour template de modules (avec bonnes pratiques JS + controller, service etc...)

RequireJS galère pour AngularJS
Browserify galère aussi

##Debug
Dans DOM ng-scope = info de debug
outils de débug : batarang + angular watcher (chrome watchers)

## cyle de vie ng
Max 2000 watchers officiellement par app (ng-repeat dans ng-repeat crée enormement de watcher)

Digest cycle : phase d'analyse et compilsation des directives
ce qui déclenche un digest cycle: 
 - modif watcher
 - ng event (ng-click...)
 - $http
 - $timeout/$interval
Pour déclencher un cycle de digestion:
 - $apply()
 - $applyAsync() : attend le cycle de digestion suivant
Attention $digest à éviter
Ne pas faire de digest cycle pour tout ce qui est purement déco (ex: zoom sur une image). Si on touche pas data, on évite.
=> la bonne solution est de faire une directive et utiliser la méthode link

A voir:
 - latentflip.com/loup pour observer le comportement de JS (notamment les cycles)n faire un test avec setTimeout,0
 - angular-bind-notifier.js : optimisation pour avoir moins de watcher grâce à un système de clé
par exemple sur un ng-repeat :key:truc => il y a un seul watcher
 - la scope chaine en JS

 node.js est un runtime JS, son objet global est son process (window pour un browser)

 Node.js est un REPL (Read Eval Print Loop)

 cls = clear unix dans cmd prompt windows

 ctrl+shit+H = pretty print sublim






