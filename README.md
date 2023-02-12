# Chifoumi-Daniel2

import random

# on defini les 3 choix possible
choix = ("p", "f", "c")

while True:
    
    # on defini la variable du joueur et du programme
    joueur = None
    programme = random.choice(choix)
    
    while joueur not in choix:
        joueur = input("Tapez 'p' (pierre) 'f' (feuille) ou 'c' (ciseaux) pour confirmer votre choix:")

    print(f"Joueur: {joueur}")
    print(f"Ronald: {programme}")
    
    # conditions pour gagner
    if joueur == programme:
        print("Personne a gagné !")
    elif joueur == "p" and programme == "c":
        print("Vous etes trop fort !")
    elif joueur == "f" and programme == "p":
        print("Vous etes trop fort !")
    elif joueur == "c" and programme == "f":
        print("Vous etes trop fort !")
    else:
        print("Aie aie aie vous avez perdu :(")
        
    # on donne la possibilite de rejouer     
    rejouer = input("Voulez vous rejouer ? (tapez 'oui' ou 'non'):")
    if not rejouer == "oui":
        break
    
print("Merci d'avoir jouer ♥ a bientot !!")
