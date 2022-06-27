# Tests Unitaires contrat "Voting"

Test portant sur le contrat "voting.sol" originaire de la correction. Aucune modofication apporté.

Tests fait dans l'ordre chronologique des fonctions et de leurs déroulement interne.
___

## Nombre de test effectué : 17

Pas de tableau avec le pourcentage de tests réussi car pas de coverage car sur Truffle.

___

### 1) Test de la fonction addVoter


### 3 tests :

1. Owner ne doit pas pouvoir rajouter une voter
2. Doit retourner un voter et être Whitelisted
3. Doit retourner un voter et ne pas être Whitelisted

___

### 2) Test de la fonction addProposal

### 3 tests :

1. Doit ne pas accepter encore de proposition
2. Doit ne pas accepter de réponse vide
3. Doit retourner les propositions émise

___

### 3) Tests des require sur le Modifier et les Workflows

### 5 tests :

1. Doit revert si l'on est pas un voter
2. Doit revert si la phase de proposition n'est pas terminée 
3. Doit revert si la session de vote n'a pas débuté 
4. Doit revert si la session de vote n'est pas terminée
5. Doit revert si la session d'enregistrement des proposition ne peut être démarrée 
___

### 4) Tests de la fonction vote

### 3 tests :

1. Doit retourner qu'un voter a déjà voté
2. Doit avoir pu rentrer un vote 
3. Doit retourner l'id du vote par l'emit "Voted"

___

### 5) Tests de la fonction "tallyVotes"

### 3 tests :

1. Doit retourner que les votes ne sont pas terminés
2. Doit pourvoir retourner la proposition gagnante
3. Doit pouvoir passer du status 4 au status 5
