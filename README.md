I MADE A CONSOLE BASED CHESS GAME MADE IN C++ FOR MY FINAL PROJECT OF OOP.

This Chess Game simulates a real two-player Chess match inside the console environment.
The system validates moves according to official Chess rules, detects check/checkmate situations, and prevents illegal gameplay actions such as self-check moves.

The project focuses on both:

Strong game logic implementation
Clean and modular OOP design
♟️ Key Features
✅ Complete Chess Set

Implemented all standard Chess pieces with their individual movement behavior:

King
Queen
Rook
Bishop
Knight
Pawn

Each piece follows official Chess movement rules.

✅ Piece-Specific Move Validation

Every piece contains its own movement logic:

Bishop → Diagonal movement
Rook → Horizontal & Vertical movement
Knight → L-shaped movement
Queen → Combined Rook + Bishop movement
King → One-step movement
Pawn → Forward movement with attack diagonals
✅ Collision Detection System

The board verifies whether a piece’s path is clear before allowing movement.

Examples:

Rooks cannot jump over pieces
Bishops require a clear diagonal path
Knights are exempt since they can jump
✅ Check & Checkmate Detection

Advanced game logic identifies:

When a King is under attack (Check)
When no valid moves remain (Checkmate)

This ensures realistic gameplay mechanics.

✅ Self-Check Prevention (Undo Logic)

The game automatically rejects moves that place the player's own King in danger.

This feature simulates professional Chess rules by preventing illegal moves.

✅ Turn-Based Gameplay
White and Black turns alternate automatically
Invalid moves are rejected with proper validation
✅ Color-Coded Console Interface

Using the windows.h library, the board is displayed with a clean and readable color-based layout inside the Windows terminal.

🛠️ Technical Implementation
🔹 Object-Oriented Programming Concepts
🔸 Inheritance

A common base class Piece contains shared attributes such as:

Position
Color
Piece Name

Derived classes like:

Queen
Knight
Pawn

inherit and customize functionality.

🔸 Polymorphism

The function:

virtual bool isValidMove()

is declared virtual in the base class and overridden in every derived piece class.

This allows the board to interact with all pieces uniformly through base-class pointers.

🔸 Encapsulation
Piece positions
Board state
Game logic

are managed securely within classes to maintain data integrity and modularity.

🔸 Dynamic Memory Management

The board is implemented using:

Piece* board[8][8];

Memory allocation and cleanup are handled carefully using destructors to avoid memory leaks.

In conclusion, every move of piece and validations are implemented successfullly..

