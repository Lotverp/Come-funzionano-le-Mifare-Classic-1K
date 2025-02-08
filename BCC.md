# 🔍 Che cos'è il BCC (Block Check Character)

  

## 📌 Introduzione

Il **BCC (Block Check Character)** è un **byte di controllo** usato per garantire l'integrità dell'UID in una scheda **MIFARE Classic**.

Si trova nel **Settore 0, Blocco 0**, subito dopo i byte dell'UID.

  

---

  

## 📂 **Dove si trova il BCC?**

Il BCC è posizionato nel **byte 4** del **Blocco 0** nel **Settore 0** della scheda.

Esempio di **Blocco 0** da un dump NFC:

  

```

Block 0: 4E 21 3B 16 42 08 04 00 62 63 64 65 66 67 68 69

```

  

Qui:

-  **UID** = `4E 21 3B 16` (4 byte)

-  **BCC** = `42` (1 byte, subito dopo l'UID)

-  **Byte 5-6** = `08 04` (ATQA e SAK)

-  **Byte 7-15** = Altri dati

  

---

  

## 🔢 **Come si calcola il BCC?**

Il **BCC** è calcolato facendo un'operazione **XOR** tra tutti i byte dell'UID.

  

📌 **Formula:**

```

BCC = UID_0 ⊕ UID_1 ⊕ UID_2 ⊕ UID_3

```

Dove:

-  `⊕` indica l'operazione **XOR** (OR esclusivo)

-  `UID_0, UID_1, UID_2, UID_3` sono i primi quattro byte dell'UID

  

---

  

## ✏️ **Esempio di calcolo del BCC**

Consideriamo questo UID:

```

UID = 4E 21 3B 16

```

Calcoliamo lo XOR tra i byte:

```

4E ⊕ 21 ⊕ 3B ⊕ 16

```

Convertiamo in binario:

```

4E = 01001110

21 = 00100001

3B = 00111011

16 = 00010110

```

Ora facciamo **XOR** passo dopo passo:

```

01001110

⊕ 00100001

------------

01101111

⊕ 00111011

------------

01010100

⊕ 00010110

------------

01000010 (42 in esadecimale)

```

✅ **Risultato finale: `42` (BCC corretto)**

  

---

  

## ⚠️ **Perché il BCC è importante?**

- 🔄 **Verifica l'integrità dell'UID**: Se l'UID è stato alterato, il BCC sarà errato.

- 🔒 **Protezione base contro la corruzione dei dati**.

- 🚨 **Schede clonate** possono avere BCC errato se l'UID viene modificato manualmente.

  

---

  

## 🚀 **Conclusione**

Il **BCC** è un checksum di **1 byte** usato per controllare la correttezza dell'UID, calcolato con un'operazione **XOR** tra i primi 4 byte dell'UID. Se viene alterato, indica che i dati dell'UID potrebbero essere stati modificati.
