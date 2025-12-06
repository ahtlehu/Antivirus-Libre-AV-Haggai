# Antivirus-Libre-AV-Haggai
Building an antivirus means combining static code scanning (SAST) with dynamic sandbox testing (DAST). Core parts include a detection engine with heuristics/ML, a user interface for scans, and an isolated environment. Develop in stages: prototype, MVP, production.
Building an antivirus that emphasizes code analysis involves focusing heavily on 
Static Application Security Testing (SAST) and integrating some dynamic analysis techniques to create a robust detection engine. 
Core Principles
    • No- Static Analysis (SAST): This is the primary method, which involves scanning the source code or compiled binaries without executing them to identify malicious patterns, known vulnerabilities, insecure coding practices, and structural flaws.
    • No-Dynamic Analysis (DAST): This complementary method involves executing the code in a secure, isolated environment (a sandbox or virtual machine) and monitoring its runtime behavior, such as system calls, memory usage, and network interactions, to catch issues that only appear during execution. 
Key Components to Develop
Manual Code Review:

    Function: Human security experts meticulously examine source code for vulnerabilities, design flaws, and adherence to secure coding practices.
    Benefits: Can identify complex logic flaws and design issues that automated tools might miss.
       
    1. Detection Engine: This is the heart of your antivirus.
          
        ◦ Heuristic/Behavioral Analysis: This component will analyze the code for suspicious characteristics or behaviors, even if a specific signature doesn't exist. This is where your code analysis emphasis comes in.
        ◦ Machine Learning (Optional but Recommended): You can train models to identify new and evolving threats by analyzing feature vectors from code samples.
    2. Scanning Interface: A way for users to interact with the software (GUI or command-line) to initiate scans, view reports, and manage threats.
    3. Isolation Environment (Sandbox): For dynamic analysis, you will need a secure virtualized environment to safely execute suspicious files. 
       
Recommended Tools and Libraries
    • Programming Languages: C/C++ are ideal for the performance-critical, low-level core functions, while Python is excellent for rapid prototyping, scripting analysis tools, and backend services.
    • Analysis Frameworks:
        ◦ A powerful tool for pattern matching and creating custom detection rules.
        ◦ static analysis of binaries.
        ◦ 
    • Libraries:
          
        ◦ OpenSSL: For robust cryptographic functions. 
          
Development Steps
       
    1. Develop the static analysis engine: Start by building a basic scanner that calculates file hashes and compares them against a small, manually curated database of known malware hashes.
    2. Implement advanced code analysis: Integrate a framework like to look for specific code patterns.
    3. Add dynamic analysis capabilities: Develop a system to safely run suspicious files in your isolated VM and monitor their behavior for malicious actions (e.g., attempts to encrypt files, make unusual network connections, modify system settings).
    4. Build the user interface: Create a user-friendly way to interact with your engine using a framework like Qt.
    5. Test rigorously: Continuously test your antivirus against a wide range of malware code that does not compile. No malware should run or it should be missing parts so no one can run it, or can scape from la cazerola. (in your isolated lab only!) and benign software to fine-tune your detection logic and minimize false positives. 
---------------------------------------------------------------------------------------
