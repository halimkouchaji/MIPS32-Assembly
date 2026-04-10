# MIPS32-Assembly

Cryptographic Memory Maze (MIPS32 & C)

A low-level systems and cryptography-inspired project implementing a deterministic memory maze generator and decoder using MIPS32 Assembly and C. The system models memory as a structured 16×16 grid, where both topology and stored data are derived entirely from a student-specific cryptographic transformation of an 8-digit ID.

The project focuses on bit-level manipulation, memory-mapped logic, and custom encoding techniques to simulate a lightweight cryptographic memory system.

Core Concept

The system transforms a student ID into a unique computational signature that drives both:
• Maze structure generation (walls vs. paths)
• Encrypted data encoding inside memory cells

Each grid cell is defined using positional bit encoding and ID-based transformations, ensuring that every generated maze is fully unique and deterministic per input ID.

Technical Highlights
• Dynamic generation of a 16×16 memory maze
• Wall placement derived from modular evaluation against a sequence of prime numbers (< 50)
• Bitwise position encoding:
• position = (x << 16) | y
• ID-based encryption using XOR transformations:
• temp = position XOR ID
• Bit rotation-based encryption:
• ROTATE(temp, ID % 32)
• Stateful decoder architecture using four dependent memory buffers (A, B, C, D)
• XOR-chain dependencies to enforce sequential decoding integrity

Implementation Details
• MIPS32 Assembly: Low-level implementation focusing on direct memory control, bitwise operations, and register-level optimization
• C Language: Reference implementation used for validation and algorithmic clarity

Skills Demonstrated
• Low-level memory manipulation and architecture-aware programming
• Bitwise cryptographic transformations (XOR, rotation, masking)
• Algorithmic maze generation using number theory (primes)
• Stateful system design with interdependent memory buffers
• Cross-language system modeling (Assembly ↔️ C)

Outcome

This project demonstrates the design of a deterministic cryptographic memory model, combining systems programming, mathematical logic, and low-level assembly techniques to simulate secure and structured data representation within constrained memory environments.
