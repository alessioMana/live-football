# live-football
## Come Programmare:

Apri il progetto che ti interessa modificare e fai la modifiche che vuoi su una copia del branch sul tuo profilo, quando hai finito fai la pull request in modo che io possa vedere le modifiche, testare il codice e applicarle.

> Per modificare il server e le pagine Web puoi farlo direttamente da qualsiasi editor o da GitHub Web

> Per modificare l'app Android segui [questo tutorial](https://www.html.it/pag/67712/integrare-github-in-android-studio/) per installare git su Android Studio

> IOS Coming Soon! (Se qualcuno volesse iniziare a svilupparlo è libero di farlo)

#### :warning: Attenzione! :warning:
***
__Nella pull request seleziona sempre il branch della funzionalità che stai modificando (le pull request al master non verranno considerate) e se stai inviando un codice non ancora finito segnalalo con il tag `In Progress` o, al contrario, con `working`__
***
## Tipi di progetto:

Sono presenti diverse parti del progetto individuali:
- Server
  - Server RTMP in Node.js
- Client (Live in entrata e uscita)
  - Android
  - IOS
  - Web (Testing del server attuale)
  
Guarda la [wiki](https://github.com/alessioMana/live-football/wiki) per saperne di più.

## Il protocollo RTMP:

Il funzionamento del server RTMP è molto semplice: il client in streaming si connette al server, tramite ip e porta, e invia i pacchetti della diretta codificati nella maniera specificata dal client. Il server si occupa di ricevere i pacchetti e inoltrarli a tutti i client connessi a quella live stream tramite il percorso. Tutti i client connessi alla stanza ricevono i pacchetti e li decodificano per poterli vedere.

#### Esempio:

> Il client in streaming si connette al server `rtmp://127.0.0.1:999/live/streaming1` e dopo l'handshake inizia a inviare i pacchetti video

> Il server riceve i pacchetti e li inoltra a tutti i client connessi all'indirizzo specificato dal client in streaming

> Un client può vedere la diretta connettendori a `rtmp://127.0.0.1:999/live/streaming1` mentre può vederne un'altra connettendosi a `rtmp://127.0.0.1:999/live/streaming2`

Ulteriori informazioni sul protocollo RTMP potete trovarle su [Wikipedia](https://en.wikipedia.org/wiki/Real-Time_Messaging_Protocol) o sul [Manuale Ufficiale](https://www.adobe.com/devnet/rtmp.html)
