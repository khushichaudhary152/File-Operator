<div align="center">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=42&duration=2500&pause=1000&color=FF0000&center=true&vCenter=true&width=700&lines=%F0%9F%93%82+FILE+OPERATOR" alt="📂 FILE OPERATOR" />
<h3>📔 Personal Journal Manager</h3>

🐍 Python File Handling Project

Write your thoughts. Save your memories. Find them anytime. ✨

</div>


## 📌 About the Project

File Operator is a beginner-friendly Python project that demonstrates how files can be managed through a command-line menu. Users can store journal entries in a text file, view saved entries, search by a keyword or date, clear all entries, or replace the journal content.

Each new entry is saved with a timestamp so it is easier to identify when it was written.

## ✨ Features

|Feature              |Description                                                                    |
|---------------------|-------------------------------------------------------------------------------|
|🆕 Create Journal File|Creates `journal.txt` if it does not already exist.                            |
|✍️ Add New Entry      |Appends a journal entry with the current date and time.                        |
|📖 View All Entries   |Displays the entries saved in the journal file.                                |
|🔎 Search Entries     |Searches journal content using a keyword or date.                              |
|🗑️ Delete All Entries |Clears the journal after user confirmation.                                    |
|♻️ Overwrite Journal  |Replaces the existing content with new content.                                |
|🚪 Exit               |Closes the application safely.                                                 |
|🛡️ Error Handling     |Handles missing files, operating-system file errors, and keyboard interruption.|



## 🧰 Built With

<table>
  <tr>
    <th>Technology</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>🐍 <b>Python</b></td>
    <td>Core programming language</td>
  </tr>
  <tr>
    <td>📂 <b>os</b></td>
    <td>Operating-system-related functionality</td>
  </tr>
  <tr>
    <td>🕒 <b>datetime</b></td>
    <td>Adds timestamps to journal entries</td>
  </tr>
  <tr>
    <td>📝 <b>File Handling</b></td>
    <td>Uses open(), read(), write(), and file modes</td>
  </tr>
  <tr>
    <td>🏗️ <b>Object-Oriented Programming</b></td>
    <td>Uses the JournalManager class and methods</td>
  </tr>
  <tr>
    <td>🛡️ <b>Exception Handling</b></td>
    <td>Handles errors using try, except, and specific file errors</td>
  </tr>
  <tr>
    <td>🔀 <b>Pattern Matching</b></td>
    <td>Uses match-case for menu selection</td>
  </tr>
</table>  

## 🔄 Application Workflow

```mermaid
flowchart TD
    A([🚀 Start]) --> B[Create JournalManager object]
    B --> C[Display main menu]
    C --> D{User choice}
    D -->|1| E[Create journal file]
    D -->|2| F[Add timestamped entry]
    D -->|3| G[View all entries]
    D -->|4| H[Search by keyword or date]
    D -->|5| I{Confirm deletion?}
    I -->|Yes| J[Clear journal file]
    I -->|No| K[Cancel deletion]
    D -->|6| L[Overwrite journal content]
    D -->|7| M([Exit program])
    E --> C
    F --> C
    G --> C
    H --> C
    J --> C
    K --> C
    L --> C
    D -->|Invalid choice| N[Show error message]
    N --> C
```

## 🧠 How File Handling Works

```mermaid
flowchart LR
    A[User selects an operation] --> B{File mode}
    B -->|x| C[Create only if file does not exist]
    B -->|a| D[Append new entry]
    B -->|r| E[Read saved content]
    B -->|w| F[Clear or replace content]
    C --> G[(journal.txt)]
    D --> G
    E --> G
    F --> G
```

|Mode |Used for           |Behaviour                                                         |
|-----|-------------------|------------------------------------------------------------------|
|`"x"`|Create file        |Creates a new file; raises `FileExistsError` if it already exists.|
|`"a"`|Add entry          |Adds new content at the end of the file.                          |
|`"r"`|View and search    |Reads existing content without changing it.                       |
|`"w"`|Delete or overwrite|Clears existing content before writing new content.               |

