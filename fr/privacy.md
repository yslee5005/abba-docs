---
layout: default
title: Politique de confidentialité — Abba
---

# Politique de confidentialité

**Dernière mise à jour : 22 avril 2026**

## 1. Introduction

Abba (« nous », « notre », « l'application ») est un compagnon mobile de prière et de temps de méditation (Quiet Time) conçu pour les chrétiens qui souhaitent prier plus profondément. Cette politique de confidentialité décrit comment Abba collecte, utilise, stocke et protège vos informations lorsque vous utilisez l'application iOS (Bundle ID : `com.ystech.abba`).

Abba est actuellement exploité en tant que projet de développeur indépendant. Lorsque nous utilisons « nous » dans cette politique, nous désignons l'équipe Abba. Si Abba devient une société enregistrée à l'avenir, cette politique sera mise à jour en conséquence.

Cette politique s'applique dans le monde entier. Nous suivons les principes du Règlement général sur la protection des données de l'UE (RGPD), du California Consumer Privacy Act (CCPA) et de la loi coréenne sur la protection des données personnelles (PIPA), lorsque cela est applicable.

## 2. Informations que nous collectons

### 2.1 Informations de compte
Abba fonctionne en mode **anonyme par défaut**. Lorsque vous ouvrez l'application pour la première fois, nous créons un identifiant utilisateur anonyme (UUID) afin que vos prières et paramètres puissent être synchronisés entre les sessions. Vous n'avez pas besoin de fournir un nom, une adresse e-mail ou un numéro de téléphone pour utiliser Abba.

Vous pouvez éventuellement vous connecter avec **Apple Sign-In** ou **Google Sign-In** pour sauvegarder vos données. Dans ce cas, nous recevons votre adresse e-mail et un identifiant unique fourni par Apple ou Google. Vous pouvez utiliser « Masquer mon e-mail » avec Apple Sign-In si vous le préférez.

### 2.2 Contenu des prières (données principales)
Lorsque vous utilisez Abba, nous collectons :
- **Enregistrements audio** de vos prières parlées
- **Transcriptions** générées à partir de ces enregistrements
- **Textes de méditation et réflexions** que vous écrivez ou générez
- **Passages bibliques** que vous mettez en favoris

Il s'agit des données les plus sensibles qu'Abba traite, et nous les traitons avec soin. Votre audio est stocké dans votre propre dossier privé sur notre stockage sécurisé. Seul vous pouvez y accéder. Nous ne l'écoutons pas, ne le partageons pas et ne l'utilisons pas à des fins de marketing.

### 2.3 Informations d'abonnement
Si vous vous abonnez à Abba Pro, un service tiers appelé **RevenueCat** enregistre votre statut d'abonnement (actif, expiré, essai, etc.) avec l'identifiant anonyme. Nous ne recevons **pas** votre numéro de carte bancaire — celui-ci reste chez Apple.

### 2.4 Informations techniques
- Langue de l'appareil (pour définir votre langue d'application par défaut)
- Rapports de plantage avec données personnelles masquées (via Sentry)
- Jeton de notification push (FCM, optionnel — uniquement si vous activez les notifications)
- Version de l'application et version iOS (pour le débogage)

## 3. Comment nous utilisons vos informations

Nous utilisons vos informations pour :
- **Fournir une analyse par IA** de vos prières et réflexions de temps de méditation (Google Gemini)
- **Synchroniser vos données** entre sessions et appareils
- **Gérer votre abonnement** et vos droits
- **Corriger les bogues et améliorer l'application** grâce aux rapports de plantage
- **Envoyer des notifications push optionnelles** (rappels quotidiens de temps de méditation) si vous y consentez

Nous ne faisons **pas** :
- Afficher de la publicité de quelque nature que ce soit
- Vendre vos données à qui que ce soit
- Partager le contenu de vos prières avec des tiers (sauf le traitement IA décrit ci-dessous)
- Utiliser votre contenu pour entraîner des modèles d'IA

## 4. Services tiers

Abba s'appuie sur un petit nombre de services de confiance pour fonctionner.

| Service | Objectif | Données envoyées | Région |
|---|---|---|---|
| **Supabase** | Base de données et authentification | ID anonyme, prières, métadonnées | US / UE |
| **Google Gemini API** | Analyse IA des prières | Texte de prière uniquement | Google Cloud |
| **RevenueCat** | Gestion des abonnements | ID anonyme, reçus d'achat | US |
| **Sentry** | Rapports de plantage (PII masqués) | Traces d'erreur sans e-mails, longues transcriptions, JWT supprimés | US / UE |
| **Firebase Cloud Messaging** | Notifications push (optionnel) | Jeton FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Liaison de compte optionnelle | E-mail, ID fournisseur | Apple / Google |

