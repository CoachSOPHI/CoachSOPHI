# Coach Sophie - Intelligence Artificielle de Coaching Personnel

## 📚 Description
Coach Sophie est un coach virtuel alimenté par l'intelligence artificielle, conçu pour vous accompagner dans votre développement personnel. Grâce à des algorithmes avancés, Coach Sophie vous offre :

- **Des conseils personnalisés** : Adaptés à vos objectifs et à votre profil.
- **Un suivi intelligent** : Pour mesurer vos progrès et rester motivé.
- **Une assistance 24/7** : Un soutien constant, accessible à tout moment.
- **Une large gamme de sujets** : De la gestion du stress à la réalisation de soi.

## ✅ Fonctionnalités
- **Interaction via chat** : Discutez avec Coach Sophie pour obtenir des conseils personnalisés.
- **Planification de réunions Zoom** : Organisez des sessions de coaching en ligne.
- **Suivi des objectifs** : Définissez et suivez vos objectifs personnels.
- **Gestion des habitudes** : Suivez vos habitudes et recevez des recommandations.
- **Prise de décisions assistée** : Recevez des conseils pour vous aider à prendre de meilleures décisions.
- **Coaching en relations interpersonnelles** : Des recommandations pour améliorer vos relations sociales.
- **Transcription vocale** : Convertissez votre voix en texte pour interagir avec Coach Sophie.

## 🚀 Déploiement
Coach Sophie peut être déployé facilement sur **Render** en suivant ces étapes :
1. **Créer un dépôt GitHub** contenant le code source.
2. **Connecter Render à GitHub** et sélectionner le dépôt.
3. **Configurer l’environnement** sur Render :
   - Build Command : `pip install -r requirements.txt`
   - Start Command : `uvicorn main:app --host=0.0.0.0 --port=10000`
4. **Ajouter les variables d’environnement** :
   - `OPENAI_API_KEY`
   - `PINECONE_API_KEY`
   - `ZOOM_API_KEY`
   - `ZOOM_API_SECRET`
   - `SECURE_TOKEN`
5. **Lancer le déploiement et tester l’API**

## 🤖 Technologies Utilisées
- **[FastAPI](https://fastapi.tiangolo.com/)** : Framework web rapide pour l’API.
- **[OpenAI GPT-4](https://openai.com/)** : Modèle d’intelligence artificielle pour le traitement du langage.
- **[Pinecone](https://www.pinecone.io/)** : Base de données vectorielle pour la gestion du contexte.
- **[Zoom API](https://marketplace.zoom.us/)** : Intégration pour la planification de réunions.
- **[SpeechRecognition](https://pypi.org/project/SpeechRecognition/)** : Conversion de la voix en texte.

## 🚀 Utilisation
Une fois déployé, Coach Sophie peut être utilisé via des requêtes API :

### Exemples d’Endpoints
#### 1. **Tester l’API**
```sh
GET /health
```
Réponse attendue :
```json
{
  "status": "OK",
  "openai": true,
  "pinecone": true,
  "zoom": true
}
```

#### 2. **Interagir avec Coach Sophie**
```sh
POST /chat
```
Corps de la requête :
```json
{
  "user_id": "user_123",
  "message": "Comment améliorer ma productivité ?"
}
```
Réponse attendue :
```json
{
  "response": "Voici quelques conseils pour améliorer votre productivité..."
}
```

#### 3. **Planifier une réunion Zoom**
```sh
POST /schedule_zoom
```
Corps de la requête :
```json
{
  "topic": "Coaching personnel",
  "start_time": "2024-02-10T15:00:00Z",
  "duration": 60
}
```
Réponse attendue :
```json
{
  "meeting_url": "https://zoom.us/j/123456789",
  "meeting_id": "123456789"
}
```

## 🛠️ Contribuer
Les contributions sont les bienvenues !
1. **Forker le projet**
2. **Créer une branche (`git checkout -b feature-nouvelle-fonctionnalite`)**
3. **Commit (`git commit -m 'Ajout d'une nouvelle fonctionnalité'`)**
4. **Pousser (`git push origin feature-nouvelle-fonctionnalite`)**
5. **Créer une Pull Request**

## 🔒 Sécurité et Confidentialité
- Toutes les interactions sont sécurisées.
- Les données utilisateur ne sont pas partagées avec des tiers.
- Les tokens API doivent être stockés en variables d’environnement.

## 👤 Auteurs
- **[Ton Nom]** - Développeur principal

## 📊 Licence
Ce projet est sous licence **MIT**.

---

Vous avez des questions ? N’hésitez pas à ouvrir une issue sur GitHub ! 🚀


