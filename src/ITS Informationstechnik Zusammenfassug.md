# ITS Informationstechnik Zusammenfassung

---

## Zahlensysteme

---

Die Darstellung von Zahlenwerten durch geeignete Symbole.

### Begriffe

---

- **Zahlensystem**
  System zur Darstellung von Zahlen.
- **Zahlenwert**
  Wert einer Zahl die aus einem oder mehrerer Symbole in einem Zahlensystem dargestellt werden.
- **Ziffer / Symbol**
  Symbole sind visuelle Darstellung die in einem Zahlensystem genutzt werden um eine Zahl darzustellen.
- **Wertigkeit**
  Wert eines Symboles (Ist unter umständen Kontextabhängig).
- **Index (Indizes)**
  Kennzeichnet im Kontext vom Stellenwertsystem welche Basis verwendet wird bezogen auf eine Zahl.

### Römisches Zahlensystem (Additionssystem)

---

Symbole des Römischen Zahlensystems und ihre Wertigkeit:

| Symbol | Wertigkeit |
| ------ | ---------- |
| I      | 1          |
| V      | 5          |
| X      | 10         |
| L      | 50         |
| C      | 100        |
| D      | 500        |
| M      | 1000       | 

Es gibt Regeln zur Darstellung eines Zahlenwertes!

1. **Additionsregel**
  Steht ein Symbol rechts neben einem wertgleichen oder werthöheren Symbol, dann werden beide Symbolwerte addiert.
2. **Subtraktionsregel**
  Steht ein Symbol links neben einem werthöheren Symbol, dann wird der Symbolwert des linken Symbols vom rechten Symbolwert subtrahiert.
3. **Maximal drei gleiche Zeichen**

Wir nutzen das Römisches Zahlensystem nicht mehr, da bei großen Zahlen deutlich mehr Symbole / Ziffern verwendet werden müssen.

### Stellenwertsystem

---

Ein Stellenwertsystem oder polyadisches Zahlensystem ist ein Zahlensystem, dessen Zahlzeichen aus Ziffern besteht, deren jeweiliger Beitrag zum Gesamtwert der Zahl von ihrer Position innerhalb des Zahlzeichens abhängt.

#### Häufig verwendete Basen im Stellenwertsystem

---

|             | **Dezimal**       | **Binär**         | **Hexadezimal**      | **Oktal**         |
| ----------- | ----------------- | ----------------- | -------------------- | ----------------- |
| **Basis**   | 10                | 2                 | 16                   | 8                 |
| **Symbole** | 0123456789        | 01                | 0123456789ABCDEF     | 01234567          |
| **Indizes** | $Z_{10}$ $Z_d$ $Z_D$ | $Z_2$ $Z_b$ $Z_B$ | $Z_{16}$ $Z_h$ $Z_H$ | $Z_8$ $Z_o$ $Z_O$ |

#### Zahlenwert ermitteln

---

Beispiel mit einer Zahl ins Dezimalsystem $18,32$

| $b=10$          | $1$                             | $8$                 | $2$                 | $3$                   |
| --------------- | ------------------------------- | ------------------- | ------------------- | --------------------- |
| **Position**    | $2$                             | $1$                 | $-1$                 | $-2$                  |
| **Stellenwert** | $10^{2-1} = 10$                 | $10^{1-1} = 1$      | $10^{-1} = 0.1$    | $10^{-2} = 0.01$    |
| **Potenzwert**  | $1 \cdot 10 = 10$             | $8 \cdot 1 = 8$ | $3 \cdot 0.1 = 0.3$ | $2 \cdot 0.01 = 0.02$ |
| **Zahlenwert**  | $10 + 8 + 0.3 + 0.02 = 18,32$ |                     |                     |                       |

#### Bit & Byte

---

##### Bit

---

- Bits sind die kleinsten Einheiten von digitaler Information.
- Ein einzelnes Bit ist eine Abkürzung für "binary digit" (binäre Ziffer) und kann entweder den Wert 0 oder 1 haben.

##### Bytes

<table>
  <tr>
    <th>Bit 7</th>
    <th>Bit 6</th>
    <th>Bit 5</th>
    <th>Bit 4</th>
    <th>Bit 3</th>
    <th>Bit 2</th>
    <th>Bit 1</th>
    <th>Bit 0</th>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
    <td>0</td>
    <td>1</td>
    <td>1</td>
    <td>0</td>
    <td>0</td>
    <td>1</td>
  </tr>
  <tr>
    <td>MSB</td>
    <td colspan="6"></td>
    <td>LSB</td>
  </tr>
  <tr>
    <td colspan="4">Nibble 1</td>
    <td colspan="4">Nibble 0</td>
  </tr>
  <tr>
    <td colspan="8">Byte</td>
  </tr>