**Google Gemini :** Conformément à la politique publiée par Google pour l'utilisation payante de l'API, le contenu de prière envoyé à Gemini **n'est pas utilisé pour entraîner les modèles d'IA de Google**. Le traitement est transitoire.

**Masquage PII Sentry :** Nous appliquons des règles de masquage avant d'envoyer les rapports de plantage — les e-mails, les transcriptions coréennes de plus de 50 caractères, les JWT et autres identifiants sont supprimés.

## 5. Stockage et sécurité des données

- Toutes les données en transit sont chiffrées via HTTPS (TLS 1.2+).
- Les données au repos sont protégées par le chiffrement de notre fournisseur de base de données.
- La **sécurité au niveau des lignes (RLS)** de Supabase garantit que vous ne pouvez accéder qu'à vos propres données.
- Les fichiers audio sont stockés dans des dossiers par utilisateur avec un accès contrôlé par votre jeton d'authentification.
- Les jetons d'accès sont stockés dans l'iOS Secure Enclave (`flutter_secure_storage`), jamais dans des préférences en clair.

Nous conservons vos données tant que votre compte est actif. Si vous supprimez votre compte, nous supprimons vos données dans un délai de **30 jours**, sauf lorsque nous sommes légalement tenus de conserver des enregistrements (tels que les dossiers fiscaux pour les achats d'abonnement, qu'Apple/RevenueCat conservent selon leurs propres politiques).

## 6. Vos droits

Vous disposez des droits suivants sur vos données personnelles :

- **Accès** — demander une copie des données que nous détenons à votre sujet
- **Rectification** — nous demander de corriger des informations inexactes
- **Suppression** — nous demander de supprimer votre compte et vos données (disponible dans l'application : Paramètres → Compte → Supprimer le compte, ou par e-mail)
- **Portabilité** — demander un export de vos données dans un format lisible par machine
- **Opposition** — vous opposer à certains traitements
- **Retrait du consentement** — vous pouvez révoquer le consentement pour les notifications push, le traitement IA ou la liaison de compte à tout moment

Pour les résidents du RGPD (UE) et du CCPA (Californie), ces droits sont garantis par la loi. Pour exercer un droit, envoyez un e-mail à **rrallvv@gmail.com**. Nous répondons sous 30 jours.

## 7. Confidentialité des enfants

Abba est classé 4+ dans l'App Store. Nous ne collectons pas sciemment d'informations auprès d'enfants de moins de 13 ans (COPPA) ou de moins de 16 ans (RGPD, dans certains pays de l'UE) sans le consentement parental vérifiable. Si vous pensez qu'un enfant a fourni des informations personnelles, veuillez nous contacter et nous les supprimerons immédiatement.

## 8. Transferts internationaux de données

Notre infrastructure est hébergée aux États-Unis et dans l'Union européenne. En utilisant Abba, vous consentez au transfert et au traitement de vos données dans ces régions. Nous nous appuyons sur les Clauses contractuelles types (CCT) lorsque cela est requis.

## 9. Demandes gouvernementales et légales

Nous divulguons les données des utilisateurs uniquement lorsque la loi l'exige (citation à comparaître valide, ordonnance judiciaire ou équivalent). Nous ne publions pas encore de rapport de transparence, mais nous nous engageons à informer les utilisateurs concernés lorsque la loi le permet.

## 10. Modifications de cette politique

Nous pouvons mettre à jour cette politique de confidentialité à mesure qu'Abba évolue. Lorsque nous apportons des modifications substantielles, nous vous en informons dans l'application et mettons à jour la date « Dernière mise à jour » en haut. L'utilisation continue d'Abba après les modifications signifie que vous acceptez la politique mise à jour.

## 11. Contactez-nous

Questions, demandes ou réclamations ?

- **E-mail :** rrallvv@gmail.com
- **Délai de réponse :** sous 30 jours (généralement plus tôt)

Vous avez également le droit de déposer une plainte auprès de votre autorité locale de protection des données (par exemple, votre DPA d'État membre de l'UE, le procureur général de Californie ou la PIPC coréenne).

---

⚠️ **Avis de traduction** : Ceci est une traduction fournie à titre de commodité. En cas de divergence, la [version anglaise](../privacy.html) prévaudra.
