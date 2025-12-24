# Basic MIDI Concepts and MIDI Devices

## 1. Introduction to MIDI

**MIDI (Musical Instrument Digital Interface)** is a **standard communication protocol** that allows electronic musical instruments, computers, and audio devices to **communicate musical information** with each other.

📌 **Important:**
MIDI **does not store actual sound**.
It stores **instructions** about how music should be played.

---

## 2. What MIDI Represents

Instead of audio waveforms, MIDI stores:

* Which **note** is played
* **When** it is played
* **How long** it is played
* **How loud** it is played
* Which **instrument** is used

This makes MIDI files **very small in size**.

---

## 3. Basic MIDI Concepts

### 3.1 MIDI Note

A **MIDI note** represents a musical pitch.

* Notes are numbered from **0 to 127**
* Each number corresponds to a musical note

Example:

* 60 → Middle C

---

### 3.2 Note On and Note Off

* **Note On**: Starts a note
* **Note Off**: Stops a note

Each Note On message contains:

* Note number
* Velocity

---

### 3.3 Velocity

**Velocity** represents how fast or hard a key is pressed.

* Range: **0–127**
* Affects loudness and expression

Higher velocity → louder sound

---

### 3.4 MIDI Channels

* MIDI supports **16 channels** (1–16)
* Each channel can control a different instrument

Example:

* Channel 1 → Piano
* Channel 10 → Drums (standard)

---

### 3.5 Program Change

A **Program Change message** selects an instrument sound.

Example:

* Program 1 → Piano
* Program 41 → Violin

(Exact sounds depend on the synthesizer.)

---

### 3.6 Control Change (CC)

Used to control sound parameters in real time.

Common Control Changes:

* Volume
* Pan (left/right balance)
* Sustain pedal
* Modulation

---

### 3.7 Pitch Bend

* Changes pitch smoothly up or down
* Used for vibrato or guitar-like effects
* Allows expressive performance

---

### 3.8 MIDI Timing

MIDI uses **ticks** instead of seconds.

* Timing is measured in **pulses per quarter note (PPQ)**
* Ensures precise synchronization between devices

---

## 4. Structure of a MIDI File

A MIDI file contains:

* Header chunk (format, number of tracks)
* One or more track chunks
* Sequence of MIDI messages

### MIDI File Formats

| Format | Description                  |
| ------ | ---------------------------- |
| Type 0 | Single track                 |
| Type 1 | Multiple synchronized tracks |
| Type 2 | Multiple independent tracks  |

---

## 5. Advantages of MIDI

* Very small file size
* Easy to edit (change tempo, key, instrument)
* Device-independent
* Low bandwidth requirement

---

## 6. Limitations of MIDI

* No actual sound stored
* Sound quality depends on synthesizer
* Not suitable for vocals or natural sounds

---

## 7. MIDI Devices

### 7.1 MIDI Controller

A **MIDI controller** sends MIDI messages but does not produce sound.

Examples:

* MIDI keyboard
* Drum pads
* Wind controllers

Functions:

* Sends Note On/Off
* Sends velocity and control data

---

### 7.2 MIDI Synthesizer

A **MIDI synthesizer** converts MIDI messages into actual sound.

Types:

* Hardware synthesizer
* Software synthesizer (VST instruments)

---

### 7.3 MIDI Interface

Connects MIDI devices to computers.

Examples:

* USB-MIDI interface
* Audio interface with MIDI ports

---

### 7.4 Sound Module

A sound module:

* Receives MIDI data
* Generates sound
* Has no keyboard

Used in studios and live performances.

---

### 7.5 Sequencer

A **MIDI sequencer** records, edits, and plays MIDI data.

Examples:

* DAWs (FL Studio, Cubase, Logic Pro)
* Hardware sequencers

---

## 8. MIDI Connections

### Traditional MIDI Ports

* MIDI IN
* MIDI OUT
* MIDI THRU

### Modern MIDI

* USB-MIDI
* Bluetooth MIDI

---

## 9. General MIDI (GM)

**General MIDI** is a standard that ensures:

* Consistent instrument mapping
* Standard drum layout
* Better compatibility

Key points:

* 128 standard instruments
* Channel 10 reserved for drums

---

## 10. MIDI Signal Flow

```
MIDI Controller
      ↓
MIDI Interface
      ↓
Computer / Sequencer
      ↓
Synthesizer / Sound Module
      ↓
Audio Output
```

---

## 11. MIDI vs Digital Audio

| Feature       | MIDI             | Digital Audio |
| ------------- | ---------------- | ------------- |
| Data stored   | Instructions     | Waveform      |
| File size     | Very small       | Large         |
| Sound quality | Device-dependent | Fixed         |
| Editing       | Easy             | Difficult     |
| Vocals        | Not supported    | Supported     |

---

## 12. Exam-Friendly Short Notes

* **MIDI**: A protocol that transmits musical performance data, not sound.
* **Velocity**: Measures how hard a key is pressed.
* **MIDI Channel**: Logical path for controlling instruments.
* **Synthesizer**: Converts MIDI data into sound.
* **Sequencer**: Records and edits MIDI events.

