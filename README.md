
# 🚀 Atelier JS n°3 — Programmation Fonctionnelle & Traitement de Données

![Banner](https://capsule-render.vercel.app/api?type=waving&color=0:00c6ff,100:0072ff&height=200&section=header&text=Atelier%203%20JS&fontSize=40&fontAlign=center)

Cet atelier explore la **programmation fonctionnelle** en JavaScript à travers une série d'exercices progressifs,  
culminant sur la création d'une mini application de type **Dashboard Produit** avec tri, recherche, et visualisation graphique.

---

## 🧠 Objectifs pédagogiques

🎯 Maîtriser les concepts suivants :

- Manipulation fonctionnelle des tableaux (`map`, `filter`, `reduce`)
- Traitement de chaînes de caractères
- Gestion de fichiers `.json` côté client avec `FileReader`
- Création d’une mini-application d’analyse de données
- Affichage dynamique avec `Chart.js`
- Structuration fluide d’une page HTML interactive

---

## 🗂️ Contenu par exercice

### ✅ Exercice 1 : Extraire les nombres pairs et trier

```js
const numbers = [1, 7, 10, 9, 8, 2];
const evenSorted = numbers.filter(n => n % 2 === 0).sort((a, b) => a - b);
```

> Objectif : filtrer les éléments pairs et les afficher dans l'ordre croissant.

---

### ✅ Exercice 2 : Factorielle de chaque nombre

```js
const numbers = [1, 3, 4];
const factorials = numbers.map(n => {
  let f = 1;
  for (let i = 1; i <= n; i++) f *= i;
  return f;
});
```

> Objectif : retourner `[1, 6, 24]` en calculant la factorielle de chaque élément.

---

### ✅ Exercice 3 : Manipulation fonctionnelle de texte

```js
const text = "bonjour\nici\nintelligence\njavascript";
const result = text.split("\n")
                   .map(line => line.toUpperCase())
                   .filter(line => line.includes("I"));
```

> Objectif : diviser, transformer et filtrer des lignes contenant la lettre "I".

---

### ✅ Exercice 4 : Extraire la valeur maximale

```js
const max = Math.max(...[1, 7, 10, 9, 8]); // ➜ 10
```

---

### ✅ Exercice 5 : Prix total avec TVA (25%)

```js
const products = [
  { name: "Shirt", price: 20 },
  { name: "Shoes", price: 50 },
  { name: "Hat", price: 15 }
];
const totalTTC = products
  .map(p => p.price * 1.25)
  .reduce((sum, p) => sum + p, 0);
```

---

### ✅ Exercice 6 : Mini App Dashboard Produits

> Application web fonctionnelle avec :  
> 🔸 Chargement de fichier `.json`  
> 🔸 Tri, filtrage, recherche  
> 🔸 Graphique dynamique

**Version avec CSS fluide & responsive :** `ex6/Exercice 6 V2 (css).html`  
**Fichier JSON d'exemple :** `ex6/products.json`

#### Aperçu de la logique JS :

```js
function sortByPrice() {
  const sorted = [...displayedProducts].sort((a, b) => a.price - b.price);
  displayProducts(sorted);
}
```

> Affichage graphique avec `Chart.js` :

```js
new Chart(ctx, {
  type: 'bar',
  data: {
    labels: data.map(p => p.name),
    datasets: [{
      label: 'Stock',
      data: data.map(p => p.stock)
    }]
  }
});
```

---

## 📸 Capture d’écran 
![image](https://github.com/user-attachments/assets/9e4bb60d-6460-4ddf-8f04-8dbd8f0ac322)
![image](https://github.com/user-attachments/assets/1d397991-bafc-4cd7-88c1-fea5a8b5556b)
![image](https://github.com/user-attachments/assets/5035b1db-67e6-4ef1-a63c-31136a0c0f11)

---
## 📎 Fichiers inclus

- `Exercice 1 à 5.js` — Exercices simples avec fonctions pures
- `Exercice 6.html` — Version simple et fonctionnelle
- `Exercice 6 V2 (css).html` — Version complète avec CSS responsive
- `products.json` — Fichier de test JSON

---

## ✍️ Auteurs

- **👨‍💻 AICH Fadi** — **👨‍💻 El Badre Anass**
- **🤖 Intelligence Fonctionnelle JS** — ENSIT  

---
## ✨ Citation Deep du jour

![Quote](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight)

> *"La profondeur n'est pas dans les mots, mais dans l'empreinte qu'ils laissent."*

