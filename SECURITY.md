# 🔒 Politique de Sécurité

## Signaler une Vulnérabilité

Nous prenons la sécurité très au sérieux au sein de **QuantumShift**. Si vous découvrez une vulnérabilité de sécurité, **veuillez NE PAS la publier publiquement** sur les issues GitHub.

### Procédure de Signalement Responsable

Envoyez un email à **security@quantum-shift.fr** avec les informations suivantes :

1. **Description** : Une description claire de la vulnérabilité
2. **Composant** : Quel répo est affecté (QuantumShift AI, AETHER, TermAI)
3. **Impact** : Évaluation de la gravité (critique, haute, moyenne, basse)
4. **Preuve de Concept** : Code ou étapes pour reproduire (si possible)
5. **Timeline** : Quand avez-vous découvert cela ?

### Timeline de Réponse

- **Accusé de réception** : Dans les 24 heures
- **Triage initial** : Dans les 48 heures  
- **Patch en préparation** : 5-10 jours selon la gravité
- **Divulgation publique** : Après la publication du patch (ou après 90 jours max)

> **Note** : Les chercheurs en sécurité ayant suivi ce processus seront reconnus dans nos release notes (si vous le souhaitez).

---

## 🛡️ Bonnes Pratiques de Sécurité

### Pour les Développeurs

- ✅ Utilisez les secrets GitHub pour les variables sensibles (API keys, tokens)
- ✅ Activez l'authentification 2FA sur votre compte GitHub
- ✅ Signez vos commits avec GPG (`git commit -S`)
- ✅ Passez les audits de code avant de merger vers `main`
- ✅ Testez les dépendances avec `pip audit` et `npm audit`

### Pour les Contributeurs Externes

- ✅ Fork le répo et créez une branche dédiée
- ✅ Ne committez JAMAIS de secrets, tokens, ou clés API
- ✅ Suivez les conventions de code du projet
- ✅ Soumettez une PR avec une description détaillée

### Outils de Scan utilisés

- **SAST** : `Ruff`, `Pylint`, `TypeScript strict mode`
- **Secrets** : `Truffelhog`, `git-secrets`
- **Dépendances** : `pip audit`, `npm audit`, `go list -m all`
- **Container** : `Trivy`, `Docker Scout`

---

## 🔑 Gestion des Secrets

### ❌ À NE JAMAIS faire

```python
# ❌ MAUVAIS
API_KEY = "sk-1234567890abcdef"
DB_PASSWORD = "admin123"
```

### ✅ À faire

```python
import os
from dotenv import load_dotenv

load_dotenv()
API_KEY = os.getenv("OPENAI_API_KEY")
DB_PASSWORD = os.getenv("DATABASE_PASSWORD")
```

Stockez les secrets dans :
- `.env.local` (local development)
- GitHub Secrets (CI/CD)
- Environment variables (production)

---

## 🚨 Incidents de Sécurité Confirmés

Nous maintenant à jour un registre des vulnérabilités résolues. Consultez les **Security Advisories** dans chaque répo :

- [QuantumShift AI - Advisories](https://github.com/Quantum-Shift-app/quantumshift_ai/security/advisories)
- [AETHER - Advisories](https://github.com/Quantum-Shift-app/aether/security/advisories)
- [TermAI - Advisories](https://github.com/Quantum-Shift-app/termai/security/advisories)

---

## 📚 Ressources Supplémentaires

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [GitHub Security Best Practices](https://docs.github.com/en/code-security)
- [CWE Top 25](https://cwe.mitre.org/top25/)

---

**Merci de nous aider à maintenir un écosystème sûr ! 🙏**
