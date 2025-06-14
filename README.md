# 🧠 Prompt_TP  
**TP : Ingénierie de prompt appliquée à la génération de code avec l’IA**

---

## 1. 🛠️ Solution choisie
**🔹 Blackbox AI**

---

## 2. 📌 Définition brève de la solution
**Blackbox AI** est une plateforme d’IA générative spécialisée dans la génération et l'autocomplétion de code source à partir de prompts en langage naturel.  
Elle prend en charge plusieurs langages de programmation et peut être intégrée dans des environnements de développement comme **VS Code** ou utilisée via son interface web.

---

## 3. ✅ Avantages perçus
- ✅ **Support multilingue** : +20 langages de programmation pris en charge.
- ✅ **Extraction de code à partir de vidéos ou d’images**.
- ✅ **Interface simple et rapide** : utilisable immédiatement sans configuration lourde.

---

## 4. ⚠️ Inconvénients ou limites
- ⚠️ **Compréhension contextuelle limitée** (vs ChatGPT).
- ⚠️ **Peu de personnalisation** du style de code généré.
- ⚠️ **Moins adaptée au débogage ou à l’explication détaillée**.

---

## 5. 💡 Cas d'utilisation typiques
- 🔹 Génération rapide de fonctions simples.
- 🔹 Autocomplétion dans un IDE.
- 🔹 Extraction de code depuis YouTube ou screenshots.
- 🔹 Prototypage ou snippets de test rapide.

---

## 🧾 Conclusion sur un prompt vague

> Le code fonctionne pour les cas simples, mais manque de robustesse, de style et de bonnes pratiques.  
Le vocabulaire dépend de la langue utilisée, ce qui nuit à la réutilisabilité.

---

## 📊 Analyse comparative : Prompt vague vs Prompt spécifique

### 1. Robustesse

| Critère                    | Prompt vague | Prompt spécifique |
|---------------------------|--------------|-------------------|
| Division par zéro         | ✅ Oui        | ✅ Oui            |
| Opérations invalides      | ⚠️ Générique | ✅ Message clair  |
| Validation des entrées    | ❌ Non       | ❌ Non            |
| Arrondi sur division      | ❌ Non       | ✅ Oui            |

**✔️ Conclusion :** Le prompt spécifique est **plus robuste**.

---

### 2. Lisibilité

| Élément                     | Vague              | Spécifique         |
|----------------------------|--------------------|--------------------|
| Noms fonction/paramètres   | `operations(...)`  | `calculate(...)` ✅ |
| Langue des opérations      | Français ❌         | Symboles mathématiques ✅ |
| Commentaires               | ❌ Aucun           | ✅ Docstring clair  |
| Structure du code          | Basique            | ✅ Lisible          |

**✔️ Conclusion :** Le code spécifique est **plus lisible et pro**.

---

### 3. Couverture des cas

| Cas                             | Vague       | Spécifique   |
|--------------------------------|-------------|--------------|
| `calculate(10, 5, '+')`        | ✅ Oui      | ✅ Oui       |
| Division par zéro              | ✅ Oui      | ✅ Oui       |
| Opération invalide `%`         | ✅ Oui      | ✅ Oui       |
| Arrondi division               | ❌ Non      | ✅ Oui       |
| Autres langues (`add`)         | ❌ Inadapté | ✅ Conventionnel |

**✔️ Conclusion :** Le prompt spécifique **couvre mieux les cas**.

---

## 🧠 Résumé : Vague vs Spécifique vs Persona

| Critère                   | Vague   | Spécifique | Persona        |
|--------------------------|---------|------------|----------------|
| Nom explicite            | 🟡 Moyen | ✅ Oui     | ✅ Oui         |
| Docstring                | ❌ Non   | ✅ Basique | ✅ Complet     |
| Gestion des erreurs      | 🟡 Partielle | ✅ Bonne  | ✅ Très bonne |
| Respect de PEP8          | ❌ Non   | 🟡 Approximatif | ✅ Oui    |
| Commentaires             | ❌ Aucun | ✅ Minimes | ✅ Pertinents  |
| `if __name__ == "__main__"` | ❌ Non   | ❌ Non     | ✅ Oui         |

