FrigoTrack è un'applicazione client-server sviluppata in C\# che permette di raccogliere e gestire dati di temperatura e umidità provenienti da sensori simulati, utilizzando un sistema di comunicazione sicuro.

Avvio del progetto

Per avviare il programma:

1. Aprire la soluzione FrigoTrack.sln in Visual Studio.  
2. Avviare il progetto Server.  
3. Avviare il progetto Client.  
4. Il client si collega al server e avvia la procedura di comunicazione.

Funzionamento

Il sistema prevede una comunicazione tra client e server. Prima di inviare i dati, il client effettua un handshake con il server per stabilire una chiave di sessione condivisa attraverso l'algoritmo Diffie-Hellman.

Una volta stabilita la chiave, i dati di telemetria vengono cifrati e inviati al server in formato JSON. Il server decifra i messaggi, verifica che rispettino lo schema previsto e registra le misurazioni ricevute.

