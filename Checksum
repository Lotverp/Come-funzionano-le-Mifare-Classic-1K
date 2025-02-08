# 🔍 **Che cos'è un Checksum?**

  

## 📌 Introduzione

Un **checksum** è un valore numerico usato per **verificare l'integrità dei dati** in trasmissione o memorizzazione.

È un tipo di **controllo degli errori** che consente di rilevare **dati corrotti** o modificati.

  

---

  

## 🔢 **Come funziona un checksum?**

Il checksum è calcolato applicando un **algoritmo matematico** ai dati originali.

Quando i dati vengono ricevuti o letti, viene ricalcolato lo stesso checksum e confrontato con il valore originale:

  

1️⃣ **Il mittente calcola il checksum sui dati e lo aggiunge**.

2️⃣ **Il destinatario ricalcola il checksum sui dati ricevuti**.

3️⃣ **Se i due valori coincidono**, i dati sono **corretti**.

4️⃣ **Se i due valori sono diversi**, i dati sono **corrotti o alterati**.

  

---

  

## 🔢 **Tipi di Checksum**

  

### **1️⃣ XOR Checksum (esempio del BCC in MIFARE Classic)**

Usa l'operazione **XOR** per combinare i dati.

📌 **Formula**:

```

Checksum = Byte_1 ⊕ Byte_2 ⊕ ... ⊕ Byte_N

```

✅ **Usato per controlli di integrità semplici**, come il **BCC nelle schede MIFARE Classic**.

  

---

  

### **2️⃣ Somma Modulo N (Modulo Checksum)**

Somma tutti i byte e prende il valore modulo **256** o altro valore prefissato.

📌 **Formula** (Modulo 256):

```

Checksum = (Byte_1 + Byte_2 + ... + Byte_N) mod 256

```

✅ **Usato in protocolli di comunicazione** come **XMODEM, TCP/IP**.

  

---

  

### **3️⃣ CRC (Cyclic Redundancy Check)**

Usa la divisione polinomiale per calcolare un valore di controllo.

📌 **Formula base**:

```

CRC = (Dati * Polinomio) mod Generatore

```

✅ **Usato in reti Ethernet, ZIP, e Bluetooth**.

  

---

  

## 🚀 **Esempio pratico di XOR Checksum**

Dati in esadecimale:

```

4E 21 3B 16

```

Calcoliamo il **XOR Checksum**:

```

4E ⊕ 21 ⊕ 3B ⊕ 16 = 42

```

✅ **Risultato finale: `42` (Esadecimale)**

  

---

  

## ⚠️ **Perché è importante il checksum?**

- 🔄 **Verifica l'integrità dei dati**.

- 🔒 **Rileva errori in trasmissione**.

- ⚠ **Non previene la manipolazione intenzionale dei dati**, ma aiuta a rilevarli.
