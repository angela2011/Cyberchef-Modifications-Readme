# Project Documentation for CyberChef

## 1. Project Overview

### What does the software do?
**CyberChef** is a web-based tool designed for performing a wide range of encryption/decryption on data using various algorithms and ciphers. It allows users to encode, decode, encrypt, decrypt, compress, decompress any data stored in files or even any string of characters and analyze them through a very intuitive drag-and-drop interface.

### What problem does it solve?
CyberChef eliminates the need to use multiple tools for different data manipulation tasks. For instance a website called **dcode** can only transform data using one cipher at a time as is the case with many other similar, existing open source tools. Instead of switching between scripts, command-line tools, or websites, users can perform complex operations all in one place.

It solves problems such as:
- Data encoding/decoding (Base64, URL, Hex, etc.)
- Cryptographic operations (hashing, encryption, decryption)
- Forensic data analysis
- Debugging and reverse engineering encoded data

### Who would typically use it?
CyberChef is commonly used by:
- Regular ctf players
- Digital forensics analysts
- Penetration testers
- Anybody interested in learning cryptography or data processing

---

## 2. Repository Structure

The repository is organized into several important folders:

### `src/`
- Contains the main source code of the application.
- Includes core logic for operations (“recipes”) and UI components.
- This is where most of the functionality is implemented.

### `docs/`
- Holds documentation related to the project.
- May include guides, architecture explanations, or usage instructions.

### `test/`
- Contains test cases for verifying functionality.
- Ensures that transformations and operations work correctly.

### `assets/`
- Includes static resources such as images, icons, and stylesheets used in the UI.

### `scripts/`
- Contains build or automation scripts.
- Used for tasks like building, packaging, or deploying the application.

### `dist/`
- Contains the compiled/production-ready version of the application.
- This is what gets deployed or hosted.

### `node_modules/` (generated)
- Stores project dependencies installed via npm.
- Not usually part of the repository but created during setup.

---

## 3. Technologies Used

### Programming Languages
- **JavaScript** (primary language)
- HTML & CSS for UI

### Frameworks / Libraries
- Uses modular JavaScript architecture (custom-built components)
- Relies on various cryptographic and encoding libraries internally

### Build Tools
- **Node.js** – runtime environment
- **npm** – dependency management
- **Webpack** (or similar bundler) – for building and bundling the project

### Other Tools
- Browser-based interface (runs entirely on the client side)
- No backend/database required (stateless processing)

---

## 4. Contribution Workflow

### Contribution Guidelines
- The repository does include contribution guidelines (typically in `CONTRIBUTING.md`).
- Contributors are expected to follow coding standards and testing practices.

- Most recent contribution made to this includes:
  
Contributors: Lamby777 and C85297

Type of change: UI/UX improvement for bettr error handling

Focus: Making CyberChef more user-friendly by improving error handling by providing clearer messages when a numerical input is left empty.

- Apart from that there are 209 other contributers regularly making improvements which highights it is an active project and is being worked on continuosly.
### Issues
- Issues are used to:
  - Report bugs
  - Suggest features
  - Track improvements
- Each issue is labeled and discussed before implementation.

### Pull Requests
To contribute:
1. Fork the repository
2. Create a new branch for your feature/fix
3. Make changes and commit them
4. Submit a Pull Request
5. Wait for code review and feedback

Maintainers review PRs before merging them into the main branch.

---

## 5. Something Interesting I Noticed

I was initially drawn to this repository because it is developed by a government organization (GCHQ), which immediately caught my attention. The description of CyberChef as a “Cyber Swiss Army Knife” made me curious, and I wanted to explore what kind of capabilities such a tool could offer.

I am generally interested in exploring government-developed websites and understanding their security aspects, as many such platforms can have vulnerabilities. What surprised me the most about CyberChef was that, despite being developed by a government agency, it is open source and publicly accessible. This combination of transparency and security focus made it even more interesting to explore.

A few months ago, I conducted a workshop where I explained phishing attacks and how malicious actors can deceive users. During that time, I came across CyberChef for the first time and used it as a demonstration tool. So for the workshop, I created two visually similar URLs:

- https://manipalgov-verify.pages.dev/
- https://manipaIgov-verify.pages.dev/

At first glance, both links appear identical, but they actually differ by a single character (lowercase “l” vs uppercase “I”), making them point to entirely different destinations. This is a classic example of a homograph attack used in phishing.

By using CyberChef operations such as converting the input into hexadecimal, binary, or ASCII representations, I was able to demonstrate the difference between the two URLs. Although CyberChef cannot directly determine which link is legitimate, it helps reveal the underlying character differences, allowing users to analyze suspicious inputs more effectively.

Something I thought of while exploring the tool is the possibility of adding a feature that could analyze URLs in real time and flag potentially malicious ones by detecting visually similar characters or unusual patterns in their encoding. This could maybe enhance CyberChef’s usefulness in phishing detection. I would love to maybe contribute on something like this.
