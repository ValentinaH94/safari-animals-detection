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

## 🔄 Versione 2 — In corso
Per migliorare le performance sulla classe zebra ho aggiunto 200 nuove immagini da [questo dataset](https://universe.roboflow.com/yolo-3vcdi/zebra-detection-jpe9a) e sto riaddestando il modello. Risultati in arrivo!

## 🛠️ Strumenti
- [Roboflow](https://roboflow.com)
- YOLOv8

## 📈 Stato
- 🟢 Versione 1 — completata (mAP 87,2%)
- 🟡 Versione 2 — in addestramento

## 📝 Note
Progetto didattico — sono ancora in fase di apprendimento. Qualsiasi feedback è benvenuto!
