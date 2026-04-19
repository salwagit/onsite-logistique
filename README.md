# 🚚 **OnSite Logistics** - Application Mobile Logistique Full-Stack

[![NestJS](https://img.shields.io/badge/NestJS-%5E11.0.1-blue.svg)](https://nestjs.com/)
[![React Native](https://img.shields.io/badge/React_Native-0.81.5-green.svg)](https://reactnative.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.7.3-blue.svg)](https://typescriptlang.org/)
[![Expo](https://img.shields.io/badge/Expo-%7E54.0.33-orange.svg)](https://expo.dev/)

## 📱 **Description**
**OnSite Logistics** est une application mobile complète pour la **gestion de livraisons sur site en temps réel**.  
Admin crée des missions de colis, assigne chauffeurs/véhicules ; Chauffeurs acceptent et mettent à jour ; Destinataires suivent.

**Rôles** :
- **Admin** : Créer missions/véhicules
- **Chauffeur** : Accepter missions, update statut
- **Destinataire** : Suivi colis/carte

## 🛠️ **Tech Stack**
| Partie | Technologies |
|--------|--------------|
| **Backend** | NestJS, TypeORM, PostgreSQL, JWT, bcrypt |
| **Frontend** | React Native (Expo), Redux, React Navigation, Maps |
| **Autres** | Socket.io (real-time?), Axios |

## 🚀 **Installation & Démarrage**

### Prérequis
- Node.js 18+
- PostgreSQL
- Expo CLI : `npm i -g expo-cli`

### Backend
```bash
cd back-end
npm install
cp .env.example .env  # Configure DB/JWT
npm run start:dev     # http://localhost:3000
```

### Frontend
```bash
cd front-end
npm install
npx expo start        # Scan QR Android/iOS
```

### DB Setup
```sql
-- Migration TypeORM ou Prisma
CREATE DATABASE onsite_logistics;
```

## ✨ **Fonctionnalités Principales**

1. **Auth** : Login/Register (JWT, rôles)
2. **Missions** : Créer (pickup/dropoff/priority), assigner driver/vehicle, statuts (pending → completed)
3. **Véhicules** : CRUD (plaque, statut, driver)
4. **Dashboards** : Rôles spécifiques + Profile/Settings
5. **Tracking** : Carte (react-native-maps), notifications?

**Entités** : User (role), Mission (locations, driverId, vehicleId), Vehicle.

## 📱 **Screenshots**
*(Ajoutez images : login, admin create mission, driver trips, receiver map)*

![Admin Dashboard](screenshots/admin.png)
![Create Mission](screenshots/create-mission.png)

## 📊 **Structure du Projet**
```
onsite-logistics/
├── back-end/          # NestJS API
│   ├── src/auth/      # JWT
│   ├── src/missions/  # Core
│   └── src/vehicles/
├── front-end/         # React Native App
│   ├── src/screens/   # Admin/Driver/Receiver
│   └── src/services/  # APIs
└── README.md
```

## 🤝 **Contribuer**
1. Fork → Clone
2. `git checkout -b feature/xyz`
3. Commit/push → PR


