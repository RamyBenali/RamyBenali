<div align="center">

# Ramy Benali · API Reference

**Full stack & SaaS developer — Laravel · TypeScript · paiement en ligne**

![version](https://img.shields.io/badge/version-2026.11-0969da?style=flat-square)
![status](https://img.shields.io/badge/status-operational-2da44e?style=flat-square)
![stage](https://img.shields.io/badge/stage-disponible%20mars%202027-f59e0b?style=flat-square)
![base url](https://img.shields.io/badge/base%20url-ramy--benali.pages.dev-6e7781?style=flat-square)

</div>

---

## Introduction

Cette API décrit un développeur. Elle est REST, renvoie du JSON, et elle répond vraiment :

```bash
curl https://ramy-benali.pages.dev/api/ramy
```

## The `developer` object

```json
{
  "id": "dev_RamyBenali",
  "object": "developer",
  "name": "Ramy Benali",
  "location": "Montbéliard, France",
  "role": "Full stack developer",
  "company": "Frog Tech",
  "education": {
    "current": "L3 Informatique — Université Marie et Louis Pasteur",
    "previous": "Master 1 Génie logiciel — Université de Béjaïa"
  },
  "languages": ["fr", "ar", "es", "de"],
  "currently_building": "Intégration Stripe Connect sur un SaaS en production",
  "available_for": {
    "type": "internship",
    "start": "2027-03-15",
    "duration_months": 3,
    "location": "Île-de-France"
  },
  "livemode": true
}
```

## Endpoints

| Méthode | Endpoint | Description |
| :-- | :-- | :-- |
| `GET` | [`/v1/stack`](#get-v1stack) | Technologies utilisées en production |
| `GET` | [`/v1/projects`](#get-v1projects) | Projets publics |
| `GET` | [`/v1/changelog`](#get-v1changelog) | Parcours, version par version |
| `POST` | [`/v1/hire`](#post-v1hire) | Proposer un stage |

---

### `GET /v1/stack`

| Scope | Valeurs |
| :-- | :-- |
| `backend` | ![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white) ![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) |
| `frontend` | ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Blade](https://img.shields.io/badge/Blade-FF2D20?style=flat-square&logo=laravel&logoColor=white) |
| `mobile` | ![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white) |
| `payments` | ![Stripe](https://img.shields.io/badge/Stripe%20Connect-635BFF?style=flat-square&logo=stripe&logoColor=white) |
| `infra` | ![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) |
| `low_level` | ![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black) ![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white) |

### `GET /v1/projects`

| `id` | `language` | `description` |
| :-- | :-- | :-- |
| [`HomeInspire`](https://github.com/RamyBenali/HomeInspire) | Java | Logiciel complet de gestion d'agence immobilière |
| [`SaldaeTrip`](https://github.com/RamyBenali/SaldaeTrip) | Dart | <!-- TODO : une phrase --> |
| [`GeoGuiz`](https://github.com/RamyBenali/GeoGuiz) | TypeScript | <!-- TODO : une phrase --> |
| [`SiteRP`](https://github.com/RamyBenali/SiteRP) | TypeScript | <!-- TODO : une phrase --> |
| [`Pong-Game`](https://github.com/RamyBenali/Pong-Game) | C | Pong en C |

### `GET /v1/changelog`

```mermaid
gitGraph
   commit id: "2022 · Bac Sciences Expérimentales"
   commit id: "2025 · Licence Informatique, Béjaïa"
   commit id: "2026 · Master 1 Génie logiciel"
   branch france
   checkout france
   commit id: "08/2026 · Arrivée à Montbéliard"
   commit id: "L3 Informatique · UMLP"
   branch frog-tech
   checkout frog-tech
   commit id: "Dev full stack SaaS"
   commit id: "Stripe Connect"
   checkout france
   commit id: "03/2027 · Stage" type: HIGHLIGHT tag: "next-release"
```

### `POST /v1/hire`

```bash
curl https://ramy-benali.pages.dev/api/hire \
  -d type="internship" \
  -d start="2027-03-15" \
  -d duration_months=3 \
  -d location="Île-de-France"
```

```json
{
  "status": 201,
  "message": "Created. Réponse sous 24 h.",
  "contact": {
    "portfolio": "https://ramy-benali.pages.dev/dev",
    "linkedin": "https://linkedin.com/in/ramy-benali-dev",
    "email": "benali.ramy.2@gmail.com"
  }
}
```

## Errors

| Code | Signification |
| :-- | :-- |
| `200` | Tout fonctionne |
| `402` | Café requis |
| `409` | Conflit de merge un vendredi à 18 h |
| `429` | Trop de réunions |

<div align="center">
<sub>Documentation générée à la main · dernière mise à jour : novembre 2026</sub>
</div>
