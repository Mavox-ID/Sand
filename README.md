# 🏜️ Sand Cipher System

<div align="center">

![Sand Cipher Logo](https://img.shields.io/badge/Sand-Cipher-orange?style=for-the-badge&logo=lock&logoColor=white)
![Version](https://img.shields.io/badge/version-15.0.0-blue?style=for-the-badge)

**A unique encryption system for any small projects**

[Live Demo](#) • [Documentation](#features) • [Report Bug](#) • [Request Feature](#)

---

</div>

## ✨ Features

🔒 **Three Powerful Modes**
- **Standard Mode**: Encrypt English text (max 5 letters) to Sand code
- **Decrypt Mode**: Decode Sand cipher back to English text (unlimited length)
- **Numbers Mode**: Convert between Sand code and pure numbers

🛡️ **Advanced Anti-Collision System**
- No repeating cipher letters in a single message
- No repeating numbers in a single message
- Cipher letter value never equals its paired number (e.g., B≠2, C≠3)
- Smart conflict detection and prevention

🎨 **Beautiful UI**
- Modern gradient design
- Responsive layout
- Real-time validation
- Interactive cipher table

## 🚀 Quick Start

### Live Demo

Simply open website: [**https://mavox-id.github.io/Sand**](https://mavox-id.github.io/Sand)

### Usage Example

```javascript
// Encrypt
Input: YOU
Output: E11F2O1

// Decrypt
Input: E11F2O1
Output: YOU

// To Numbers
Input: E11F2O1
Output: 51162151

// To Sand Code
Input: 51162151
Output: E11F2O1
```

## 📖 How It Works

### Sand Cipher Alphabet

The Sand Cipher uses **16 letters (A-P)** and **17 numbers (0-16)** to create unique encryption codes.

| Cipher Letters | Values | Numbers | Range |
|---------------|--------|---------|-------|
| A - P | 1 - 16 | 0 - 16 | 17 values |

### Encryption Rules

1. **Unique Combinations**: Each English letter maps to a unique Sand code (letter + number)
2. **No Self-Reference**: A cipher letter's numeric value cannot match its paired number
   - ❌ `B2` is invalid (B = 2nd letter)
   - ✅ `B4` is valid (B ≠ 4)
3. **No Repetition**: Within a single encrypted message:
   - Each cipher letter appears only once
   - Each number appears only once
   - No conflicts between letter values and numbers

### Example Breakdown

```
Word: NO
├─ N → N12 (cipher letter N=14, number 12) ✅
└─ O → O5  (cipher letter O=15, number 5)  ✅

Encrypted: N12O5
```

**Why this works:**
- N (14) ≠ 12 ✅
- O (15) ≠ 5 ✅
- No repeating letters: N, O (unique) ✅
- No repeating numbers: 12, 5 (unique) ✅
- No conflicts: 14 ∉ {12, 5} and 15 ∉ {12, 5} ✅

## 🎯 Modes Explained

### 📝 Standard Mode (Encryption)

**Purpose**: Convert English text to Sand cipher code

- **Input**: A-Z letters (max 5)
- **Output**: Sand code (e.g., `A0B6C9`)
- **Limit**: 5 letters maximum
- **Validation**: Real-time conflict detection

### 🔓 Decrypt Mode

**Purpose**: Convert Sand cipher back to English text

- **Input**: Sand code (unlimited length)
- **Output**: English text
- **Format**: Must match pattern `[A-P]\d+`
- **Example**: `A0B6C9D11E13` → `HELLO`

### 🔢 Numbers Mode

Two sub-modes for advanced operations:

#### ➡️ Sand → Numbers
Converts Sand code to pure numeric format

```
A0B6 → 1026
│ │   ││└─ number 6
│ │   │└── B position (2)
│ │   └─── number 0
│ └─────── A position (1)
```

#### ⬅️ Numbers → Sand
Reconstructs Sand code from numbers

```
1026 → A0B6
│││└─ becomes B6
││└── becomes 0
│└─── becomes B
└──── becomes A
```

## 🎨 Color Scheme

| Mode | Gradient | Purpose |
|------|----------|---------|
| Standard | 🟦 Blue → 🟪 Purple | Active mode indicator |
| Encrypted | 🟩 Cyan → 🟪 Pink | Encryption success |
| Decrypted | 🟧 Orange → 🟥 Red | Decryption success |
| Numbers | 🟨 Yellow → 🟧 Orange | Number conversion |

## 🛠️ Technical Details

### Technologies Used

- **HTML5**: Semantic structure
- **CSS3**: Modern gradients, flexbox, animations
- **JavaScript ES6+**: Regex parsing, Set operations, dynamic validation

### Browser Support

| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 90+ | ✅ Full |
| Firefox | 88+ | ✅ Full |
| Safari | 14+ | ✅ Full |
| Edge | 90+ | ✅ Full |

### Key Algorithms

**Cipher Generation**
```javascript
// Ensures no self-referential conflicts
letterValue !== number // B(2) ≠ 2
```

**Conflict Detection**
```javascript
// Tracks used elements in real-time
usedCipherLetters.has(letter) → Error
usedNumbers.has(number) → Error
```

## 📊 Performance

- ⚡ Instant encryption/decryption
- 🎯 O(n) complexity for validation
- 💾 Zero external dependencies
- 📱 Mobile-optimized responsive design

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Inspired by classical substitution ciphers
- Built with modern web standards
- Designed for educational purposes

## 📬 Contact

- Mavox-ID: [https://github.com/Mavox-ID](https://github.com/Mavox-ID/)

- Project: [https://github.com/Mavox-ID/Sand](https://github.com/Mavox-ID/Sand/)

---

<div align="center">

**Made with Mavox-ID**

⭐ Star this repository if you find it helpful!

</div>
