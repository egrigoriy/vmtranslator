# VM Translator for Hack Machine Language from nand2tetris.org written in Java

This is a Java implementation of Virtual Stack Machine translator to Hack Assembly language. 
It is written as part of the NandToTetris course: https://www.nand2tetris.org/project07 and https://www.nand2tetris.org/project08.
The Virtual Machine language specification can be found in included pdf files.
The Hack Language specifications can be found here: https://www.nand2tetris.org/project04


# Description

1. **VMTranslator.java**: drives the process of translating code written in Virtual Stack Machine language to Hack assembly language. 
It is responsible for reading the input file (\*.vm) or directory containing one or more VM files and and writing the result in a sinle one file (\*.asm).
2. **VMProgram.java**: translates all given vm files to assembler. If it's a single file, them assembler code of infinite loop is appended.
If there are more than one file, them assembler code for bootstrap is prepended.
3. **VMParser.java**: returns assembly code corresponding to given VM file. Each original VM command is included as comment just before corresponding assembly code.
4. **VMPreprocessor.java**: removes all empty lines and comments (full-line and inline).
5. **ASMWriter.java**: provides assembly code for each VM command. It combines assembly code from ASM.java methods.
6. **ASM.java**: contains methods providing assembly code for all required Hack assembly commands, including stack management.


# Usage

```bash
$ javac VMTranslator.java
$ java VMTranslator source
```

where source is either a relative path to a VM file ("\path\to\folder\xxx.vm") or a folder ("\path\to\folder\") containing one or more VM files.
 
 
# License

This project is licensed under the [GNU General Public License v3.0](LICENSE)

