# db-challenge

## Gestione Biblioteca
### Diagramma E/R
<img width="1278" height="824" alt="Screenshot 2025-11-15 122215" src="https://github.com/user-attachments/assets/281f7ae8-9daf-4d4f-b9e7-d9138e6e5829" />
Questo modello è stato progettato per rappresentare la gestione di una biblioteca.
Le entità principali individuate sono: libri, autori, categorie e utenti.

Dal punto di vista delle relazioni, un libro può avere zero o più prestiti, può appartenere a una o più categorie e può essere associato a uno o più autori. Gli utenti, invece, possono effettuare da zero a più prestiti.

Le tabelle libri, autori e categorie contengono tutte le informazioni descrittive relative al catalogo, mentre la tabella utenti registra i soggetti che possono richiedere o hanno già richiesto un prestito.

La tabella prestiti collega un libro a un utente registrando la data del prestito, permettendo così di creare uno storico completo delle operazioni: in questo modo è possibile sapere quale utente ha preso in prestito un determinato libro e in quale data e ora.


## Gestione Food Delivery
### Diagramma E/R
<img width="1271" height="836" alt="Screenshot 2025-11-15 150529" src="https://github.com/user-attachments/assets/7fb12795-5f33-464c-ab7e-862818b8002d" />
Questo modello è stato progettato per rappresentare la gestione di un sistema di food delivery.
Le entità principali individuate sono: piatti, ristoranti, clienti, ordini e consegne.

Dal punto di vista delle relazioni, un ristorante può offrire uno o più piatti e un piatto può essere proposto da più ristoranti: per questo è stata introdotta la tabella associativa ristorante_piatto, che permette anche di memorizzare informazioni specifiche come il prezzo e la disponibilità del piatto in quel ristorante.

I clienti possono effettuare da zero a più ordini. Ogni ordine è collegato a un singolo ristorante e può contenere uno o più piatti, gestiti dalla tabella dettaglio_ordine, che registra quantità e prezzo unitario per ciascun piatto ordinato.

La tabella consegne è collegata uno-a-uno con gli ordini e contiene informazioni relative alla spedizione, come indirizzo, orario stimato e stato della consegna.

L’intero modello consente di tracciare in modo preciso le offerte dei ristoranti, gli ordini dei clienti e lo stato delle consegne, garantendo integrità dei dati e uno storico completo delle operazioni.


## Gestione Eventi
### Diagramma E/R
<img width="1015" height="743" alt="Screenshot 2025-11-15 163149" src="https://github.com/user-attachments/assets/e5a044ba-e4a2-4ce9-b323-f32080da8b4f" />
Questo modello rappresenta un sistema di gestione eventi. 
Le entità principali individuate sono: eventi, partecipanti, sponsors, locations e biglietti.

La tabella eventi contiene le informazioni fondamentali su ogni evento (nome, descrizione, date, capienza), mentre locations memorizza i luoghi in cui questi vengono svolti. La tabella partecipanti rappresenta gli utenti che possono partecipare agli eventi, mentre sponsors raccoglie i soggetti che finanziano o supportano gli eventi.

La tabella biglietti collega direttamente partecipanti ed eventi, rappresentando ogni iscrizione o accesso. PS: Aggiungere il campo prezzo di tipo decimal dentro la tabella "Biglietto".


## Gestione Cinema
### Diagramma E/R
<img width="1026" height="736" alt="Screenshot 2025-11-15 165540" src="https://github.com/user-attachments/assets/127e1c5c-0434-49f3-8ac5-036273489768" />
Questo modello è stato progettato per rappresentare la gestione di un cinema.
Le entità principali individuate sono: film, sale, proiezioni e spettatori.

Dal punto di vista delle relazioni, un film può essere proiettato in una o più proiezioni, mentre una sala può ospitare una o più proiezioni nel tempo. Gli spettatori, invece, possono effettuare da zero a più prenotazioni.

Le tabelle film e sale contengono tutte le informazioni descrittive relative alla programmazione e alle strutture del cinema, mentre la tabella spettatori registra i clienti che possono prenotare uno spettacolo.

La tabella prenotazioni collega uno spettatore a una specifica proiezione, registrando il posto assegnato. In questo modo è possibile gestire la distribuzione dei posti e mantenere uno storico completo delle prenotazioni effettuate.


## Gestione Social
### Diagramma E/R
<img width="1198" height="766" alt="Screenshot 2025-11-16 183547" src="https://github.com/user-attachments/assets/2a494ba0-d656-4102-8292-4b0665768e69" />
Questo modello è stato progettato per rappresentare il funzionamento di una piattaforma social.
Le entità principali individuate sono: utenti, posts, commenti, media e likes.

Dal punto di vista delle relazioni, un utente può creare zero o più post, ai quali possono essere associati zero o più contenuti multimediali tramite la tabella media. Gli utenti possono inoltre interagire con i post pubblicando commenti o lasciando like. I commenti sono legati sia al post che all’utente che li ha scritti, mentre i like possono essere attribuiti ai post o ai commenti, permettendo di tracciare tutte le interazioni degli utenti.

La tabella utenti contiene le informazioni identificative e di accesso degli iscritti, mentre la tabella posts rappresenta i contenuti pubblicati sulla piattaforma. Le tabelle commenti e media arricchiscono i post rispettivamente con testo aggiuntivo e contenuti multimediali.

La tabella likes registra le reazioni degli utenti ai post o ai commenti.
