# 🔐 **Sistema di Accesso nelle MIFARE Classic - Trailer Block**

  

## 📌 Introduzione

Le schede **MIFARE Classic** usano un sistema di accesso basato su **chiavi segrete** e **bit di accesso**.
Ogni settore ha un **blocco trailer** che controlla la lettura, scrittura e autenticazione.

  

Esempio di **Blocco Trailer (Settore 0, Blocco 3):**

```

Block 3: C1 52 67 B5 EB 39 FF 07 80 69 3E AD 98 4A 14 C6

```

Struttura del blocco:

-  **Key A (6 byte)** → `C1 52 67 B5 EB 39`

-  **Access Bits (4 byte)** → `FF 07 80 69`

-  **Key B (6 byte)** → `3E AD 98 4A 14 C6`

  

---

  



# 🏗️ **Struttura del Blocco Trailer**

  

Il **Blocco Trailer** è composto da **16 byte** organizzati nel seguente modo:





| Byte | Contenuto |
|-------|--------------------------------|
| 0-5 | **Key A (6 byte)** 🔑 | 
| 6-9 | **Access Bits (4 byte)** 📋 | 
| 10-15 | **Key B (6 byte)** 🔑 *(opzionale)* |



  

---

  

### 📌 **Esempio di Blocco Trailer**

  

```mathematica

C1 52 67 B5 EB 39 FF 07 80 69 3E AD 98 4A 14 C6

```

  

### 📌 **Dove:**

-  **Byte 0-5** → `C1 52 67 B5 EB 39` = **Key A** 🔑

-  **Byte 6-9** → `FF 07 80 69` = **Access Bits** 📋

-  **Byte 10-15** → `3E AD 98 4A 14 C6` = **Key B** 🔑

  

>  **Nota:** Se **Key B** non viene utilizzata, può essere sovrascritta con dati di sistema.

---

  

## 🔑 **Chiavi di Accesso (Key A e Key B)**

- La **Key A** viene solitamente usata per **autenticare** e leggere dati.

  

- La **Key B** può essere usata per scrivere dati o specificare permessi avanzati.

  
  

📌 **Esempio di chiavi nel dump NFC:**

  

```

Key A: C1 52 67 B5 EB 39

Key B: 3E AD 98 4A 14 C6

```

Se le chiavi non sono note, il sistema rifiuta l'accesso ai dati.

  

---

  

## 🔢 **Bit di Accesso (Access Bits)**

Gli **Access Bits** sono 4 byte che determinano i permessi di lettura e scrittura per i blocchi del settore.

  

📌 **Esempio di Access Bits:**

  

```

FF 07 80 69

```

Formato:

  

```

C1 C2 C3 | C1 C2 C3 | C1 C2 C3 | C1 C2 C3 | 00000000

```

Dove:

  

-  **C1, C2, C3** determinano le regole di accesso per ogni blocco.

  

-  **Il byte finale è sempre `00000000` per sicurezza.**

  

### 📊 **Tabella dei Permessi**

  

| Accesso  | Solo Key A |  Solo Key B |
|--|--|--|
| **Leggere Dati** | ✅ Sì | ✅ Sì |
| **Scrivere Dati** | ❌ No | ✅ Sì |
| **Cambiare Chiavi** | ❌ No | ✅ Sì |


  

---

  

## 🚀 **Conclusione**

- 🔐 **Key A e Key B** proteggono i dati del settore.

  

- 📋 **Access Bits** determinano i permessi per lettura e scrittura.

  

- ⚠️ **Attenzione**: Le chiavi predefinite (`FF FF FF FF FF FF`) sono vulnerabili agli attacchi!
