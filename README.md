> CRUD CON FIREBASE Y ANGULAR


npx  
  
**Paso en VS code(opcional)**

Cmd + Shift + P = installar en el path para poder usar code .


- **Angular**

firebase login(Selecionamos la misma cuenta de VS code)

firebase projects:list (Ver listado de proyectos del firebase)

firebase init(Iniciar el firebase e ir selecionando las opciones presentadas)

ng add @angular/fire(Instalar la herramientas necesarias)


- Instalar firebase en el proyecto

npm install 


- **Crear proyecto**

ng new [nombreproyecto]


- **Iniciar servidor**

ng serve -o


- **Crear servicios**

ng generate service services/[servicio]


https://github.com/GarajedeIdeas/CodePills-CRUD-AngularFirebase


- **Crear componentes**

ng generate component components/[componenete]







Methodso for CRUD(Examples)

constructor(private firestore: Firestore) €•}
addPlace (place: • Place) • {
const placeRef = collection(this.firestore, 'places');
• return addDoc (placeRef, place) ;
｝
getPlaces (): Observable<Place [] > {
const placeRef = collection (this. firestore, 'places');
return collectionData(placeRef, { idField: 'id' }) as Observable<Place []>;
｝
deletePlace(place: • Place) {
const placeDocRef = doc (this. firestore, places/${place. id}*);
return deleteDoc (placeDocRef);
｝
