# safari-animals-detection
"Object detection su alcuni animali del Safari usando Roboflow e Yolov8-learning project"

# 🦒 Safari Animals — Object Detection con Roboflow

Progetto personale di computer vision, realizzato per esercitarmi con la piattaforma Roboflow mentre studio Machine Learning.

## 📌 Obiettivo
Addestrare un modello di object detection su immagini di animali safari, partendo da un dataset pubblico su Roboflow Universe, analizzarne i risultati e iterare per migliorare le performance.

## 🗂️ Dataset
- **Fonte:** [Safari Animals — Roboflow Universe](https://universe.roboflow.com/dog-pictures/safari-animals)
- **Immagini:** ~4100
- **Classi:** Giraffa, Impala, Lechwe, Tsessebe, Zebra, Elefante

## ⚙️ Workflow
1. Fork del dataset nel workspace personale
2. Esplorazione e revisione delle annotazioni
3. Data augmentation applicata:
   - Flip orizzontale
   - Variazione luminosità (±25%)
   - Crop casuale (0–20%)
   - Rumore (fino al 2%)
4. Training del modello tramite Roboflow

## 📊 Risultati — Versione 1

| Metrica | Valore |
|---|---|
| mAP@50 | 87,2% |
| Precisione | 92,8% |
| Richiamo | 86,4% |
| Soglia di confidenza ottimale | 31% |

### Confusion Matrix — Analisi per classe

| Classe | Rilevati | Falsi Negativi | Falsi Positivi | Valutazione |
|---|---|---|---|---|
| Giraffa | 95 | 6 | 0 | 🟢 Ottimo |
| Impala | 1202 | 161 | 131 | 🟡 Buono |
| Lechwe | 704 | 54 | 59 | 🟢 Buono |
| Tsessebe | 245 | 75 | 24 | 🟡 Da migliorare |
| Zebra | 883 | 334 | 133 | 🔴 Critico |
| Elefante | 898 | 55 | 31 | 🟢 Buono |

### Osservazioni
- ✅ Nessuna confusione tra classi — il modello classifica sempre correttamente
- 🔴 La zebra è la classe più problematica: 334 falsi negativi, probabilmente per via del pattern a strisce e della tendenza a stare in branco
- ⚠️ La giraffa è gravemente sottorappresentata (solo il 2,1% del dataset)

i risultati sono buoni,per poter ottimizzare al meglio qualche dato,in particolare la classe zebra,posso lavorare a una seconda versione!

## 🛠️ Strumenti
- [Roboflow](https://roboflow.com)
- YOLOv8

## 📈 Stato
- 🟢 Versione 1 — completata (mAP 87,2%)

## 📝 Note
Progetto didattico — sono ancora in fase di apprendimento. Qualsiasi feedback è benvenuto!
