# Documentation Rules

## General Principles
1. Each **README** should focus solely on explaining its specific concept
2. No meta-information about documentation or contributing in sub-**README**s
3. No "A Friendly Note" sections in sub-**README**s
4. Keep descriptions clear, concise, and focused
5. Use consistent formatting across all documentation
6. Any file using the **.prompt** extension MUST be treated as sourcecode and CANNOT be changed as part of this process 

## Main **README** Structure
1. Brief introduction explaining the repository's purpose
2. Table of contents with working links
3. Purpose section explaining what the repository is for
4. Repository structure showing the <directory-tree> formatted as described under **Directory Tree Format**

## Sub-**README** Structure
1. Clear title explaining the concept
2. Brief description of what the concept is
3. List of available items with brief descriptions
4. No usage instructions or best practices
5. No contributing guidelines
6. No meta-documentation information

## Directory Tree Format
1. Use table format for better link support
2. Show only folders with markdown links
3. Do not add individual files to the tree in the **main README**, do add them for **sub-README**
4. Maintain proper indentation for hierarchy
5. Use emoji indicators for visual distinction

**Directory Tree Format template**
   ```
   | 📦 prompts |
   |------------|
   | ├── 📂 [folder](path/) |
   | │   ├── 📂 [subfolder](path/) |
   | └── 📂 [folder](path/) |
   ```


## Content Guidelines
1. Each concept should be self-contained
2. Avoid cross-referencing between **README**s
3. Keep descriptions focused on the "what" not the "how"
4. Use consistent terminology across all documentation
5. Avoid redundant information 