</table>


- Bytes sind eine Gruppierung von Bits.
- Ein Byte besteht aus 8 Bits.
- $2^8 = 256$ mögliche Kombinationen.

##### Gesamtformel zum ermitteln des Zahlenwertes

---

# $\color{gray}\sum\limits_{\color{#7a59ff}n\color{gray}=1}^{\color{#59ff59}m} \color{#ff5959}x\color{gray}_{\color{#7a59ff}n} \cdot \color{#5996ff}b\color{gray}^{\color{#7a59ff}n\color{gray}-1} + \sum\limits_{\color{#7a59ff}n\color{gray}=1}^{\color{#ffd659}k} \color{#ff5959}x\color{gray}_{-\color{#7a59ff}n} \cdot \color{#5996ff}b\color{gray}^{-\color{#7a59ff}n}$

$\color{#ff5959}x\color{gray}=$ Zahlenwert des Symboles
$\color{#5996ff}b\color{gray}=$ Basis des Zahlensystems
$\color{#59ff59}m\color{gray}=$ Anzahl der Symbole vor dem Komma
$\color{#ffd659}k\color{gray}=$ Anzahl der Symbole nach dem Komma
$\color{#7a59ff}n\color{gray}=$ Iterator des Summenzeichen

### Umwandeln von Zahlensystemen

---

**Formel:**

$\color{gray}f(\color{#ff5959}x\color{gray}, \color{#5996ff}b\color{gray}) = \color{#ffd659}r\color{gray}_{\color{#59ff59}k}, ..., \color{#ffd659}r\color{gray}_2, \color{#ffd659}r\color{gray}_1$ wobei $\color{#ffd659}r\color{gray}_{\color{#7a59ff}i} = \color{#ff5959}x\color{gray} \mod \color{#5996ff}b\color{gray}^{\color{#7a59ff}i\color{gray}-1}$

**Beispiel:**

Wandle die Zahl $637_{10}$ in eine Binärzahl um:

$637 \div 2 = 318\quad r_1 = 1$
$318 \div 2 = 159 \quad r_2 = 0$
$159 \div 2 = 79 \quad r_3 = 1$
$79 \div 2 = 39 \quad r_4 = 1$
$39 \div 2 = 19 \quad r_5 = 1$
$19 \div 2 = 9 \quad r_6 = 1$
$9 \div 2 = 4 \quad r_7 = 1$
$4 \div 2 = 2 \quad r_8 = 0$
$2 \div 2 = 1 \quad r_9 = 0$
$1 \div 2 = 0 \quad r_{10} = 1$

Das Ergebnis in Binärform lautet: $1001111101_2$

## 2er Komplement Darstellung

---

Methode, um negative Zahlen in Binärform darzustellen.

### Umwandeln

| 1.  | Anfangszahl   | $00010010 = 18$  |
| --- | ------------- | ---------------- |
| 2.  | Invertieren   | $11101101$       |
| 3.  | $+1$ Addieren | $11101110 = -18$ |

Wenn man die 18 nun mit der -18 Addiert erhält man Null.

**Beispiel Zweierkompliment zu Dezimalzahl:**

| Zweierkompliment | Rechenweg  | Dezimalzahl | 
| ---------------- | ---------- | ----------- |
| $10001101_2$     | -128+8+4+1 | -115        |

### Zusätzliche Informationen

- Das MSB ist das Vorzeichenbit. 1 gleich negativ und 0 gleich positiv.
- Bei Hexadezimalen Zahlen ist es positiv von 0 - 7 und negativ von 8 - F.
- Anzahl der gegeben Bits bestimmt den Wertebereich.
    
**Beispiel:**
    
8-Bit-Zahl kann Werte zwischen -128 und +127 darstellen.
    
- Die asymmetrische Verteilung der Werte liegt an der 0.

## Rechnen mit Binärzahlen

---

### Addition

---

| A | B | Übertrag (C_in) | Summe (S) | Übertrag aus (C_out) |
|---|---|-----------------|-----------|----------------------|
| 0 | 0 |        0        |     0     |          0           |
| 0 | 1 |        0        |     1     |          0           |
| 1 | 1 |        0        |     0     |          1           |
| 0 | 1 |        1        |     0     |          1           |
| 1 | 1 |        1        |     1     |          1           |

### Subtraktion

---

| A | B | Borrow_in (C_in) | Differenz (D) | Borrow_out (C_out) |
|---|---|------------------|----------------|--------------------|
| 0 | 0 |        0         |       0        |         0          |
| 0 | 0 |        1         |       1        |         1          |
| 0 | 1 |        0         |       1        |         1          |
| 0 | 1 |        1         |       0        |         1          |
| 1 | 0 |        0         |       1        |         0          |
| 1 | 0 |        1         |       0        |         0          |
| 1 | 1 |        0         |       0        |         0          |
| 1 | 1 |        1         |       1        |         1          |

### Zweierkompliment

---

Nutze einfach die Additionsregel und nutze als Datentyp für die Summanden und für die Summe das Zweierkompliment.

## Codes

---

Codes sind Daten in einem bestimmten Format. Die Regeln die dieses Format bilden nennt man Syntax.

### Codieren

---

Daten in ein bestimmtes Format formatieren.

### Decodieren

---

Daten aus einem Format formatieren.

## Semiotik

---

Semiotik in der Informatik befasst sich damit, wie Daten (rohe Fakten oder Symbole) durch Syntax (Regeln und Strukturen) in Informationen (Bedeutungen) umgewandelt werden, die dann durch Semantik (Bedeutung und Interpretation) verstanden werden können.

Hier ein Beispiel:

> Wenn eine Reihe von Nullen und Einsen (Daten) gemäß der Syntax einer Programmiersprache angeordnet wird, um einen Algorithmus (Information) zu erstellen, der eine bestimmte Aufgabe erfüllt, und die Semantik wird verwendet, um den Algorithmus zu verstehen und seine Auswirkungen zu interpretieren.

### Daten

---

Sind einfache Zustände der Realität.

#### Syntax

---

Regeln für die Formatierung von Daten.

### Informationen

---

Ergibt sich aus interpretation von Daten.

#### Semantik

---

Interpretation von Daten.

## Wissen

---

Wissen entsteht wenn man mehrere Informationen in Kontext setzt.

## Code-Arten

---

### Numerische Codes

---

Numerische Codes codieren Ziffern. Angewendet werden sie beim Zählen und Rechnen, zur Codierung von Postleitzahlen oder Artikelnummern in Warenhäusern.

### Alphanumerische Codes

---

Alphanumerische Codes codieren neben Ziffern auch die Buchstaben des Alphabets und Steuerzeichen.

### Leitungscodes

---

Leitungscodes dienen zur Umwandlung von binären Signalen in Digitalsignale, die für das Übertragungsmedium (z.B. Kupferleitung) am besten geeignet sind.

## BCD CODE

BCD-Code Neben der Dualcodierung wird in der Informationstechnik auch der BCD-Code zur Darstellung von Ziffernfolgen genutzt. Dabei steht BCD für Binary Coded Decimals (Binär codierte Dezimalzahlen). Im BCD-Code wird jede Dezimalziffer durch 4 Bit der entsprechenden dualen Zahl dargestellt. Häufig zum Einsatz kommt dabei der 8-4-2-1-BCD-Code, dieser wird auch als Natural Binary-Coded Decimal (NBCD) bezeichnet.
Die Codewörter der BCD-Codes werden auch als Tetraden bezeichnet. Von den 16 möglichen Tetraden werden zur Darstellung der zehn Dezimalziffern jeweils sechs Tetraden nicht verwendet. Diese werden Pseudotetraden oder Pseudodezimale genannt.

## ASCII-Code

Codierung um Zeichen darzustellen.

- In ASCII ist 1 Zeichen = 1 Byte
- Beinhaltet 128 Zeichen (Beim erweiterten 256)
- Das 8te Bit wird als Paritätsbit verwendet

### Unicode

---

Unicode ist eine Globale Standard Formatierung für Zeichen nach ISO10646.

## UTF-8

---

- Die Binäre Codierung des Unicodes ist in UTF (Unicode Transformation Format).
- Ermöglicht durch eine dynamische Größe zwischen 1 - 4 Bytes je nachdem, welche Zeichen verwendet werden, effizient mehr als 256 Zeichen zu verwenden.