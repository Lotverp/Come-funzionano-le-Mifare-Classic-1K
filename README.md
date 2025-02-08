
# ❓ Come funziona una **Mifare Classic 1K?**

## 🔍**Analizziamolo**  

Tramite il flipper zero o qualsiasi altro lettore nfc possiamo eseguire un dump, ovvero estrarre il contenuto di una tessera NFC, in questo caso, una MIFARE CLASSIC 1K.

## 🗜️Esempio
Ho eseguito un dump, tramite il mio flipper zero, questo è il contenuto del file .nfc
```
Filetype: Flipper NFC device
Version: 4
# Device type can be ISO14443-3A, ISO14443-3B, ISO14443-4A, ISO14443-4B, ISO15693-3, FeliCa, NTAG/Ultralight, Mifare Classic, Mifare Plus, Mifare DESFire, SLIX, ST25TB, EMV
Device type: Mifare Classic
# UID is common for all formats
UID: 4E 21 3B 16
# ISO14443-3A specific data
ATQA: 00 04
SAK: 08
# Mifare Classic specific data
Mifare Classic type: 1K
Data format version: 2
# Mifare Classic blocks, '??' means unknown data
Block 0: 4E 21 3B 16 42 08 04 00 62 63 64 65 66 67 68 69
Block 1: D5 09 01 02 00 01 00 00 00 00 00 42 00 F4 01 3A
Block 2: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 3: C1 52 67 B5 EB 39 FF 07 80 69 3E AD 98 4A 14 C6
Block 4: 0F 00 AA 00 C8 2C 01 28 9E 0F 0B 00 03 64 00 16
Block 5: 0F 00 AA 00 C8 2C 01 28 9E 0F 0B 00 03 64 00 16
Block 6: 0E 00 AA 00 C8 90 01 28 5E CF 0A 00 00 C8 00 59
Block 7: C1 52 67 B5 EB 39 FF 07 80 69 3E AD 98 4A 14 C6
Block 8: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 9: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 10: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 11: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 12: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 13: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 14: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 15: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 16: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 17: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 18: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 19: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 20: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 21: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 22: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 23: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 24: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 25: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 26: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 27: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 28: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 29: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 30: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 31: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 32: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 33: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 34: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 35: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 36: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 37: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 38: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 39: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 40: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 41: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 42: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 43: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 44: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 45: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 46: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 47: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 48: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 49: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 50: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 51: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 52: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 53: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 54: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 55: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 56: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 57: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 58: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 59: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
Block 60: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 61: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 62: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Block 63: FF FF FF FF FF FF FF 07 80 69 FF FF FF FF FF FF
```
  

## 🏗️ Struttura della MIFARE Classic 1K

- 📂 **Settori**:
	- Il flipper non ce lo mostra direttamente ma abbiamo:
	- 16 settori, ognuno composto da 4 blocchi.
	
	- **Ogni settore ha**:
	- 3 blocchi per i **dati** (es. blocchi 0-2, 4-6...)
	- 1 blocco [**trailer**](https://github.com/Lotverp/Come-funzionano-le-Mifare-Classic-1K/blob/main/chiave%20a-b.md) che contiene le chiavi di accesso e i permessi.

- ⛓️ **Blocchi**:
	- Ognuno dei 64 blocchi, **è composto da 16 byte**

  

---

  

## 🗃️ Analizziamo i vari settori:

  

### 🔹 **Settore 0 - Blocco 0 (UID e Dati di Sistema)**

```

Block 0: 4E 21 3B 16 42 08 04 00 62 63 64 65 66 67 68 69

```

🔑 **Dettagli**:

- 🆔 **Byte 0-3**: `4E 21 3B 16` → **UID** (Unique Identifier) del tag.
	- L' UID è un identificatore univoco assegnato a un dispositivo o a un oggetto per **distinguerlo dagli altri**.

- ✅ **Byte 4**: `42` → [**BCC**](https://github.com/Lotverp/Come-funzionano-le-Mifare-Classic-1K/blob/main/BCC) (Block Check Character), [checksum](https://github.com/Lotverp/Come-funzionano-le-Mifare-Classic-1K/blob/main/Checksum) per l'UID.

- 🛠️ **Byte 5-6**: `08 04` → Dati per il sistema ([SAK, ATQA](https://github.com/Lotverp/Come-funzionano-le-Mifare-Classic-1K/blob/main/sak-atqa.md)).

- 📄 **Byte 7-15**: `00 62 63 64 65 66 67 68 69` → Dati aggiuntivi.

  

---

  

### 📊 **Settore 0 - Blocco 1 (Dati)**

```

Block 1: D5 09 01 02 00 01 00 00 00 00 00 42 00 F4 01 3A

```

- 📝 Contiene dati utente senza struttura fissa.

  

---

  

### 📊 **Settore 0 - Blocco 2 (Dati)**

```

Block 2: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00

```

- 🔍 **Blocco vuoto**. Potrebbe essere utilizzato in futuro.

  

---

  

### 🔐 **Settore 0 - Blocco 3 (Trailer - Chiavi e Permessi)**

```

Block 3: C1 52 67 B5 EB 39 FF 07 80 69 3E AD 98 4A 14 C6

```

- Le schede **MIFARE Classic** usano un sistema di accesso basato su un [sistema di autenticazione a 2 chiavi](https://github.com/Lotverp/Come-funzionano-le-Mifare-Classic-1K/blob/main/chiave%20a-b.md), dove:
	- 🔑 **Key A**: `C1 52 67 B5 EB 39`

	- 🔒 **Access Bits**: `FF 07 80 69`

	- 🔑 **Key B**: `3E AD 98 4A 14 C6`

  

---

  

## 🔎 Osservazioni Generali

1. 🆔 **UID**: `4E 21 3B 16` è l'identificatore univoco.

2. 🔐 **Chiavi di Accesso**:

-  **Key A**: `C1 52 67 B5 EB 39`

-  **Key B**: `3E AD 98 4A 14 C6`

-  **Settori successivi**: chiavi predefinite.

3. 🔒 **Access Bits**: Permessi configurati per lettura/scrittura con **Key A** o **Key B**.

4. 📊 **Dati Utente**: Solo settori 0 e 1 contengono dati, gli altri sono vuoti.
