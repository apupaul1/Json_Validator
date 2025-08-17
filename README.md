# JSON Syntax Validator (Lex & Yacc Project)

A simple **JSON Syntax Validator** built using **Lex** and **Yacc** as part of Compiler Design Lab.  
This tool validates JSON syntax and displays recognized tokens, element counts, and pretty-printed output.

---

## 🚀 Features
- ✅ **JSON Syntax Validation** – Detects whether JSON input is valid or invalid.  
- 📝 **Token Recognition** – Displays all tokens: `{`, `}`, `[`, `]`, `:`, `,`, strings, numbers, booleans, null.  
- 🔍 **Detailed Error Reporting** – Shows error type with line and column if JSON is invalid.  
- ⚡ **Supports Nested JSON** – Objects and arrays of any depth.  
- 📊 **Element Count** – Counts objects, arrays, strings, numbers, booleans, and nulls.  
- 🎨 **Colorful Output** – Green for valid values, Red for errors, Cyan for deep nested elements.  
- 💾 **Output Saved** – Pretty-printed JSON saved to `output.json`.  

---

## 🖥️ How It Works
1. **Lexical Analysis**: Lexer (`json.l`) tokenizes JSON input.  
2. **Parsing**: Parser (`json.y`) checks token sequence against JSON grammar.  
3. **Validation Result**:  
   - Valid → prints success message and saves pretty-printed JSON.  
   - Invalid → prints detailed error message with line and column.  
4. **Token Display**: After parsing, all tokens with line & column are shown.  
5. **Element Count**: Number of objects, arrays, strings, numbers, booleans, and nulls displayed.  

---

## ⚙️ Installation & Run (Windows)

### Step 1: Install Tools
- Install [WinFlexBison](https://sourceforge.net/projects/winflexbison/) (Flex & Bison for Windows).  
- Add installation directory to **System PATH** (e.g., `C:\winflexbison\`).  

### Step 2: Clone or Download Project
git clone https://github.com/your-username/json-syntax-validator.git
cd json-syntax-validator

### Step 3: Compile Lex & Yacc Files
win_flex json.l
win_bison -d json.y
gcc lex.yy.c json.tab.c -o json_validator

### Step 4: Run the Validator
-Provide a JSON file as input:
      json_validator sample.json

