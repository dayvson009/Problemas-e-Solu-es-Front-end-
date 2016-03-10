# Problemas e Soluções

* **Problema >** Eu tenho um elemento onde quero colocar `height: 0;` e `height: auto;` com `transition`. Mais não é permitido o transition.
ex:
```
  <style>
    div{
      height: 0;
      transition: 1s;
    }

    div:hover{
      height: auto;
    }
  </style>

  <div>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
  </div>
```
**A transição não vai funcionar**;
* **Solução >** Coloque o código abaixo:
```
  <style>
    div{
      overflow: hidden;
      max-height: 0px;
      transition: 1s;
    }

    div:hover{
      max-height: 9999px;
    }
  </style>

  <div>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
  </div>
```
