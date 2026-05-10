<div align="center">

<br>

<h1>🗣️ Bhojpuri-Lang</h1>

**Programming ab Bhojpuri mein! (Programming now in Bhojpuri!)**

<br>

A fun, esoteric programming language built to make learning parsers and interpreters approachable. Write code using Bhojpuri keywords, run it natively in the browser via Pyodide, and get scolded in Bhojpuri when your syntax is wrong (`galat ba bhai...`).

<br>

<a href="https://bhojpuri-lang.vercel.app/"><img src="https://img.shields.io/badge/Playground-Live-2ea44f?style=flat-square" alt="Playground Live"></a>&nbsp;
<a href="https://github.com/im-anishraj/bhojpuri-lang"><img src="https://img.shields.io/badge/Made%20in-India-orange?style=flat-square" alt="Made in India"></a>&nbsp;
<a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square&labelColor=0d1117" alt="MIT"></a>&nbsp;
<a href="https://gssoc.girlscript.tech/"><img src="https://img.shields.io/badge/GSSoC-2026-ff6b35?style=flat-square&labelColor=0d1117" alt="GSSoC 2026"></a>

<br><br>

<a href="https://bhojpuri-lang.vercel.app/"><b>Try the Playground Live! →</b></a>

<br><br>

<a href="#-quickstart">Quickstart</a>&ensp;·&ensp;<a href="#-syntax">Syntax</a>&ensp;·&ensp;<a href="#%EF%B8%8F-how-it-works">Architecture</a>&ensp;·&ensp;<a href="#-contribute">Contribute</a>

</div>

<br>

---

<br>

## 🚀 Quickstart

You don't need to install anything to try it out — just use the [Web Playground](https://bhojpuri-lang.vercel.app/). But if you want to run it locally or hack on the interpreter:

```bash
# Clone the repository
git clone https://github.com/im-anishraj/bhojpuri-lang.git
cd bhojpuri-lang

# Install dependencies (mostly just standard Python)
pip install -r requirements.txt

# Start the interactive REPL
python -m bhoj
```

Run a specific file:
```bash
python -m bhoj examples/01_hello.bhoj
```

<br>

---

<br>

## 📝 Syntax Cheat Sheet

Everything in Bhojpuri-Lang maps to standard programming logic, just with a desi twist.

<table>
  <tr>
    <th>Bhojpuri Keyword</th>
    <th>English / Python Equivalent</th>
    <th>Example Code</th>
  </tr>
  <tr>
    <td><code>bhai</code></td>
    <td>Variable declaration (<code>var</code> / <code>let</code>)</td>
    <td><code>bhai x = 10</code></td>
  </tr>
  <tr>
    <td><code>bola</code></td>
    <td>Print (<code>print()</code>)</td>
    <td><code>bola "Namaste World"</code></td>
  </tr>
  <tr>
    <td><code>agar</code></td>
    <td>If condition (<code>if</code>)</td>
    <td><code>agar x > 5 tab</code></td>
  </tr>
  <tr>
    <td><code>nahi ta</code></td>
    <td>Else condition (<code>else</code>)</td>
    <td><code>nahi ta</code></td>
  </tr>
  <tr>
    <td><code>jab tak</code></td>
    <td>While loop (<code>while</code>)</td>
    <td><code>jab tak x < 10 tab</code></td>
  </tr>
  <tr>
    <td><code>bas kar</code></td>
    <td>Break loop (<code>break</code>)</td>
    <td><code>bas kar</code></td>
  </tr>
  <tr>
    <td><code>sahi</code></td>
    <td>Boolean True (<code>True</code>)</td>
    <td><code>bhai flag = sahi</code></td>
  </tr>
  <tr>
    <td><code>galat</code></td>
    <td>Boolean False (<code>False</code>)</td>
    <td><code>bhai flag = galat</code></td>
  </tr>
</table>

<br>

---

<br>

## 🏗️ How it works (Under the hood)

Bhojpuri-Lang isn't just a regex-replace over Python code. It is a full tree-walk interpreter written from scratch. This makes it a perfect codebase for **beginners** to learn how compilers and languages actually work.

```text
┌────────────────────────────────────────────────────────┐
│ 1. Lexical Analysis (Lexer)                            │
│ Reads raw string -> Breaks it into Tokens              │
│ `bhai x = 5` -> [KEYWORD(bhai), ID(x), EQ, INT(5)]     │
├────────────────────────────────────────────────────────┤
│ 2. Parsing (Parser)                                    │
│ Reads Tokens -> Builds an Abstract Syntax Tree (AST)   │
│       (Assign)                                         │
│       /      \                                         │
│     (x)      (5)                                       │
├────────────────────────────────────────────────────────┤
│ 3. Interpretation (Interpreter)                        │
│ Traverses AST -> Executes logic in Python memory       │
│ Memory state: { "x": 5 }                               │
└────────────────────────────────────────────────────────┘
```

<br>

---

<br>

## 🤝 Contribute (GSSoC 2026)

Bhojpuri-Lang is proudly participating in **[GSSoC 2026](https://gssoc.girlscript.tech/)**! 

We have tons of [good first issues](https://github.com/im-anishraj/bhojpuri-lang/issues) open. You can contribute by:
1. Adding new Bhojpuri keywords (e.g., `gin` for `for` loops).
2. Improving the React Web Playground UI.
3. Adding fun, custom Bhojpuri error messages to the Parser.
4. Writing more example `.bhoj` scripts.

<p align="center">
<a href="https://github.com/im-anishraj/bhojpuri-lang/issues"><b>🐛 View Open Issues</b></a>
</p>

<br>

---

<br>

<div align="center">

<br>

**Crafted with ❤️ for the open-source community.**

<br>

<a href="https://github.com/im-anishraj/bhojpuri-lang/stargazers"><img src="https://img.shields.io/github/stars/im-anishraj/bhojpuri-lang?style=flat-square&logo=github&labelColor=0d1117&color=e3b341&label=stars" alt="Stars"></a>&ensp;
<a href="https://github.com/im-anishraj/bhojpuri-lang/network/members"><img src="https://img.shields.io/github/forks/im-anishraj/bhojpuri-lang?style=flat-square&logo=github&labelColor=0d1117&color=8b949e&label=forks" alt="Forks"></a>

<br>

<sub>Licensed under MIT · Maintained by <a href="https://github.com/im-anishraj">@im-anishraj</a></sub>

</div>
