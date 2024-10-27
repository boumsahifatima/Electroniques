# **Index des Chapitres**

**[1- Algèbre de Bool](#algèbre-de-bool)**

**[2- Logique Combinatoire](#logique-combinatoire)**

**[3- Logique Séquentielle](#logique-séquentielle)**


<hr>

# **Algèbre de Bool**
### [🔝 Retour à l'index](#index-des-chapitres)

L'algèbre de Bool est le fondement des circuits logiques, utilisée pour modéliser des opérations logiques binaires.

### **Opérations Booléennes de Base :**
  - **ET** (·) : $` A \cdot B `$
  - **OU** (+) : $` A + B `$
  - **NON** (−) : $` \overline{A} `$
  
### **Propriétés Importantes :**
  - **Loi de l’Identité** : $` A + 0 = A `$, $` A \cdot 1 = A `$
  - **Loi de l’Annulation** : $` A + 1 = 1 `$, $` A \cdot 0 = 0 `$
  - **Loi de l’Idempotence** : $` A + A = A `$, $` A \cdot A = A `$
  - **Loi de la Complémentation** : $` A + \overline{A} = 1 `$, $` A \cdot \overline{A} = 0 `$

### **Théorèmes de De Morgan :**
  - $` \overline{A \cdot B} = \overline{A} + \overline{B} `$
  - $` \overline{A + B} = \overline{A} \cdot \overline{B} `$

### **Symbole des Portes Logiques :**
![Portes-Logique](https://github.com/user-attachments/assets/0afc9b1d-eef1-434d-8a1f-523a396cc172)

### **Table de vérité des portes logiques :**
Chaque circuit combinatoire peut être décrit à l'aide d'une table de vérité, qui liste toutes les combinaisons possibles des entrées et leur résultat correspondant.

| Entrée A | Entrée B | ET (A . B) | OU (A + B) | XOR (A ⊕ B) | NON A |
|----------|----------|------------|------------|-------------|-------|
| 0        | 0        | 0          | 0          | 0           | 1     |
| 0        | 1        | 0          | 1          | 1           | 1     |
| 1        | 0        | 0          | 1          | 1           | 0     |
| 1        | 1        | 1          | 1          | 0           | 0     |

---

# **Logique Combinatoire**
### [🔝 Retour à l'index](#index-des-chapitres)

Dans la logique combinatoire, la sortie dépend uniquement des entrées actuelles.

## **Circuits combinatoires courants :**

### Additionneur Demi (Half-Adder) :
  - Permet l'addition de deux bits.
  - Sortie : `Somme = A ⊕ B`, `Retenue = A · B`
  - **Logigramme :**
  
![Half-Adder](https://github.com/user-attachments/assets/6565d1d7-28b6-4385-8204-bb6083dacebb)

### Additionneur Complet (Full-Adder) :
  - Ajoute trois bits (A, B, et une retenue `C_in`).
  - Sortie : `Somme = A ⊕ B ⊕ C_in`, `Retenue = (A · B) + (C_in · (A ⊕ B))`
  - Logigramme :

![Full-Adder](https://github.com/user-attachments/assets/60afee00-3e0e-4381-8bd1-2ae8769a24cb)

### Multiplexeur (MUX) :
  - Sélectionne une entrée parmi plusieurs (2^n entrées pour n bits de sélection).
  - Formule de sortie : `S = A · ¬S + B · S`
  - **Logigramme :**

![MUX4](https://github.com/user-attachments/assets/9f3a279a-1c50-43a0-a587-d940c0d50a35)

### Démultiplexeur (DEMUX) :
  - Prend un signal d'entrée et le distribue sur plusieurs sorties.
  - Inverse du MUX.
  - **Logigramme :**

![DEMUX4](https://github.com/user-attachments/assets/b77412e8-14b8-4cba-ac46-74eeff30b8bf)

### Décodeur :
  - Convertit un code binaire en une seule sortie activée (utilisé dans la gestion de la mémoire ou la sélection de lignes).
  - **Logigramme :**

![Decodeur-4bit](https://github.com/user-attachments/assets/cf268a0c-0613-49ee-8dc9-4d65ca2b764e)

### Encodeur :
  - Inverse du décodeur : il convertit plusieurs signaux d'entrée en un code binaire.
  - **Logigramme :**

![Codeur-4bit](https://github.com/user-attachments/assets/4e370849-0151-4098-b7fa-423af09cf32b)

### Décodeur - 7-Segments :
   - **Formules Algébriques pour le Décodeur BCD - 7 Segments :**

1- **Segment a :**  
   $` a = \overline{A} \, \overline{B} \, C D + \overline{A} B \, \overline{C} \, \overline{D} + A \, \overline{B} \, \overline{C} D + A B \, \overline{C} `$

2- **Segment b :**  
   $` b = \overline{A} B \, \overline{C} D + \overline{A} B C \, \overline{D} + A \, \overline{B} \, \overline{C} D + A B \, \overline{C} D `$

3- **Segment c :**  
   $` c = \overline{A} \, \overline{B} C \, \overline{D} + A B \, \overline{C} D + A B C \, \overline{D} `$

4- **Segment d :**  
   $` d = \overline{A} \, \overline{B} C D + \overline{A} B \, \overline{C} \, \overline{D} + \overline{A} B C D + A \, \overline{B} \, \overline{C} D + A \, \overline{B} C \, \overline{D} `$

5- **Segment e :**  
   $` e = \overline{A} \, \overline{B} C D + \overline{A} B \, \overline{C} D + A \, \overline{B} \, \overline{C} \, \overline{D} + A B \, \overline{C} \, \overline{D} `$

6- **Segment f :**  
   $` f = \overline{A} \, \overline{B} C D + \overline{A} \, \overline{B} \, \overline{C} D + \overline{A} B C \, \overline{D} + A B \, \overline{C} D `$

7- **Segment g :**  
   $` g = \overline{A} \, \overline{B} \, \overline{C} \, \overline{D} + \overline{A} B C \, \overline{D} + A \, \overline{B} C D + A B \, \overline{C} D `$
  - **Logigramme :**

![7-Segment](https://github.com/user-attachments/assets/cd81b6af-1950-4c2e-8e6a-081e28c74d43)

### Comparateur :
  - Un circuit qui compare deux nombres binaires et détermine leur relation (égal, supérieur, inférieur).
  - Sorties typiques : `A = B, A > B, A < B`.
  - **Logigramme :**

![Comparateur-2bit](https://github.com/user-attachments/assets/07c13c1b-559f-4fca-b98e-41b52d6c464a)

### Unité Arithmétique et Logique (UAL) :
  - L'UAL effectue des opérations arithmétiques et logiques telles que l'addition, la soustraction, ET, OU, etc.
  - **Logigramme :**

![UAL](https://github.com/user-attachments/assets/1e562ed6-f423-456e-8f43-b50dc92a8164)

## **Simplification des Circuits Combinatoires :**
- **Table de vérité** : Outil pour vérifier toutes les combinaisons possibles des entrées et leurs résultats.
- **Tableau de Karnaugh** : Utile pour simplifier des fonctions à plusieurs variables en repérant les groupes de 1.


# **Logique Séquentielle**
### [🔝 Retour à l'index](#index-des-chapitres)
Un système séquentiel est un système logique dont l’état des variables de sortie dépend non seulement de
l’état des variables d’entrée mais aussi de l’état précédant des variables de sortie. 

![logique-sequentielle](https://github.com/user-attachments/assets/a2bb8ae8-8510-4579-b787-74b9a01bc90d)


### 1. Bascule SR (Set-Reset) - **Asynchrone**

| **Définition**                                                                                                                                                                                                                     | **Symbole**                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| La bascule SR est un type de bascule qui a deux entrées (Set et Reset) et une sortie. Elle permet de mémoriser l'état logique (1 ou 0) en fonction des valeurs de ses entrées. Elle fonctionne en mode asynchrone.                | ![SR](https://github.com/user-attachments/assets/f02b5c0d-099a-4c19-91aa-18bdc899bc41) |

- **Équation Logique** :
  - $` Q_{n+1} = S + \overline{R} \cdot Q_n `$

- **Table de Vérité** :

  | S (Set) | R (Reset) | Q (Sortie)       | Q̅ (Sortie complémentaire) | **Commentaire**         |
  |---------|-----------|------------------|----------------------------|--------------------------|
  | 0       | 0         | Qn (Maintien)    | Q̅n (Maintien)             | Pas de changement d'état |
  | 0       | 1         | 0                | 1                          | Réinitialisation         |
  | 1       | 0         | 1                | 0                          | Mise à 1                 |
  | 1       | 1         | Indéterminé      | Indéterminé                | État non défini          |

- **Logigramme** :

  *(Espace pour l'image du logigramme de la bascule SR)*

- **Chronogramme** :

  *(Espace pour l'image du chronogramme de la bascule SR)*

---

### 2. Bascule JK - **Synchrone**

| **Définition**                                                                                                                                                                                                                     | **Symbole**                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| La bascule JK est une amélioration de la bascule SR qui évite l'état indéterminé. Elle a deux entrées J (Set) et K (Reset) et nécessite un signal d'horloge pour changer d'état, ce qui en fait une bascule synchrone.             | ![JK](https://github.com/user-attachments/assets/c8bdcfc9-8aa0-47b3-93df-d820af6a430c) |

- **Équation Logique** :
  - $` Q_{n+1} = J \cdot \overline{Q_n} + \overline{K} \cdot Q_n `$

- **Table de Vérité** :

  | J       | K       | Q (Sortie)       | Q̅ (Sortie complémentaire) | **Commentaire**             |
  |---------|---------|------------------|----------------------------|------------------------------|
  | 0       | 0       | Qn (Maintien)    | Q̅n (Maintien)             | Pas de changement d'état     |
  | 0       | 1       | 0                | 1                          | Réinitialisation             |
  | 1       | 0       | 1                | 0                          | Mise à 1                     |
  | 1       | 1       | Q̅n (Bascule)    | Qn (Bascule)               | Inversion de l'état (toggle) |

- **Logigramme** :

  *(Espace pour l'image du logigramme de la bascule JK)*

- **Chronogramme** :

  *(Espace pour l'image du chronogramme de la bascule JK)*

---

### 3. Bascule D (Delay) - **Synchrone**

| **Définition**                                                                                                                                                                                                                     | **Symbole**                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| La bascule D ou bascule à retard est utilisée pour introduire un délai dans un circuit. Elle a une seule entrée D et prend en compte cette entrée lors des transitions d'horloge, ce qui en fait une bascule synchrone.           | ![D](https://github.com/user-attachments/assets/cf3bc7e2-8f43-477e-b3f2-c90fe3a7407c) |

- **Équation Logique** :
  - $` Q_{n+1} = D `$

- **Table de Vérité** :

  | D       | Q (Sortie)       | Q̅ (Sortie complémentaire) | **Commentaire**                 |
  |---------|------------------|----------------------------|----------------------------------|
  | 0       | 0                | 1                          | Réinitialisation                |
  | 1       | 1                | 0                          | Stockage de l'entrée à 1        |

- **Logigramme** :

  *(Espace pour l'image du logigramme de la bascule D)*

- **Chronogramme** :

  *(Espace pour l'image du chronogramme de la bascule D)*

---

### 4. Bascule T (Toggle) - **Synchrone**

| **Définition**                                                                                                                                                                                                                     | **Symbole**                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| La bascule T est un type de bascule qui inverse son état à chaque impulsion d'horloge. Comme elle nécessite un signal d'horloge pour basculer d’un état à l’autre, elle est classée comme une bascule synchrone.                   | ![T](https://github.com/user-attachments/assets/2e9698f7-24e1-41b6-bd9d-1eca77a5efde) |

- **Équation Logique** :
  - $` Q_{n+1} = T \cdot \overline{Q_n} + \overline{T} \cdot Q_n `$ ou plus simplement $` Q_{n+1} = Q_n \oplus T `$

- **Table de Vérité** :

  | T       | Q (Sortie)       | Q̅ (Sortie complémentaire) | **Commentaire**                  |
  |---------|------------------|----------------------------|-----------------------------------|
  | 0       | Qn (Maintien)    | Q̅n (Maintien)             | Pas de changement d'état         |
  | 1       | Q̅n (Bascule)    | Qn (Bascule)               | Inversion de l'état (toggle)     |

- **Logigramme** :

  *(Espace pour l'image du logigramme de la bascule T)*

- **Chronogramme** :

  *(Espace pour l'image du chronogramme de la bascule T)*


<hr>
<h3 align="center"> 🧑🏻‍💻 | Made By : <a href="https://github.com/mohamedtalhaouii" target="_blank">Mohamed Talhaoui</a></h3>
