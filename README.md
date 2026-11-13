# AstroCapture - The Astronomical Motion Detection System
<p>AstroCapture est un logiciel d'observation automatique du ciel.</p> 
<p>Il propose la surveillance et la capture automatique d'évènements du ciel, au travers de caméras PoE.</p> 
<p>Le logiciel est développé pour fonctionner sur Windows uniquement (pour le moment).</p> 
<p>J'ai décidé de développer ce logiciel après avoir testé plusieurs équivalents qui de mon point de vue manquaient de fonctionnalités ou avaient des problèmes de stabilité.</p> 


Base Windows WPF pour l'acquisition vidéo multi-caméras.
Prérequis
Windows 10/11 64 bits
.NET 10 SDK
Visual Studio 2026 avec la charge de travail « Développement .NET Desktop » (ou VS Code + SDK)
Lancer
Depuis le dossier `AstroCapture` :
```powershell
dotnet restore
dotnet build
dotnet run
```
<p>Ajouter une source RTSP : saisir l'URL complète, par exemple `rtsp://192.168.1.100:554/stream1`</p>
<p>USB : sélectionner « Caméra USB » et saisir `0` (première caméra), `1` (deuxième), etc.</p>

<p>A l'instant, ce logiciel est un prototype d'acquisition/affichage, pas encore un détecteur.</p>
<p>La disponibilité RTSP/H.264/H.265 dépend du backend FFmpeg embarqué et du flux de la caméra.</p>
<p>La gestion des identifiants RTSP est laissée à l'URL pour ce prototype ; ne partage pas une URL contenant un mot de passe.</p>
<p>Le bouton d'ajout ajoute une tuile ; la suppression individuelle et la reconnexion automatique seront ajoutées ensuite.</p>
<p>L'interface multi-caméras est volontairement simple à ce stade.</p>
