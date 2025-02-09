# 🔐 Operatore XOR (Exclusive OR)

## 🧐 Introduzione a XOR
L'operatore **XOR** (Exclusive OR) è un'operazione logica fondamentale in informatica, elettronica e crittografia. A differenza dell'operatore OR (`A OR B`), che restituisce `1` se almeno uno degli ingressi è `1`, XOR restituisce `1` solo se gli ingressi sono **diversi**.

In altre parole:
- Se **entrambi gli ingressi sono uguali**, il risultato è `0` ❌.
- Se **gli ingressi sono diversi**, il risultato è `1` ✅.

## 📜 Tavola della Verità di XOR
| A | B | A ⊕ B | Spiegazione |
|---|---|------|-------------|
| 0 | 0 |  0   | Entrambi gli ingressi sono uguali ❌ |
| 0 | 1 |  1   | Gli ingressi sono diversi ✅ |
| 1 | 0 |  1   | Gli ingressi sono diversi ✅ |
| 1 | 1 |  0   | Entrambi gli ingressi sono uguali ❌ |

### 🛠 Costruzione di XOR con altri operatori logici:
L'operatore XOR può essere espresso come:
\[
A ⊕ B = (A \lor B) \land 
eg(A \land B)
\]
In termini di **porte logiche**, possiamo scomporlo in:

1. **OR**: A + B (se almeno uno è 1 → 1)
2. **AND**: A * B (se entrambi sono 1 → 1)
3. **NOT** dell'AND: ¬(A * B)
4. **AND tra OR e NOT(AND)**: (A + B) * ¬(A * B)

## 🖥️ XOR nei Linguaggi di Programmazione
Molti linguaggi di programmazione supportano XOR tramite l'operatore `^`. Esempi:

### 🐍 XOR in Python:
```python
a = 5  # 101 in binario
b = 3  # 011 in binario

result = a ^ b  # 110 in binario, cioè 6 in decimale
print(result)  # Output: 6
```

### 💻 XOR in C:
```c
#include <stdio.h>

int main() {
    int a = 5, b = 3;
    int result = a ^ b;
    printf("%d\n", result);  // Output: 6
    return 0;
}
```

### 🚀 XOR in JavaScript:
```javascript
let a = 5; // 101
let b = 3; // 011

let result = a ^ b; // 110 (6 in decimale)
console.log(result); // Output: 6
```

## ✨ Applicazioni Pratiche di XOR

### 🔐 1. Crittografia XOR
XOR è usato nei cifrari a flusso per crittografare i dati. Se hai un messaggio `M` e una chiave `K`, puoi cifrare con:
\[
C = M ⊕ K
\]
e decifrare con lo stesso XOR:
\[
M = C ⊕ K
\]

Esempio in Python:
```python
def xor_cipher(message, key):
    return ''.join(chr(ord(m) ^ ord(key[i % len(key)])) for i, m in enumerate(message))

message = "Hello"
key = "key"

encrypted = xor_cipher(message, key)
decrypted = xor_cipher(encrypted, key)

print(f"Cifrato: {encrypted}")
print(f"Decifrato: {decrypted}")  # Ritorna "Hello"
```

### 📡 2. Controllo di Parità e Error Detection
XOR viene utilizzato nei checksum e nei codici di rilevamento degli errori, come il **Codice di Hamming** e il **CRC**.

### 🔄 3. Scambio di Variabili senza Variabile Temporanea
```python
a = 10
b = 20

a = a ^ b
b = a ^ b
a = a ^ b

print(a, b)  # Output: 20, 10
```
Questo metodo utilizza XOR per scambiare due numeri senza l'uso di una variabile temporanea, ottimizzando la memoria.

### ⚡ 4. Verifica di Unicità in un Array
Dato un array in cui tutti gli elementi appaiono due volte tranne uno, possiamo trovare l'elemento unico con XOR:
```python
arr = [4, 3, 2, 4, 1, 3, 2]
unique = 0
for num in arr:
    unique ^= num

print(unique)  # Output: 1
```
Ogni numero che appare due volte si annulla con XOR, lasciando solo il numero unico!

## 🔎 Proprietà Matematiche di XOR
- **Auto-annullamento**: \( A ⊕ A = 0 \)  
- **Identità**: \( A ⊕ 0 = A \)  
- **Commutativa**: \( A ⊕ B = B ⊕ A \)  
- **Associativa**: \( (A ⊕ B) ⊕ C = A ⊕ (B ⊕ C) \)  
- **Inversione**: \( A ⊕ 1 = 
eg A \) (inverti i bit)

## 🧠 XOR e Algebra di Boole
Nell'algebra booleana, XOR è indicato con il simbolo **⊕** e segue regole precise per la manipolazione delle espressioni logiche.

Ad esempio:
\[
(A ⊕ B) ⊕ C = A ⊕ (B ⊕ C)
\]
Ciò significa che possiamo riordinare gli XOR senza cambiare il risultato!

## 📌 Conclusione
L'operatore XOR è una delle operazioni logiche più potenti, con applicazioni in crittografia, calcolo distribuito, elaborazione di dati e intelligenza artificiale. 🎯

🔹 XOR è usato nei circuiti logici, nella programmazione, nei checksum, nella sicurezza informatica e persino nei giochi!  
🔹 La sua capacità di invertire i bit lo rende una scelta eccellente per molti algoritmi di elaborazione dati.  
🔹 Comprendere XOR può migliorare la tua capacità di scrivere codice più efficiente e sicuro! 🚀

---

🔗 **Risorse Utili**
- [Wikipedia XOR](https://en.wikipedia.org/wiki/Exclusive_or)
