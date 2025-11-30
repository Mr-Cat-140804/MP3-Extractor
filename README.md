# 🎧 MP3-Extractor (Spotify Metadata Tool)

MP3-Extractor is een open-source tool die muziek-informatie (metadata) verzamelt via de **officiële Spotify Web API**.  
Het doel van dit project is om snel en overzichtelijk **track-, playlist-, artiest- en audiofeature-gegevens** te kunnen exporteren zonder audio te downloaden of DRM te omzeilen.

Deze README is ontworpen om iedereen (ook beginners) duidelijk te maken wat het project doet, waarom het bestaat en hoe het gebruikt kan worden.

---

## 📚 Table of Contents
1. [Overzicht](#-overzicht)
2. [Waarom deze technologie?](#-waarom-deze-technologie)
3. [Hoe het proces werkt](#-hoe-het-proces-werkt)
4. [Repository Inhoud](#-repository-inhoud)
5. [Features](#-features)
6. [Installatie](#-installatie)
7. [Gebruik](#-gebruik)
8. [Motivatie](#-motivatie)
9. [Limitaties](#-limitaties)
10. [Challenges](#-challenges)
11. [Doel & Oplossing](#-doel--oplossing)
12. [Intended Use](#-intended-use)
13. [Credits](#-credits)
14. [Licentie](#-licentie)

---

## 📝 Overzicht
MP3-Extractor maakt het mogelijk om gestructureerde muziekgegevens te verzamelen uit Spotify, zoals:
- Track titles  
- Artiesten  
- Albums  
- Audio-analyse gegevens (tempo, energy, danceability, etc.)  
- Playlist inhoud  

Dit project is ideaal voor developers, onderzoekers, dataliefhebbers en iedereen die met muziekdata wil werken.

---

## 💡 Waarom deze technologie?
Spotify bevat één van de grootste uniforme databases van muziek ter wereld.  
Toegang tot deze metadata maakt het mogelijk om:

- Muziekdata te analyseren (bijv. BPM of genres)  
- Playlists te exporteren  
- Data-gedreven muziekprojecten te bouwen  
- Muziekonderzoek te doen  

De officiële Spotify Web API zorgt ervoor dat alles legaal en betrouwbaar gebeurt.

---

## ⚙️ Hoe het proces werkt
1. De gebruiker voert een Spotify playlist ID, track ID of artiest ID in.  
2. MP3-Extractor verstuurt een beveiligde aanvraag naar de Spotify Web API.  
3. De API stuurt metadata terug in JSON-formaat.  
4. Het script verwerkt de gegevens en exporteert ze naar:
   - JSON
   - CSV
   - TXT  
5. De gebruiker ontvangt een nette dataset die eenvoudig te analyseren is.

**Belangrijk:**  
Deze tool **downloadt geen MP3’s of audio**. Het verwerkt uitsluitend metadata.

---

## 📁 Repository Inhoud

```txt
/
├── src/
│   ├── api/
│   │   ├── spotifyClient.js       (API verbindingsmodule)
│   │   ├── fetchPlaylist.js       (Playlist data ophalen)
│   │   ├── fetchTrack.js          (Track metadata ophalen)
│   │   └── fetchArtist.js         (Artiest-info ophalen)
│   ├── utils/
│   │   ├── exportJSON.js          (JSON export)
│   │   ├── exportCSV.js           (CSV export)
│   │   └── exportTXT.js           (TXT export)
│   └── index.js                   (Hoofdbestand)
│
├── examples/
│   ├── sample_playlist.json
│   ├── sample_tracks.csv
│   └── sample_output.txt
│
├── .env.example                    (Voorbeeld environment config)
├── README.md                       (Dit document)
├── package.json                    (Project config)
└── LICENSE


===========================================
            MP3-Extractor Features
===========================================

[1] Playlist Metadata Extraction
    - Haalt alle nummers uit een Spotify-playlist op
    - Titel, artiest, album, duur, releasejaar

[2] Track Information Lookup
    - Zoek individuele tracks
    - Verkrijg volledige metadata
    - Inclusief albuminformatie en populariteit

[3] Artist Metadata Retrieval
    - Genres
    - Populariteit score
    - Top tracks van een artiest

[4] Audio Feature Analysis
    - Tempo (BPM)
    - Energy
    - Danceability
    - Valence
    - Loudness
    - Instrumentalness & meer

[5] Exporteren in Meerdere Formaten
    - JSON
    - CSV
    - TXT-lijsten

[6] Volledig Compliant met Spotify API
    - Geen MP3-download
    - Geen DRM-omzeiling
    - 100% legaal gebruik
