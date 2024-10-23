<img src="https://www.unidformazione.com/wp-content/uploads/2017/05/logoUNIUD-2.jpg" alt="Logo Università degli Studi di Udine" width="300">

# ✏️📱 Progettazione di Applicazioni Mobili

###### 👨‍🏫 Prof. Stefano Burigat - 📧 stefano.burigat@uniud.it

##### ORARIO DELLE LEZIONI

| Giorno  | Orario        | Sede di Pordenone                              | Sede di Udine                                   |
| ------- | ------------- | ---------------------------------------------- | ----------------------------------------------- |
| Venerdì | 14:30 - 18:30 | Aula L06 (Una volta in presenza, una volta no) | Aula A018 (Una volta in presenza, una volta no) |

#### ESAME FINALE

[https://elearning.uniud.it/moodle/mod/page/view.php?id=133765](https://elearning.uniud.it/moodle/mod/page/view.php?id=133765)

> **NOTE SULL'ESAME FINALE**:
> Il professore ha il **Google Pixel 4a** quindi dobbiamo cercare di creare l'applicazione che funzioni al meglio su quel dispositivo, anche perché la testerà solo su quel dispositivo.

###### © 2024 | Appunti di [Pasquale Mazzullo](https://www.linkedin.com/in/pasqualemazzullo/) e [Giulia Martin](https://www.linkedin.com/in/martin-giulia/)

---

##### Lezione 1 - 04 Ottobre 2024 [Aula A018, Udine]

# Tipi di approcci per lo sviluppo di app

Quando si sviluppa un'applicazione, ci sono tre principali approcci che si possono seguire:

1. **Approccio Web**
   Questo metodo consiste nel creare l'app utilizzando tecnologie tipiche del web come **HTML**, **CSS** e **JavaScript**. L'app funziona all'interno di un browser e viene eseguita come una pagina web, ma è ottimizzata per essere utilizzata su dispositivi mobili. Un esempio sono le **Web App**. Questo approccio è utile perché permette di sviluppare l'app una sola volta per diversi dispositivi, ma ha accesso limitato alle funzionalità hardware del dispositivo (come la fotocamera o i sensori).

2. **Approccio Ibrido**
   L'approccio ibrido combina tecnologie web con strumenti che permettono di far funzionare l'app come se fosse nativa. Si utilizzano tecnologie come **HTML**, **CSS** e **JavaScript**, ma l'app viene "incapsulata" in un contenitore che la rende eseguibile sui dispositivi mobili. Un esempio di framework per questo approccio è **Ionic**. L'approccio ibrido permette di riutilizzare molto codice, ma non offre la stessa fluidità e accesso diretto alle funzionalità hardware come le app native.

3. **Approccio Nativo**
   Le app native vengono sviluppate utilizzando gli strumenti e i linguaggi messi a disposizione dalle piattaforme mobili specifiche:

   - **Android**: Si utilizza **Java** o **Kotlin** insieme all'**Android SDK**.
   - **iOS**: Si utilizza **Objective-C** o **Swift** insieme a **Xcode**.

   Questo approccio permette di accedere a tutte le funzionalità del dispositivo, inclusi elementi hardware come fotocamera, GPS e sensori, e offre le migliori prestazioni. Tuttavia, sviluppare un'app nativa richiede la scrittura di codice separato per ogni piattaforma (Android, iOS).

## Un esempio moderno: Flutter

Oggi esistono anche linguaggi e framework che permettono di sviluppare app native per più piattaforme contemporaneamente. Un esempio è **Flutter**, un **SDK** _(Software Development Kit)_ che consente di scrivere il codice una sola volta e poi compilarlo per diverse piattaforme (Android, iOS, Web, ecc.). Sebbene sia necessario apportare alcune modifiche specifiche per ogni dispositivo, la maggior parte del codice rimane uguale, riducendo il lavoro di sviluppo.

### Istruzioni per installare Flutter su Mac per lo sviluppo di app Android

**Passo 1: Scaricare Flutter SDK**

1. Vai al sito ufficiale di Flutter: [https://docs.flutter.dev/get-started/install/macos/mobile-android#install-the-flutter-sdk](https://docs.flutter.dev/get-started/install/macos/mobile-android#install-the-flutter-sdk).
2. Nella tabella che vedi, clicca sulla sezione `Download and install`. Dovrebbe essere selezionata di default ma se fosse selezionata `Use VS Code to install`, cambia sezione.
3. Clicca su uno dei bottoni blu per scaricare il pacchetto `.zip`. Fai attenzione a scaricare il pacchetto compatibile per il tuo processore. Se hai un Mac un po' vecchiotto, è probabile che tu abbia un processore Intel e quindi scarica il pacchetto per `Intel Processor`; se hai un Mac prodotto dal 2020 in poi, è probabile che tu abbia un processore Apple Silicon (M1, M2, M3, ...) e quindi scarica il pacchetto per `Apple Silicon`.

**Passo 2: Estrarre Flutter SDK**

1. Una volta scaricato il file `.zip`Puoi estrarre il contenuto del pacchetto in qualsiasi posto tu voglia del tuo computer. Ti consiglio di farlo in una directory denominata `development` (senza spazi e tutto minuscolo) in modo da tenere tutti i dati relativi allo sviluppo in un unico punto del tuo computer.

**Passo 3: Installare Android Studio "Ladybug"**

1. Vai sul sito ufficiale di Android Studio: [https://developer.android.com/studio](https://developer.android.com/studio).
2. Clicca sulla Call To Action `Download Android Studio Ladybug`.
3. Scorri tutti i _Terms and Conditions_ e spunta _I have read and agree with the above terms and conditions_.
4. Seleziona la versione di Android Studio corretta per il tuo Mac. Se hai un Mac un po' vecchiotto, è probabile che tu abbia un processore Intel e quindi scarica il pacchetto `Mac with Intel chip`; se hai un Mac prodotto dal 2020 in poi, è probabile che tu abbia un processore Apple Silicon (M1, M2, M3, ...) e quindi scarica il pacchetto `Mac with Apple chip`.

**Passo 4: Installare Android Studio**

1. Una volta scaricato il file `.dmg`, aprilo e trascina l'icona di Android Studio nella cartella _Applicazioni_.

**Passo 5: Configurare l'SDK Android 14**

1. Apri Android Studio.
2. Vai su **Preferences** > **Appearance & Behavior** > **System Settings** > **Android SDK**.
3. Nella scheda SDK Platforms, seleziona `Android 14 (UpsideDownCake)` e clicca su Apply per scaricare l'SDK.
4. Vai nella scheda SDK Tools, assicurati che sia selezionato `Android SDK Build-Tools` e clicca su OK.

**Passo 6: Configurare Flutter con Android Studio**

1. Apri Android Studio.
2. Vai su **Preferences** > **Plugins**.
3. Nella barra di ricerca in alto a destra, cerca `Flutter`.
4. Clicca su `Install` accanto al plugin Flutter.
5. Durante l'installazione, Android Studio ti chiederà di installare il plugin **Dart**. Conferma per installarlo.
6. Riavvia Android Studio per applicare i cambiamenti.

**Passo 7: Verificare l'installazione di Flutter in Android Studio**

1. Apri un nuovo progetto in _Android Studio_.
2. Seleziona _Flutter_ come tipo di progetto e segui le istruzioni per creare un'app Flutter di base.
3. Se ti viene chiesto, specifica il percorso di Flutter SDK (quello che hai specificato in _Passo 2: Estrarre Flutter SDK_).

**Passo 8: Configurare l'emulatore Android per Android 14**

1. In Android Studio, vai su `Device Manager` cliccando sull'icona `More Actions` (tre puntini) nell'angolo in alto a destra della finestra di Android Studio.
2. Clicca su `Create Device`.
3. Seleziona un modello di dispositivo (per l'esame il **Google Pixel 4a**, ossia quello sul quale il profesore testerà l'applicazione) e clicca su `Next`.
4. Nella sezione `System Image`, seleziona l'immagine di sistema per `Android 14 (UpsideDownCake)`.
5. Clicca su `Next`, poi su `Finish` per completare la creazione dell'emulatore.

**Passo 9: Avviare l'emulatore**

1. Dalla finestra `Virtual Device Manager`, avvia il nuovo emulatore cliccando sull'icona del play accanto al nome del dispositivo. La prima volta ci metterà un po' di tempo perché deve allocare la memoria e fare tutto il suo setup, ma più volte lo si avvia, prima si caricherà.

**Passo 10: Creare un'app Flutter**

1. Apri _Android Studio_.
2. Clicca sull'icona centrale `New Flutter Project`.
3. Assicurati che nella barra laterale a sinistra, sia selezionata la voce _Flutter_ e che in alto ci sia il path del pacchetto Flutter SDK (quello che hai specificato in _Passo 2: Estrarre Flutter SDK_).
4. Compila i campi richiesti:
   - **Project name**: Inserisci un nome per il tuo progetto (es. esame_pam).
   - **Flutter SDK path**: Se non è già popolato, specifica il percorso del Flutter SDK (quello che hai specificato in _Passo 2: Estrarre Flutter SDK_).
   - **Project location**: Scegli dove salvare il progetto sul tuo Mac. Per comodità ti consiglio di utilizzare la stessa directory nella quale hai il Flutter SDK in modo da avere tutto in un unico posto.
   - **Description**: Puoi aggiungere una descrizione opzionale per la tua app (es. "Nome e Cognome - Matricola - Esame di Progettazione di Applicazioni Mobili - A.A. 2024/2025").
5. Nella sezione `Piattaforme`, spunta solo `Android` per l'esame.
6. Clicca su `Next` e concludi il processo. Dovresti a questo punto ritrovarti Android Studio con tutti i file di basse dell'applicazione Flutter.

##### Lezione 2 - 11 Ottobre 2024 [Aula L06, Pordenone]
