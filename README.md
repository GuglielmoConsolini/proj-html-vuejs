SPIEGAZIONE PROGETTO ARTIST


Sviluppatori: Guglielmo , Luciano , Massimiliano.


<--------Descrizione progetto------>

L'obbiettivo è di ricreare il sito web di MaxCoach , un portale che offre una moltitudine di corsi 
che variano fra classi che insegnano lingue , Fitness , Danza e tecniche artistiche. Il nostro progetto
si concentra sulla parte artistica del sito.

Divisione del lavoro:

-Header e sezione OnlineCourses- Sviluppatore: Massimiliano

-Main fino alla sezione Slider: Guglielmo

-Footer e sezione blog : Luciano


Summary della mia esperienza sul codice:

Nella prima sezione che ho chiamato SezioneCards vado a generare con un ciclo v-for un componente figlio 
di none Card.vue(con le props) così da far apparire 4 cards allineate. Ho gestito le immagine che popolano 
il background con position absolute e z-index , mentre per gestire il movimento ho usato la libreria Kinesis.
Il drag del Carosello funziona grazie alla libreria vue-dragscroll mentre il funzionamento vero e proprio lo 
gestisco con le proprietà offsetWidth e offsetLeft e la funzione ScrollTo(x,y). Invece per gestire l'hover nella 
sezione youtube ho usato lo pseuto selettore :before per far ingrandire solo il background e non il vero contenitore.

Librerire e Framework utilizzati:

Bootstrap - FontAwesome - Kinesis - Vue-Dragscroll