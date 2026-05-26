# ♟️ Chess System Java

Um jogo de xadrez completo rodando no terminal, desenvolvido em Java com foco em Programação Orientada a Objetos.

---

## ✨ Funcionalidades

- ♟️ Jogo completo de xadrez para dois jogadores
- 🎯 Destaque visual dos movimentos possíveis para cada peça
- ⚠️ Detecção de **xeque** e **xeque-mate**
- 🔄 Movimentos especiais:
  - **Roque** (Kingside e Queenside)
  - **En Passant**
  - **Promoção de Peão**
- 📋 Histórico de peças capturadas
- 🛡️ Programação defensiva com tratamento de erros e exceções customizadas

---

## 🎮 Como Jogar

O tabuleiro é representado por **colunas (a–h)** e **linhas (1–8)**. Para mover uma peça:

1. Digite a **posição de origem** da peça (ex: `e2`)
2. Os movimentos possíveis serão destacados em **amarelo** no tabuleiro
3. Digite a **posição de destino** (ex: `e4`)

```
Source: e2
Target: e4
```

---

## 🖥️ Pré-requisitos

- [Java JDK](https://www.oracle.com/java/technologies/downloads/) 11 ou superior
- Terminal com suporte a cores ANSI (recomendado: Git Bash no Windows, Terminal no Linux/macOS)

> ⚠️ **Windows:** O Prompt de Comando (cmd) e o PowerShell padrão não exibem as cores corretamente. Use o **Git Bash** para melhor experiência visual.

---

## 🚀 Como Executar

### Clonando o repositório

```bash
git clone https://github.com/ryansouzas/chess-system-java.git
cd chess-system-java
```

### Compilando e executando

```bash
# Compilar
javac -d bin src/application/Program.java src/boardgame/*.java src/chess/*.java src/chess/pieces/*.java

# Executar
java -cp bin application.Program
```

Ou importe o projeto em uma IDE como **Eclipse** ou **IntelliJ IDEA** e execute a classe `application.Program`.

---

## 🗂️ Estrutura do Projeto

```
src/
├── application/
│   └── Program.java          # Ponto de entrada da aplicação
├── boardgame/
│   ├── Board.java             # Lógica do tabuleiro genérico
│   ├── BoardException.java    # Exceção para erros de tabuleiro
│   ├── Piece.java             # Classe abstrata de peça
│   └── Position.java          # Posição no tabuleiro (linha/coluna)
└── chess/
    ├── ChessException.java    # Exceção específica do xadrez
    ├── ChessMatch.java        # Lógica principal da partida
    ├── ChessPiece.java        # Extensão de Piece com regras do xadrez
    ├── ChessPosition.java     # Posição no formato xadrez (a1–h8)
    ├── Color.java             # Enum para as cores das peças (WHITE/BLACK)
    └── pieces/
        ├── Bishop.java        # Bispo
        ├── King.java          # Rei
        ├── Knight.java        # Cavalo
        ├── Pawn.java          # Peão
        ├── Queen.java         # Rainha
        └── Rook.java          # Torre
```

---

## 🏗️ Design e Arquitetura

O projeto utiliza dois pacotes principais com responsabilidades bem definidas:

- **`boardgame`** — camada genérica e reutilizável de tabuleiro, independente das regras do xadrez
- **`chess`** — camada de regras do xadrez, construída sobre o `boardgame` via herança e polimorfismo

Principais conceitos de POO aplicados:

- Herança e polimorfismo (hierarquia de peças)
- Encapsulamento e programação defensiva
- Exceções customizadas por camada
- Matrizes e manipulação de posições

---

## 📸 Demonstração

```
Captured pieces:
White: 
Black: 

Turn: 1
Waiting player: WHITE

  a b c d e f g h
8 R N B Q K B N R 8
7 P P P P P P P P 7
6 - - - - - - - - 6
5 - - - - - - - - 5
4 - - - - - - - - 4
3 - - - - - - - - 3
2 P P P P P P P P 2
1 R N B Q K B N R 1
  a b c d e f g h

Source: 
```

---

## 📄 Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 👤 Autor

Feito por **Ryan Souza**

[![GitHub](https://img.shields.io/badge/GitHub-ryansouzas-181717?style=flat&logo=github)](https://github.com/ryansouzas)
