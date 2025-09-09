Py2CPP is an experimental project that uses a LLM to automatically convert Python code into equivalent, compilable C++ code.

The project wraps Anthropic’s Claude model into a Gradio interface that streams converted C++ code in real-time as you enter Python. 

It is designed to help developers, researchers, and students quickly translate Python snippets into performant C++ while preserving logic and numerical precision.

Python is simple and widely used for prototyping, but performance-critical applications often require C++.

Manually rewriting Python into C++ is error-prone and time-consuming.

LLMs can automate the translation, but often add explanations or extra text.
This project enforces strict, code-only outputs, so you can copy, compile, and run right away.

The provided Python code defines a calculate() function that performs a large iterative computation using two parameters, measuring how long it takes with time.time(), and then prints the result with 12 decimal places and the execution time with 6 decimals.
The LLM-generated C++ output is a direct translation of this logic: it replicates the same iterative process using integer variables j1 and j2, preserves the mathematical operations, and measures execution time with std::chrono for higher precision. 
Finally, it prints the computed result with 12 decimal places and the runtime with 6 decimals, producing the same style of output as Python but in a format ready to be compiled and executed in C++.
