# 🚀 Guide de Contribution

Merci de vouloir contribuer à **QuantumShift** ! Ce guide vous expliquera comment bien démarrer.

---

## 📖 Table des Matières

1. [Code de Conduite](#code-de-conduite)
2. [Comment Commencer](#comment-commencer)
3. [Types de Contributions](#types-de-contributions)
4. [Processus de Contribution](#processus-de-contribution)
5. [Recommandations de Code](#recommandations-de-code)
6. [Commit & Messages](#commit--messages)
7. [Tests](#tests)
8. [Documentation](#documentation)

---

## 📜 Code de Conduite

Lire attentivement [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) avant de contribuer. Toutes les contributions doivent respecter nos standards communautaires.

---

## 💡 Comment Commencer

### Prérequis
- GitHub account
- Git configuré localement
- Python 3.10+ ou Go 1.24+ (selon le projet)
- Compréhension basique de Git & GitHub

### Setup Rapide

```bash
# 1. Fork le répo
gh repo fork Quantum-Shift-app/quantumshift_ai --clone

# 2. Créez une branche
cd quantumshift_ai
git checkout -b feature/awesome-feature

# 3. Installez les dépendances
pip install -r requirements.txt
pre-commit install  # Hooks git pour la qualité du code

# 4. Créez, testez, committez
# (détails dans les sections suivantes)

# 5. Push & créez une PR
git push origin feature/awesome-feature
```

### Pour les Sous-Projets

- **AETHER** : `pip install -e ".[dev]"` + `pytest`
- **TermAI** : `go mod download` + `make build`
- **Frontend** : `npm install` + `npm run dev`

---

## 📋 Types de Contributions

### 🐛 Bug Reports
Trouvé un bug ? Reportez-le :

```markdown
**Description** : Une description claire du bug
**Reproduction** : Étapes pour reproduire
**Expected** : Le comportement attendu
**Actual** : Le comportement observé
**Environmental** : Version, OS, Configuration
**Logs** : Sortie d'erreur (si applicable)
```

### ✨ Feature Requests
Avez-vous une idée ? Créez une issue de feature :

```markdown
**Problem Statement** : Quel problème résolvez-vous ?
**Proposed Solution** : Comment pourrait-ce fonctionner ?
**Alternatives** : Avez-vous envisagé d'autres solutions ?
**Additional Context** : Screenshots, liens, idées
```

### 📚 Documentation
- Améliorer le README
- Ajouter des examples de code
- Clarifier les diagrammes
- Corriger les typos

### 🔍 Code Reviews
Reviewez les PRs des autres ! C'est une excellente façon d'apprendre.

### 🎨 Design & UX
- Proposer des améliorations visuelles
- Suggérer une meilleure UX
- Tester l'accessibilité

---

## 🔄 Processus de Contribution

### Step 1️⃣ : Créez une Issue

**Avant** de commencer à coder, créez une issue pour :
- Discuter de votre approche
- Obtenir un retour de l'équipe
- Éviter les doublons

```bash
# Exemple : Issue de bug
Title: [BUG] Crash au téléchargement de fichiers > 500MB
Label: bug, priority:high
```

### Step 2️⃣ : Assignez-vous

Commentez sur l'issue :
> "Je serais heureux de corriger cela. Puis-je me l'assigner ?"

L'équipe vous assignera la tâche.

### Step 3️⃣ : Créez une Branche

```bash
# Convention de nommage
git checkout -b [type]/[description]

# Exemples
git checkout -b feature/quantum-optimizer
git checkout -b bugfix/crash-on-large-files
git checkout -b docs/api-reference
git checkout -b refactor/test-structure
```

Types acceptés : `feature/`, `bugfix/`, `docs/`, `refactor/`, `perf/`, `chore/`

### Step 4️⃣ : Commitez avec Style

```bash
# Format convenu (Conventional Commits)
git commit -m "feature: add quantum QAOA optimizer for scheduling

- Implements quantum approximate optimization algorithm
- Reduces computation time from O(n³) to O(log n)
- Includes 25 unit tests with 100% coverage
- Closes #1234"
```

**Rules** :
- ✅ Type + description en minuscules : `feature:`, `fix:`, `docs:`, `test:`, `refactor:`
- ✅ Première ligne ≤ 50 caractères
- ✅ Corps ≤ 72 caractères par ligne
- ✅ Référencez l'issue : `Closes #1234`
- ✅ Signez si possible : `git commit -S -m ...`

### Step 5️⃣ : Testez Localement

```bash
# Exécutez les tests
pytest tests/ -v --cov=src/

# Vérifiez le linting
ruff check .
mypy src/ --config ruff.toml  # TypeScript check si applicable

# Format le code
ruff format .
```

### Step 6️⃣ : Créez une Pull Request

```bash
# Push et ouvrez une PR
git push origin feature/quantum-optimizer
```

**Template PR** (sera pré-rempli) :

```markdown
## 🎯 Description
Brève description de ce que vous faites

## 📝 Détails
Explication plus détaillée

## 🔗 Issues Liées
Closes #1234

## 🧪 Testing
- [ ] Tests unitaires ajoutés
- [ ] Tous les tests passent
- [ ] Coverage > 80%

## ✅ Checklist
- [ ] Code review complétée
- [ ] Pas de merge conflicts
- [ ] Noms explicites (variables, fonctions)
```

### Step 7️⃣ : Code Review

1. L'équipe review votre PR
2. Répondez aux commentaires poliment  3. Demandez des clarifications si nécessaire
4. Une fois approuvée → merged ! 🎉

---

## 🎯 Recommandations de Code

### Python

```python
# ✅ BON
def calculate_quantum_state(qubits: int, theta: float) -> np.ndarray:
    """
    Calculate quantum state vector.
    
    Args:
        qubits: Number of qubits
        theta: Rotation angle in radians
        
    Returns:
        Quantum state vector
    """
    logger.debug(f"Initializing {qubits} qubits")
    # Implementation...
```

```python
# ❌ MAUVAIS
def calc_q_state(n, t):
    # calculate quantum state
    st = np.zeros(n)
    # ...
    return st
```

### TypeScript/Go

- Utilisez des noms explicites
- Tapez fortement (TypeScript strict mode)
- Commentez les logiques complexes
- Maintenez une couverture > 80%

---

## 📝 Commit & Messages

### Format Standard : Conventional Commits

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

**Types** : `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `chore`

**Exemple complet** :
```
feat(api): add webhook support for payment notifications

- Implement POST /webhooks/payment endpoint
- Add signature verification using HMAC-SHA256
- Store webhook logs in audit table
- Add 10 integration tests

Closes #892
BREAKING CHANGE: Removed deprecated /v1/payments endpoint
```

---

## 🧪 Tests

### Couverture Attendue

- **Minimum** : 70%
- **Cible** : 85%+
- **Critical paths** : 100%

### Exécution des Tests

```bash
# Tous les tests
pytest tests/ -v

# Avec coverage
pytest tests/ --cov=src --cov-report=html

# Tests spécifiques
pytest tests/test_quantum_optimizer.py -k "test_qaoa"

# Test depuis une PR
# (Les tests s'exécutent automatiquement via GitHub Actions)
```

### Exemple de Test

```python
import pytest
from src.quantum_optimizer import QuantumOptimizer

class TestQuantumOptimizer:
    
    @pytest.fixture
    def optimizer(self):
        """Initialize optimizer before each test"""
        return QuantumOptimizer(n_qubits=5)
    
    def test_initialization(self, optimizer):
        """Test that optimizer initializes correctly"""
        assert optimizer.n_qubits == 5
        assert optimizer.state is not None
    
    def test_qaoa_convergence(self, optimizer):
        """Test that QAOA algorithm converges"""
        result = optimizer.run_qaoa(iterations=100)
        assert result.energy < initial_energy
        assert result.convergence_rate > 0.9
```

---

## 📚 Documentation

### Docstrings (Python)

```python
def solve_circuit(circuit: QuantumCircuit, shots: int = 1024) -> Dict:
    """
    Execute quantum circuit and measure results.
    
    This function simulates a quantum circuit on a classical backend
    and returns measurement statistics. For production use, consider
    using cloud backends like IBM Quantum or AWS Braket.
    
    Args:
        circuit (QuantumCircuit): Input quantum circuit to execute
        shots (int, optional): Number of measurement repetitions.
                              Defaults to 1024.
    
    Returns:
        Dict: Dictionary with keys:
            - 'counts': Measurement outcome counts
            - 'fidelity': Average measurement fidelity
            - 'time_ms': Execution time in milliseconds
    
    Raises:
        ValueError: If circuit has > 20 qubits
        RuntimeError: If backend is unavailable
    
    Example:
        >>> circuit = create_bell_pair()
        >>> result = solve_circuit(circuit, shots=2048)
        >>> print(result['counts'])
        {'00': 1024, '11': 1024}
    
    Note:
        Thread-safe. Uses a global simulation backend.
    """
```

### README

- Soyez clair et concis
- Incluez des examples
- Mentionnez les prérequis
- Liez vers la documentation complète

---

## 🎓 Ressources Utiles

- [GitHub Docs - Contributing](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Real Python Testing](https://realpython.com/python-testing/)
- [Go Code Review Comments](https://github.com/golang/go/wiki/CodeReviewComments)

---

## ❓ Questions ?

- 💬 Utilisez les Discussions GitHub
- 📧 Contactez : contribute@quantum-shift.fr
- 🐛 Reportez les bugs directement en issue

---

**Merci de rendre QuantumShift meilleur ! 🌌✨**

*Dernière mise à jour : Mars 2026*
