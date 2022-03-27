                                -------- README -----------
                                   
                                   Blazor CRUD .NET 5

1- Creando un proyecto Blazor Server en Visual Studio .NET 5 se inicio limpiando la solución
   como modelos "WeatherForecast", las pagina "Counter" y "FetchData" dejando la solución limpia.
2- Microsoft SQL Server Management Studio, se define la base de datos, para conocer los modelos
   que se crearan en la solución para tener las definiciones claras.
 -Se creo las tablas "Classification", con los campos "Id" "IdClassification" "scientificName"
  "families" "lifespan" "ordera" "phylum" "kingdom" "image"
3- En el archivo "appsettings.json" se conecta la base de datos, mediante "View>SQL Server Object Explorer" 
   se busca la base de datos, y en propiedades se busca "Connection strin" y mediante la sentencia 
   "ConnectionStrings": {
    "SqlConnection": "Data Source=OSCARPOW96\\SQLEXPRESS;Initial Catalog=BlazorCRUD;Integrated Security=True;Connect Timeout=30;Encrypt=False;TrustServerCertificate=False;ApplicationIntent=ReadWrite;MultiSubnetFailover=False"
   } se conecta la base de datos.
4- Diseñamos arquitectura de la solución, creando un nuevo proyecto "Class Library .NET Standard", se crea la clase llamada "Classification.cs"
   escribimos una propiedad por cada una de las columnas que se crearon.
5- Se crea el Component Razor con el nombre de "Insectos.razor" para el insert de datos, guardado mediante "SaveFilm"
   Que servira igual como Update mas adelante.
   -Implementamos una clase nueva que es "ClassificationRepository" y "IClassificationRepository" para definir los metodos
   que tendra la solución.
   -Implementamos una clase nueva que es "ClassificationService" y una interfaz que es "IClassificationService".
6-Creando un Component Razor con el nombre de "InsectList.razor" que mostrara la lista de la base de datos, y de los datos
  que se ingresaran despues.
   -En las clases "ClassificationRepository","IClassificationRepository", ClassificationService" y "IClassificationService"
    definimos los metodos, y las sentencias SQL para hacer el llamado a la base de datos para hacer el CRUD.
7-Se cambio el diseño para verlo mas presentable el aplicativo, usando Radzen y sus componentes para ver mas limpio todo.