## 🎨 Output — Flowchart
```mermaid
flowchart TD
    A([Start]) --> B[Welcome Message]
    B --> C[Display Main Menu]
    C --> D[/Enter Your Choice/]
    D --> E{Select Option}
    E -->|1| F[Create Journal File]
    F --> F1[Display Success Message]
    F1 --> C
    E -->|2| G[Enter Journal Entry]
    G --> G1[Add Entry to File]
    G1 --> G2[Display Success Message]
    G2 --> C
    E -->|3| H[Read Journal File]
    H --> H1[Display All Entries]
    H1 --> C
    E -->|4| I[Enter Keyword or Date]
    I --> I1[Search Journal Entries]
    I1 --> I2[Display Search Results]
    I2 --> C
    E -->|5| J[Confirm Deletion]
    J --> K{Confirmation}
    K -->|Yes| L[Delete All Entries]
    K -->|No| C
    L --> C
    E -->|6| M[Enter New Journal Content]
    M --> M1[Overwrite Journal File]
    M1 --> M2[Display Success Message]
    M2 --> C
    E -->|7| N[Display Goodbye Message]
    N --> O([End])
    E -->|Invalid Choice| P[Display Error Message]
    P --> C
    style A fill:#D5F5E3,stroke:#229954,stroke-width:2px,color:#145A32
    style B fill:#D6EAF8,stroke:#2874A6,color:#154360
    style C fill:#D6EAF8,stroke:#2874A6,color:#154360
    style D fill:#FCF3CF,stroke:#D4AC0D,color:#7D6608
    style E fill:#E8DAEF,stroke:#884EA0,stroke-width:2px,color:#512E5F
    style F fill:#D5F5E3,stroke:#229954,color:#145A32
    style F1 fill:#D5F5E3,stroke:#229954,color:#145A32
    style G fill:#D6EAF8,stroke:#2874A6,color:#154360
    style G1 fill:#D6EAF8,stroke:#2874A6,color:#154360
    style G2 fill:#D5F5E3,stroke:#229954,color:#145A32
    style H fill:#D6EAF8,stroke:#2874A6,color:#154360
    style H1 fill:#D5F5E3,stroke:#229954,color:#145A32
    style I fill:#FCF3CF,stroke:#D4AC0D,color:#7D6608
    style I1 fill:#D6EAF8,stroke:#2874A6,color:#154360
    style I2 fill:#D5F5E3,stroke:#229954,color:#145A32
    style J fill:#FADBD8,stroke:#C0392B,color:#78281F
    style K fill:#E8DAEF,stroke:#884EA0,color:#512E5F
    style L fill:#F5B7B1,stroke:#C0392B,color:#78281F
    style M fill:#D6EAF8,stroke:#2874A6,color:#154360
    style M1 fill:#D6EAF8,stroke:#2874A6,color:#154360
    style M2 fill:#D5F5E3,stroke:#229954,color:#145A32
    style N fill:#D5F5E3,stroke:#229954,color:#145A32
    style O fill:#D5F5E3,stroke:#229954,stroke-width:2px,color:#145A32
    style P fill:#FADBD8,stroke:#C0392B,color:#78281F
```

## 📸 Output Screenshot

 <img width="1901" height="2317" alt="op 6 ss" src="https://github.com/user-attachments/assets/7ffa29a6-cd29-4b53-aa74-5031b1ebfa6d" />


## 🎥 Demo Video




⸻

<h3 align="center">👩‍💻 Created by Khushi Chaudhary</h3>
<p align="center">
  💖 Thank you for visiting my project!<br>
  Made with ❤️ and Python 🐍
</p>
<p align="center">
  ✨ Keep Learning • Keep Creating • Keep Growing ✨
</p>

⸻
