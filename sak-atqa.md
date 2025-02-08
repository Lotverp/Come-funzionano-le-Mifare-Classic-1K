# 🔍 Che cosa sono SAK e ATQA nelle schede MIFARE?

  

## 📌 Introduzione

Le schede **MIFARE Classic** e altre schede RFID/NFC usano due parametri fondamentali per identificarsi nel processo di comunicazione con un lettore NFC:

  

1.  **ATQA (Answer To Request Type A)** → Fornisce informazioni generali sul tipo di scheda.

2.  **SAK (Select Acknowledge)** → Aiuta il lettore NFC a determinare il tipo specifico della scheda.

  

Questi parametri sono usati durante la fase di **anticollisione e selezione del tag**.

  

---

  

## 🏗️ **Che cos'è l'ATQA?**

L'**ATQA (Answer To Request Type A)** è un codice di **2 byte** che la scheda NFC invia in risposta a una richiesta **REQA (Request Type A)** da parte del lettore.

Questo valore indica il tipo di scheda e le sue funzionalità.

  

📌 **Esempio di ATQA nel dump NFC:**

```

Byte 5-6: 08 04 → ATQA = 0x0408

```

  

### 📊 **Valori comuni di ATQA**

| ATQA (Hex) | Tipo di Scheda |

---------------------------

| `0x0004` | MIFARE Classic 1K |

| `0x0002` | MIFARE Ultralight |

| `0x0044` | MIFARE DESFire |

  

---

  

## 🔑 **Che cos'è il SAK?**

Il **SAK (Select Acknowledge)** è un **byte di risposta** inviato dalla scheda NFC dopo la fase di anticollisione.

Aiuta il lettore a determinare la categoria e le funzionalità della scheda.

  

📌 **Esempio di SAK nel dump NFC:**

```

Byte 7: 08 → SAK = 0x08

```

  

### 📊 **Valori comuni di SAK**

| SAK (Hex) | Tipo di Scheda |

--------------------------

| `0x08` | MIFARE Classic 1K |

| `0x18` | MIFARE Classic 4K |

| `0x20` | MIFARE Plus |

| `0x28` | MIFARE DESFire |

  

---

  

## 🔄 **Come funzionano ATQA e SAK nel processo NFC?**

1️⃣ **Il lettore NFC invia REQA (Request Type A).**

2️⃣ **La scheda risponde con ATQA**, fornendo informazioni generali.

3️⃣ **Il lettore avvia la fase di anticollisione e selezione.**

4️⃣ **La scheda invia il valore SAK**, indicando il suo tipo esatto.

5️⃣ **Il lettore può ora autenticare la scheda** e accedere ai dati.

  

---

  

## 🚀 **Conclusione**

-  **ATQA** aiuta a identificare la categoria della scheda.

-  **SAK** specifica il modello e le funzionalità.

- Sono usati nel processo di **anticollisione e autenticazione**.

 