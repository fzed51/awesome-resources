# awesome-resources
Collection de ressource pour toute sortes de projets

## nodejs

## js

### création d'un projet vite

Création d'un projet vite avec tout ce qu'il faut

- créatin du prjet
  ```shell
  cd parent
  yarn create vite my-project --template react-ts
  cd my-project
  yarn
  git init
  touch .env
  echo >>.gitignore
  echo '# Environement'>>.gitignore
  echo '.env'>>.gitignore
  echo '.env.*'>>.gitignore
  echo '!.env.sample'>>.gitignore
  rm README.md
  echo `# my-project`
  rm public/*
  rm src/assets/*
  ```

  vite-env.d.ts
  ```typescript
  /// <reference types="vite/client" />
  interface ImportMetaEnv {
    readonly VITE_VAR: string;
  }  
  interface ImportMeta {
    readonly env: ImportMetaEnv;
  }
  ```
  main.tsx
  ```typescript
  import React from 'react'
  import ReactDOM from 'react-dom/client'
  import App from './App.tsx'
  import "main.css"
  
  ReactDOM.createRoot(document.getElementById('root')!).render(
    <React.StrictMode>
      <App />
    </React.StrictMode>,
  )
  ```
  main.css
  ```css
  html {}
  body {}
  ```
  App.tsx
  ```typescript
  import "./App.css";
  function App() {
    return <>App</>;
  }  
  export default App;
  ```
  App.css
  ```css
  #root {}
  ```
#### compléments

- compilation du scss
  ```shell
  yarn add -D sass
  ```

- utilisation de MUI
  ```shell
  yarn add @mui/material @emotion/react @emotion/styled @mui/icons-material
  yarn add @fontsource/roboto
  ```
  App.tsx
  ```typescript
  import { CssBaseline, ThemeProvider } from "@mui/material";
  import { theme } from "./theme";
  import "./App.css";
  
  function App() {
    return (
      <ThemeProvider theme={theme}>
        <CssBaseline/>
        <>App</>
      </ThemeProvider>
    );
  }
  export default App;
  ```
  theme.ts
  ```typescript
  import { createTheme } from "@mui/material";
  import createPalette from "@mui/material/styles/createPalette";
  import "@fontsource/roboto"
  export const palette = createPalette({});
  export const theme = createTheme({
    palette,
    typography: {
      fontFamily: [
          'Roboto',
          '-apple-system',
          '"Segoe UI"',
          'Arial',
          'sans-serif',
          '"Apple Color Emoji"',
          '"Segoe UI Emoji"',
          '"Segoe UI Symbol"',
        ].join(','),
    }
  });
  ```

  - join URL
    ```shell
    yarn add url-join
    ```
    
  - delais asynchrone
    ```shell
    yarn add delay-async
    ```
    
  - usehooks(🔥)-ts
    ```shell
    yarn add usehooks-ts
    ```
    voir [usehooks-ts.com](https://usehooks-ts.com/)

  - génération d'UUID
    ```shel
    yarn add uuid
    yarn add -D @types/uuid
    ```
    ```typescript
    import { v4 as uuid } from 'uuid';
    uuid(); // ⇨ '9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d'
    ```
    pour les navigateur utiliser directement `crypto.randomUUID()`
    
## php

## python


