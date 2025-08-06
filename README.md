# 🎼 AI Music Generator with LSTM using MIDI Files

This project demonstrates how to generate music using an LSTM model trained on MIDI data. The model predicts the next note (pitch, duration, and step) based on sequences of notes from real MIDI files.

---

## 📌 Features

- Converts MIDI files to structured training data
- Trains a multi-output LSTM model to predict future notes
- Generates new music note-by-note
- Saves and plays generated music as a `.mid` file

---


---

## 🚀 How It Works

1. **MIDI to Notes Conversion**  
   Parses MIDI files into pitch, step (time since last note), and duration.

2. **Sequence Generation**  
   Builds fixed-length input sequences and corresponding targets.

3. **Model Architecture**  
   LSTM-based model with three outputs:
   - `pitch` (classification)
   - `step` (regression)
   - `duration` (regression)

4. **Training**  
   Compiles and trains using custom loss weights for each output.

5. **Music Generation**  
   Generates music by predicting the next note iteratively.

6. **Output**  
   Saves the generated notes into a playable `.mid` file using PrettyMIDI.

---

## 🛠️ Dependencies

Install the following Python packages:

```bash
pip install pretty_midi
pip install numpy pandas tensorflow
apt-get install -y fluidsynth
pip install pyfluidsynth


