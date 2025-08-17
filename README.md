{
  "name": "saborial-app",
  "version": "1.0.0",
  "private": true,
  "description": "Gestión integral para Saborial",
  "dependencies": {
    "react": "^18.0.0",
    "react-dom": "^18.0.0",
    "react-router-dom": "^6.0.0"
  },
  "scripts": {
    "start": "react-scripts start"
  },
  "author": "fabri0117-bit"
}
node_modules/
build/
.env
.DS_Store
# Saborial App

Aplicación web para la gestión integral de la empresa Saborial: Inventario, Producción, Ventas, Atención al Cliente, Gestión de Usuarios y Reportes.

## Instalación

```bash
npm install
```

## Ejecución

```bash
npm start
```

## Características

- Inventario
- Producción
- Ventas
- Atención al Cliente
- Gestión de Usuarios
- Reportes

## Autor

fabri0117-bit

<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Saborial App</title>
  </head>
  <body>
    <div id="root"></div>
  </body>
</html>
import React from "react";
import { BrowserRouter as Router, Routes, Route, Link } from "react-router-dom";
import Inventario from "./components/Inventario";
import Produccion from "./components/Produccion";
import Ventas from "./components/Ventas";
import AtencionCliente from "./components/AtencionCliente";
import GestionUsuarios from "./components/GestionUsuarios";
import Reportes from "./components/Reportes";
import "./App.css";

function App() {
  return (
    <Router>
      <div>
        <nav>
          <ul>
            <li><Link to="/inventario">Inventario</Link></li>
            <li><Link to="/produccion">Producción</Link></li>
            <li><Link to="/ventas">Ventas</Link></li>
            <li><Link to="/atencion-cliente">Atención al Cliente</Link></li>
            <li><Link to="/gestion-usuarios">Gestión de Usuarios</Link></li>
            <li><Link to="/reportes">Reportes</Link></li>
          </ul>
        </nav>
        <Routes>
          <Route path="/inventario" element={<Inventario />} />
          <Route path="/produccion" element={<Produccion />} />
          <Route path="/ventas" element={<Ventas />} />
          <Route path="/atencion-cliente" element={<AtencionCliente />} />
          <Route path="/gestion-usuarios" element={<GestionUsuarios />} />
          <Route path="/reportes" element={<Reportes />} />
          <Route path="/" element={
            <div className="container">
              <h2>Bienvenido a Saborial</h2>
              <p>
                Gestiona Inventario, Producción, Ventas, Atención al Cliente, Usuarios y Reportes de forma moderna y eficiente.
              </p>
            </div>
          } />
        </Routes>
      </div>
    </Router>
  );
}

export default App;
