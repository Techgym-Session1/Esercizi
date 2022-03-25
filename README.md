# Esercizi
Prima di iniziare, scarica questa repo sul tuo pc in locale.

1. Cercare, scaricare ed avviare l'immagine `nginx`
   1. Cercare l'immagine di `nginx`.
   2. Scaricare l'immagine di `nginx`.
   3. Avviare un container partendo dall'immagine di `nginx`, sulla porta locale `3000` esponendo la porta `80`, in modalità background
   4. Testare il funzionamento del container con  `curl localhost:3000`.
   5. Rimuovere il container creato.
 
2. Avviare container nginx e modifica della homepage con il comando exec.
   1. Avviare un container partendo dall'immagine di nginx, sulla porta locale `3000` esponendo la porta `80`, in modalità background.
   2. Trovare l'id del container ispezionando i container attivi.
   3. Eseguire il comando `sed -i -e's/Welcome to nginx!/Welcome to TechGym!/' /usr/share/nginx/html/index.html` sul container.
   4. Testare il funzionamento del container con  `curl localhost:3000`.
  
3. Salvare il container creando una nuova immagine. Run della nuova immagine.
   1. Salvare il container creato nel punto 2 creando una nuova immagine con il nome "my-techgym-image"
   2. Rimuovere il container dopo aver creato l'immagine.
   3. Avviare un nuovo container partendo dall'immagine appena creata, sulla porta locale `3000`, esponendo la porta `80`, in modalità background.
   4. Testare il funzionamento del container con  `curl localhost:3000`.
   5. Rimuovere il container creato.
  
4. Avviare un container nginx e modifica della homepage utilizzando un volume locale.
   1. Posizionarsi all'interno della cartella `Esercizio-4/html`
   2. Avviare un container nginx sulla porta locale `3000`, esponendo la porta `80`, in modalità background, montando come volume la cartella `html` con al suo interno il file `index.html`, associandolo a questo path `/usr/share/nginx/html/index.html` del container.
   3. Testare il funzionamento del container con  `curl localhost:3000`.
   4. Modifica e salva il file `index.html` in locale.
   5. Testare la modifica con  `curl localhost:3000`.
   6. Rimuovere il container creato.
 
5. Scrivere un dockerfile che prenda l'immagine di nginx e modifichi la homepage. 
   1. Prendere l'immagine nginx.
   2. Lanciare il comando per la modifica della homepage.
   3. Costruire l'immagine partendo dal Dockerfile creato con il nome di `nginx-build`.
   4. Avviare un nuovo container partendo dall'immagine appena creata, sulla porta locale `3000`, esponendo la porta `80`, in modalità background.
   5. Testare il funzionamento del container con  `curl localhost:3000`.
   6. Rimuovere il container creato.

6. Scrivi un Dockerfile per un'applicazione React
   1. Scarica l'applicazione React da questo link: https://github.com/Techgym-Session1/Game
   2. Svolgi tutti i punti elencati all'interno del file `Dockerfile`
   4. Builda il container con il comando `docker build -t techgym-game .`
   5. Fai partire il container con il comando `docker run -d -p 3000:3000 techgym-game`
   6. Collegati all'indirizzo `http://localhost:3000`
   7. Partecipa al gioco 🎮