**✅ Conclusion :** Le **prompt avec persona** produit un code :
- plus clair,
- plus maintenable,
- **plus conforme aux standards professionnels**.

---

## 🔍 Analyse Critique

### 1. Prompt vague
- ❌ Utilise des mots comme `"addition"` au lieu de `'+'`.
- ❌ Retourne des erreurs sous forme de texte plutôt que d'exception (`raise`).
- ❌ Pas de vérification de type (`int`, `float`, etc.).

### 2. Temps et qualité
| Type de prompt   | Temps de correction estimé |
|------------------|----------------------------|
| Vague            | ⏱️ 15–30 min               |
| Spécifique       | ⏱️ 5–10 min                |

---

## 🎯 Exercice 2.2 – Exemple et Robustesse

- ✅ Le code généré avec **exemple concret** (input/output) place correctement les tirets.
- ✅ Les **règles implicites** sont clarifiées.
- ✅ Les **messages d’erreurs sont explicites**.
- ✅ Les **cas d’erreurs sont testés**.

### 📌 Conclusion :
**Exemples bien choisis → meilleure robustesse + meilleure interprétation du prompt.**

---

## 🤖 Exercice 2.3 – Calculatrice

### 🔹 Prompt vague
> Résultat fonctionnel mais :  
- Design très basique  
- Pas de gestion clavier, erreurs, ou responsive.

### 🔹 Prompt détaillé
> Permet à l’IA de :
- gérer erreurs (`/0`, double opérateur),
- inclure des effets `hover`, responsive design,
- éviter `eval()` et suivre les bonnes pratiques JS.

**✔️ Conclusion :** Plus le prompt est **précis + illustré**, meilleure est la qualité du code généré.

---

## 🐛 Exercice 3.1 – Débogage

### 🛑 Problème
```bash
TypeError: unsupported operand type(s) for +=: 'int' and 'str'


💡 Cause
'three' est une chaîne, donc total += num échoue.
✅ Correction proposée:
def calculate_average(numbers_list):
    """Calcule la moyenne des éléments numériques dans une liste."""
    numeric_values = [n for n in numbers_list if isinstance(n, (int, float))]
    if not numeric_values:
        raise ValueError("Aucune valeur numérique valide trouvée.")
    return sum(numeric_values) / len(numeric_values)
✅ Tests unitaires avec pytest:
import pytest
from my_module import calculate_average

def test_average_with_integers():
    assert calculate_average([1, 2, 3]) == 2.0

def test_average_with_floats():
    assert calculate_average([1.0, 2.0, 3.0]) == 2.0

def test_average_with_mixed_values():
    assert calculate_average([1, "two", 3]) == 2.0

def test_average_with_no_numerics():
    with pytest.raises(ValueError):
        calculate_average(["a", "b", "c"])

def test_average_with_empty_list():
    with pytest.raises(ValueError):
        calculate_average([])
🛠️ Exercice 3.2 – Refactoring
🔧 Code initial
a = [5, 3, 8, 6, 7, 2] 
for i in range(len(a)): 
    for j in range(i+1, len(a)): 
        if a[i] > a[j]: 
            tmp = a[i] 
            a[i] = a[j] 
            a[j] = tmp 
print(a)
✅ Refactoring avec bonnes pratiques
def sort_numbers(numbers: list) -> list:
    """
    Trie une liste d'entiers en ordre croissant en utilisant un tri par sélection.
    
    Args:
        numbers (list): Liste d'entiers à trier.
    
    Returns:
        list: Liste triée.
    """
    sorted_list = numbers.copy()
    for i in range(len(sorted_list)):
        for j in range(i + 1, len(sorted_list)):
            if sorted_list[i] > sorted_list[j]:
                sorted_list[i], sorted_list[j] = sorted_list[j], sorted_list[i]
    return sorted_list

if __name__ == "__main__":
    sample_numbers = [5, 3, 8, 6, 7, 2]
    print("Liste triée :", sort_numbers(sample_numbers))

