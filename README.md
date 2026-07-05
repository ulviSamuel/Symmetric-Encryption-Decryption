# CifraturaDecifrSimmetrica

![Java](https://img.shields.io/badge/Java-Console%20Application-blue)
![Stato](https://img.shields.io/badge/Stato-Progetto%20didattico-orange)
![Ambito](https://img.shields.io/badge/Ambito-Crittografia-lightgrey)
![Algoritmo](https://img.shields.io/badge/Tipo-Cifratura%20simmetrica-green)

**CifraturaDecifrSimmetrica** è un progetto Java didattico dedicato alla simulazione di processi di **cifratura e decifratura simmetrica**.

L’applicazione mostra il funzionamento della crittografia simmetrica utilizzando una chiave condivisa per trasformare un testo in formato cifrato e ripristinarlo successivamente in chiaro.

---

## Indice

- [Descrizione](#descrizione)
- [Funzionalità](#funzionalità)
- [Obiettivo didattico](#obiettivo-didattico)
- [Tecnologie utilizzate](#tecnologie-utilizzate)
- [Struttura del progetto](#struttura-del-progetto)
- [Flusso logico](#flusso-logico)
- [Esecuzione del progetto](#esecuzione-del-progetto)
- [Note sul progetto](#note-sul-progetto)
- [Possibili miglioramenti futuri](#possibili-miglioramenti-futuri)
- [Autore](#autore)
- [Licenza](#licenza)

---

## Descrizione

Il progetto implementa un meccanismo di crittografia simmetrica in Java con l’obiettivo di:

- cifrare un messaggio in input;
- decifrare il messaggio cifrato con la stessa chiave;
- evidenziare il ciclo completo **testo in chiaro → testo cifrato → testo decifrato**.

È un progetto orientato all’apprendimento dei concetti base di sicurezza informatica e manipolazione delle stringhe.

---

## Funzionalità

L’applicazione permette di:

- inserire un testo da cifrare;
- inserire/impostare una chiave simmetrica;
- applicare una trasformazione di cifratura;
- visualizzare il testo cifrato;
- applicare la decifratura con la stessa chiave;
- verificare il ripristino del testo originale.

---

## Obiettivo didattico

Il progetto è pensato per comprendere in modo pratico:

- differenza tra testo in chiaro e testo cifrato;
- ruolo della **chiave condivisa** nella cifratura simmetrica;
- importanza della corretta gestione della chiave;
- logica di inversione tra cifratura e decifratura.

---

## Tecnologie utilizzate

- **Java** (100% del repository)
- Programmazione orientata agli oggetti (se applicata nella struttura)
- Applicazione da console (tipicamente in progetti didattici di questo tipo)

---

## Struttura del progetto

> Struttura indicativa (adattabile ai file reali presenti nel repository):

```text
CifraturaDecifrSimmetrica/
│
├── Main.java
├── Cifratura.java
├── Decifratura.java
├── Utility.java
└── README.md
```

Se vuoi, posso generarti una seconda versione del README con la **struttura file reale al 100%** leggendo direttamente il repository.

---

## Flusso logico

1. L’utente inserisce un messaggio.
2. L’utente fornisce la chiave simmetrica.
3. Il sistema cifra il testo.
4. Il sistema mostra l’output cifrato.
5. Il sistema decifra usando la stessa chiave.
6. Il sistema mostra il testo decifrato.

---

## Esecuzione del progetto

### Requisiti

- JDK installato (consigliato Java 8+)

### Compilazione

Dalla directory principale:

```bash
javac -d out $(find . -name "*.java")
```

### Avvio

```bash
java -cp out Main
```

> Se il package della classe principale è definito, usare il nome completo (es. `it.nome.progetto.Main`).

---

## Note sul progetto

Questo repository contiene un progetto a scopo didattico, utile per consolidare:

- gestione input/output;
- trasformazioni su stringhe/caratteri;
- modellazione di logiche reversibili (encrypt/decrypt);
- basi di crittografia simmetrica.

---

## Possibili miglioramenti futuri

- supporto a più algoritmi (es. Cesare, XOR, AES tramite librerie);
- gestione errori e validazioni avanzate;
- interfaccia grafica;
- test automatici (JUnit);
- esportazione risultati su file;
- modalità batch per cifrare più testi.

---

## Autore

Progetto realizzato da **Samuel Ulivi**.

---

## Licenza

Questo progetto è stato sviluppato per scopi didattici.
