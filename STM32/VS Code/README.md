# VS Code files for STM32

I abandonned STM32CubeIDE because, well I hate it. So I code using VS Code and the `STM32CubeIDE for Visual Studio Code` extension. I [wrote an article](https://medium.com/machina-speculatrix/a-coding-environment-for-stm32-using-vs-code-375343ab3612) about it. Even ST itself thinks this is the best way to go now.

## tasks.json

This is a file that sets up a task to flash code to the microcontroller without debugging. It assumes you have installed **STM32CubeProg**.There's a useful [YouTube video](https://www.youtube.com/watch?v=0VvnFkwu2Y0) about it.

You create this file in the `.vscode` directory of your project.

You need to change `projectname.elf` in line 10 to the name of the ELF file for your project.

It assumes the relevant ELF file is in the `build/Debug` folder. If not, change this part of the path on line 10.

This setup is for a Mac. The path to STM32CubeProgrammer in line 7 is typical for a MacOS setup, but you may need to double-check. On another OS you need to find the full path for the executable and amend line 7.
