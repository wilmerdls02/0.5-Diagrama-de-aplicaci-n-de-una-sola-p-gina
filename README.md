# 0.5-Diagrama-de-aplicaci-n-de-una-sola-p-gina

parte0 0.5: Diagrama de aplicación de una sola página


mermaid

sequenceDiagram

participant Usuario

participant Nanvegador

participant Servidor

Usuario->>Navegador: Accede a la ULR SPA (http://studies...spa)

Navegador->>Servidor: Get / exampleapp/spa (solicita el html de la spa)

Servidor-->>Navegador: Devuelve el html de la spa

Note right of Navegador: el navegador ejecuta JavaScript y carga la vista de la spa

Navegador->>Servidor: Get / exampleapp/main.css (Solicita la hoja de estilo)

Servidor-->>Navegador: Devuelve la hoja de estilo (CSS)

Navegador->>Servidor: Get / exampleapp/main.js (Solicita el archivo JavaScript)

Servidor-->>Navegador: Devuelve el archivo JavaScript (JS)

Navegador->>Servidor: Get / exampleapp/data.json (Solicita solicita los datos de las notas)

Servidor-->>Navegador: Devuelve las notas en formato JSON

Note right of Navegador: El navegador renderiza las notas en la vista


