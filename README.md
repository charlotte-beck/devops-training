# DevOps Training

Labs for the DevOps training.

## GIT

### Lab 1.A

#### Énoncé

Modifier l'historique pour atteindre les objectifs suivants :

- Changer le message associé au commit 03. Le nouveau message sera "03- Started Hello World Feature".

- Permuter l'ordre des commits 02 et 03. Le commit 03 portera le message "02- Started Hello World Feature", le commit 02 portera alors le message "03- Finished Hello World Feature".

- Changer l'auteur du commit 05 pour qui'il soit Me, the Challenger.

- Écraser l'actuel commit numéro 06.

- Fusionner les 3 commits 07, 08, et 09 en un seul commit portant le message "Add doc".

- Fusionner les commits 10 et 11 en ne conservant que le message du commit 10.

#### Réalisation

- Utiliser la commande `git rebase -i HEAD~10`

- Lors de la sélection des modes, modifier comme suit :

```
reword c5b62a7 03- StArrtid Helo Volrd feature  
reword 7334685 02- Finished Hello World feature  
pick 51f0593 04- Really made the thingy done  
edit 0e79be6 05- debugging  
drop 2866904 06- important secret  
reword c26947b 07- Add doc - step 1  
fixup dc90067 08- Add doc - step 2  
fixup f34ae9c 09- Add doc -step 3  
pick c418784 10- Test for the feature hello world  
fixup 5d7bd5a 11- I forgot a semicolon
```

- Lors des prompts, modifier comme suit :

  * Renommer le message du commit 03 en "02- Started Hello World feature"
  * Renommer le message du commit 02 en "03- Finished Hello World feature"
  * Effectuer le commande `git commit --amend --author="Me, the Challenger <challenger@challengeland.com>" --no-edit` suivi de la commande `git rebase --continue`
  * Renommer le message du commit 07 en "Add doc"
