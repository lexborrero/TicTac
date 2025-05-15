# TicTacToe iOS App

A simple two-player TicTacToe game implemented in Swift and UIKit. This ViewController manages the game board UI, turn logic, win/draw detection, and scorekeeping.

---

## Features

- **Two players** (“Nought” and “Cross”) alternate turns  
- **9-button grid** for selecting cells  
- **Win detection** for horizontal, vertical, and diagonal lines  
- **Draw detection** when all cells are filled  
- **Scoreboard** displayed in an action sheet after each round  
- **Automatic board reset** and turn swapping  

---

## UI Elements

- **UILabel** (`turnLabel`): shows whose turn it is (“X” or “O”)  
- **UIButtons** (`a1`–`a9`): represent the 3×3 grid cells  

All buttons are connected as `@IBOutlet`s and share the same `@IBAction` (`boardTapAction`) for taps.

---

## Game State Properties

```swift
enum Turn { case Nought, Cross }

var firstTurn  = Turn.Cross        // Who starts each round
var currentTurn = Turn.Cross       // Whose turn it is now

let NOUGHT = "O"                   // Symbol for Nought
let CROSS  = "X"                   // Symbol for Cross

var board = [UIButton]()           // Array holding all 9 grid buttons

var noughtsScore = 0               // Running score for Nought
var crossesScore = 0               // Running score for Cross
