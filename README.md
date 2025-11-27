# 🎴 Poker Game

Una aplicación web interactiva de Póker desarrollada con TypeScript, implementando la arquitectura Modelo-Vista-Controlador (MVC) y usando el framework CSS Bulma con estilos personalizados de la Universidad de La Laguna.

## 📋 Descripción

Este proyecto simula un juego de póker para dos jugadores, permitiendo repartir manos de 5 o más cartas, clasificarlas automáticamente según las reglas del póker (escalera, color, full, etc.) y determinar el ganador. El sistema reconoce todas las jugadas estándar del póker, desde parejas hasta escalera real.

## ✨ Características

- **Lógica completa de póker**: Reconoce las 10 jugadas estándar (pareja, doble pareja, trío, escalera, color, full, póker, escalera de color y escalera real)
- **Comparación de manos**: Algoritmo que determina automáticamente el ganador siguiendo las reglas oficiales
- **Interfaz gráfica moderna**: Diseño responsive con Bulma CSS personalizado
- **Arquitectura MVC**: Separación clara entre modelo, vista y controlador
- **Baraja completa**: 52 cartas con imágenes individuales
- **Algoritmo Fisher-Yates**: Para barajar de forma aleatoria y justa
- **Manos configurables**: Permite jugar con 5 o más cartas por mano
- **Documentación técnica**: Generada automáticamente con TypeDoc

## 🚀 Building and Running the Code

### Requisitos previos

- Node.js (v14 o superior)
- npm (v6 o superior)

### Instalación

1. Clona el repositorio:
```bash
git clone git@github.com:Guillermo-Gonzalez-Pineda/PokerGame.git
cd PokerGame
```

2. Instala las dependencias:
```bash
npm install
```

### Compilación

Para compilar el proyecto en modo desarrollo:
```bash
npm run build
```

Para compilar en modo producción:
```bash
npm run build:prod
```

### Ejecución

Inicia el servidor de desarrollo con hot-reload:
```bash
npm start
```

El juego estará disponible en: `http://localhost:8080`

### Generar documentación

Para generar la documentación técnica con TypeDoc:
```bash
npm run doc
```

La documentación se generará en el directorio `docs/` y estará accesible en `http://localhost:8080/docs`


## 🛠️ Tecnologías Utilizadas

- **TypeScript**: Lenguaje principal del proyecto
- **Webpack**: Bundler y servidor de desarrollo
- **Bulma CSS**: Framework de estilos con personalización ULL
- **TypeDoc**: Generación de documentación
- **ESLint**: Linter para mantener calidad del código
- **ts-loader**: Cargador de TypeScript para Webpack

## 📁 Estructura del Proyecto

```
PokerGame/
├── model/              # Lógica del negocio
│   ├── card.ts        # Clase Card (representa una carta)
│   ├── deck.ts        # Clase Deck (mazo de cartas)
│   ├── hand.ts        # Clase Hand (mano genérica)
│   ├── poker-hand.ts  # Clase PokerHand (mano de póker con lógica)
│   └── poker-game.ts  # Clase PokerGame (orquestador del juego)
├── view/              # Interfaz de usuario
│   └── PokerView.ts   # Renderizado de cartas y UI
├── controller/        # Controlador de eventos
│   └── GameController.ts
├── www/               # Archivos estáticos
│   ├── index.html     # Página principal
│   ├── poker.html     # Página del juego
│   ├── uml.html       # Diagrama UML
│   ├── img/           # Imágenes de cartas (52 PNG)
│   └── styles/        # Estilos CSS personalizados
├── docs/              # Documentación generada (TypeDoc)
├── dist/              # Archivos compilados
└── main.ts            # Punto de entrada
```

## 🎯 Cómo Jugar

1. Abre la aplicación en tu navegador
2. (Opcional) Configura el número de cartas por mano (mínimo 5)
3. Haz clic en **"Repartir ambas"** para repartir cartas a ambos jugadores
4. O usa **"Repartir mano 1"** / **"Repartir mano 2"** para repartir individualmente
5. El sistema clasificará automáticamente las manos y mostrará el ganador

## 🏗️ Arquitectura

El proyecto sigue el patrón **Modelo-Vista-Controlador**:

- **Modelo**: Clases que representan la lógica del juego (Card, Deck, Hand, PokerHand, PokerGame)
- **Vista**: Clase PokerView que maneja el renderizado del DOM
- **Controlador**: GameController que conecta la lógica con la interfaz y gestiona eventos

## 👤 Autor

**Guillermo González Pineda**

- Universidad de La Laguna
- Grado en Ingeniería Informática
- Programación de Aplicaciones Interactivas (PAI)
- Email: alu0101574899@ull.edu.es
