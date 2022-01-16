# Architecture

## Introduction

This file describes the project architecture, such as classes, database modeling, etc. If you need to create a diagram, use the [mermeid live editor] (https://mermaid-js.github.io/mermaid-live-editor/), which is free and open-source. Just copy the mermeid "source code" and paste it here using:

A must have for any project is the high level view of main entities (or parts). A simple data-flow diagram can also help a lot. Additionally, keeping this file closer to the source code of your app make it more likely to be updated.

<pre>
```mermeid
 comand
 ...
 comand
```
</pre>

## Examples

### Example of communication

```mermeid
sequenceDiagram
    Alice->>+John: Hello John, how are you?
    Alice->>+John: John, can you hear me?
    John-->>-Alice: Hi Alice, I can hear you!
    John-->>-Alice: I feel great!
    Alice->>+John: ❤️
```

### ER example

```mermeid
erDiagram
          CUSTOMER }|..|{ DELIVERY-ADDRESS : has
          CUSTOMER ||--o{ ORDER : places
          CUSTOMER ||--o{ INVOICE : "liable for"
          DELIVERY-ADDRESS ||--o{ ORDER : receives
          INVOICE ||--|{ ORDER : covers
          ORDER ||--|{ ORDER-ITEM : includes
          PRODUCT-CATEGORY ||--|{ PRODUCT : contains
          PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```

### Class diagram example

```mermeid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
    class Fish{
      -int sizeInFeet
      -canEat()
    }
    class Zebra{
      +bool is_wild
      +run()
    }
```

