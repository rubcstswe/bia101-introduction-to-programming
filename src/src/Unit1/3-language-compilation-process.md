# Language Compilation Process

Computer programs are written in high-level programming languages (e.g., Python, Java, C++), which are human-readable but not directly executable by computers. 

To run these programs, they need to be translated into a form that the computer's processor can understand, typically machine code or bytecode. 

This translation process is known as compilation or interpretation, depending on the approach used.

![Compilation vs Interpretation](/src/images/com_vs_int.webp)

# Compilation

Compilation is the process of translating a high-level programming language into machine code, which is a low-level language that the computer's processor can directly execute.

Compiled programs typically run faster than interpreted programs because the translation to machine code is done ahead of time, and the resulting executable can run directly on the processor without the need for further translation at runtime.

# Interpretation

Interpretation is the process of executing a high-level programming language directly, without first translating it into machine code. 

An interpreter reads the source code, analyzes it, and immediately executes the corresponding instructions.

Interpreted programs are generally easier to develop and debug because the source code can be executed directly without the need for a separate compilation step. 

However, interpreted programs typically run slower than compiled programs because the translation and execution happen simultaneously at runtime.

# Compilation vs. Interpretation

| S.NO. | Compiled Language | Interpreted Language |
|-------|-------------------|----------------------|
| 1     | Compiled language follows at least two levels to get from source code to execution. | Interpreted language follows one step to get from source code to execution. |
| 2     | A compiled language is converted into machine code so that the processor can execute it. | An interpreted language is a language in which the implementations execute instructions directly without earlier compiling a program into machine language. |
| 4     | The compiled programs run faster than interpreted programs. | The interpreted programs run slower than the compiled program. |
| 5     | In a compiled language, the code can be executed by the CPU. | In Interpreted languages, the program cannot be compiled, it is interpreted. |
| 6     | This language delivers better performance. | This language delivers slower performance. |

**Compiled languages**:
- C
- C++
- Rust
- Go

**Interpreted languages**:
- Python
- Ruby
- JavaScript
- PHP