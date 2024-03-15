fetch('menu.json')
//Que hace? Eta linea inicia la carga del archivo menu.json fetch es una funcion de javascript que facilita la realizacion de solicitudes de red,como obtener datos de un archivoo un endoint de API. 
//Comofnciona? fetch devuelve una promesa que;cuando  resuelve, te da acceso a la respuesta de la solicitud. Esta respuesta no es directaamnete o datos en formao JON,sino un objeto de respuesta que incluye varios detalles sobre la respuesta
.then (reponse => reponse.json())
//Que hace? Esta linea toma objeto de respuesta obtenido del fetch y utiliza lmetodo.json() para convertir el cuerpo de la respuesta en un objeto JavaScript (eto asume que el cuerpo de la respuesta eta en formato JSON).

//Como funciona? El metodo.json ()tambien devuelve una promesa, la cual se resuelve con el contenido formato JSON 
then (data =>{
    const menuContainer = document.getElementById
    ('menu-container') ;
    // que hace? Aqisepprocan los datos Json ya conertidos, se obtiene una referencia el contenido del menu en html mediante getElementById('menu container'), y luego se itera sobre los elementos (categorias) del menu.
    data.items.forEach(category =>{
        const categoryTitle = document.createElement('h2');
        //Que hace? Aqui se crea un elemento h2, se asigna el nombre de la catgoria como su contenido de texto, y luego se añade ste titulo al contenedor del menu/.
        categoryTitle.textContent = category.category;
        menuContainer.appendChild(categoryTitle);

  const table = document.createElement('table');  
  //Que hace? Se crea un elemento table para cada caegoria. Ademas,se prepara el encabezado (tableHead) con las columnas pertinentes. tablebody se iniciliza vacio y se llenara con los elementos de la categoria.
  const tableHead = <tr><th>Foto</th><th>Description</th><th>Precio</th></tr>;
  let tableBody= '';
  // Como funciona Para cada categoria en los datos , se realizan varia paos: Crear un titulo para la categoria , se  establece su contenido de texto al nombre de la categoria (category. category), luego se agrega al contenedor del menu).
  // Crear tabla para los elementos de esas categorias (primero se define el encabzado de la tabla <tr><th>Foto</th><th>Description</th><th>Precio</th></tr> ).
  category .items. forEach(item=>{
    tableBody += `<tr>
        <td><img src=" ${item.name} alt ="${item.name}"</td>
        <td>${item.name} - "${item.description}" </td>
        <td>${item.price}</td>
    </tr> `;
  
   } );
    
 } );
 } )

