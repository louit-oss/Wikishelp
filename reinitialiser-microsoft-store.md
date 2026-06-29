====== Résoudre les bugs de téléchargement du Microsoft Store (wsreset) ======

Cette fiche pratique explique comment vider et réinitialiser le cache de la boutique d'applications **Microsoft Store** sous Windows 10 et Windows 11. Cette manipulation résout la majorité des blocages liés aux téléchargements impossibles ou aux mises à jour d'applications qui restent figées.

===== 1. Contexte et Symptômes =====

Le cache du Microsoft Store peut parfois accumuler des fichiers corrompus lors de son utilisation ou suite à une mise à jour système incomplète. Les symptômes les plus fréquents sont :
  * Les applications restent bloquées indéfiniment sur "En attente" ou "Téléchargement en cours".
  * La boutique affiche un code d'erreur générique (ex: 0x80073D05 ou 0x8024001E).
  * L'application Microsoft Store se ferme toute seule immédiatement après son ouverture (crash au démarrage).

===== 2. La Solution : La commande WSReset.exe =====

Windows intègre un outil officiel en ligne de commande nommé **WSReset** (Windows Store Reset). Cet utilitaire permet de vider l'intégralité du cache de l'application sans supprimer les applications déjà installées ni modifier les paramètres du compte Microsoft de l'utilisateur.

==== Procédure étape par étape ====

  # L'utilisateur doit fermer l'application Microsoft Store si celle-ci est actuellement ouverte.
  # Ouvrir le menu Démarrer de Windows ou appuyer sur le raccourci clavier **touche Windows + R** pour ouvrir la boîte de dialogue "Exécuter".
  # Dans le champ de saisie, taper scrupuleusement la commande suivante :
<code>
wsreset.exe
</code>
  # Valider en appuyant sur la touche **Entrée** (ou en cliquant sur "OK").



==== Que se passe-t-il ensuite ? ====

Une fenêtre d'invite de commandes (un écran noir) totalement vide apparaît à l'écran. 

:!: **Important :** Il ne faut pas fermer cette fenêtre manuellement. L'utilitaire travaille en arrière-plan et l'opération peut prendre entre 10 secondes et 2 minutes selon l'état du système. :!:

Dès que le nettoyage est terminé, la fenêtre noire se ferme automatiquement et l'application Microsoft Store s'ouvre d'elle-même sur une page d'accueil propre.

===== 3. Que faire si le problème persiste ? =====

Si la commande ''wsreset'' n'a pas suffi à débloquer la situation, il est recommandé de procéder à une réparation plus profonde via les paramètres système :

  * Se rendre dans les **Paramètres** de Windows > **Applications** > **Applications installées**.
  * Rechercher **Microsoft Store** dans la liste.
  * Cliquer sur les trois petits points, puis sur **Options avancées**.
  * Faire défiler la page jusqu'à la section "Réinitialiser" et cliquer d'abord sur **Réparer**. Si cela échoue, cliquer sur **Réinitialiser** (cette action déconnectera temporairement le compte utilisateur de la boutique, il suffira de se reconnecter).