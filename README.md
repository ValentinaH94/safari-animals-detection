# safari-animals-detection
"Object detection su alcuni animali del Safari usando Roboflow e Yolov8-learning project"


# 🦒 Safari Animals — Object Detection con Roboflow

Primo progetto personale di computer vision, fatto per esercitarmi con la piattaforma Roboflow mentre studio Machine Learning.

## 📌 Obiettivo
Addestrare un modello di object detection su immagini di animali safari, partendo da un dataset pubblico su Roboflow Universe.

## 🗂️ Dataset
- **Fonte:** [Safari Animals — Roboflow Universe](https://universe.roboflow.com/dog-pictures/safari-animals)
- **Immagini:** ~4100
- **Classi:** Elefante, Giraffa, Zebra, Impala

## ⚙️ Workflow
1. Fork del dataset nel workspace personale
2. Esplorazione e revisione delle annotazioni
3. Data augmentation applicata:
   - Flip orizzontale
   - Variazione luminosità (±25%)
   - Crop casuale (0–20%)
   - Rumore (fino al 2%)
4. Training del modello tramite Roboflow

## 🛠️ Strumenti
- [Roboflow](https://roboflow.com)
- YOLOv8

## 📈 Stato
🟡 Modello in addestramento...

## 📝 Note
Progetto didattico — sono ancora in fase di apprendimento. Qualsiasi feedback è benvenuto!
