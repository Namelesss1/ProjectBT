### Building
This project uses the CT-Code Engine developed by Mr.Bean35000vr & Chadderz to patch the game at specific memory address using PowerPC assembly. 
See https://github.com/Chadderz121/wii-ct-code for information on how it works.
Of course, it is possible to use other methods of patching the game for this project. But this file outlines how it was done while this project was in development.

## Resources needed
- CT-Code Engine (https://github.com/Chadderz121/wii-ct-code) 
- Wiimm's ISO Tools (https://wit.wiimm.de/)
- DevkitPPC/DevkitPro (Supposedly only older versions will work with ct-code)
- Some way of running the game, Dolphin/Wii

## Extracting the game files
Use Wiimm's ISO tools to extract a legally-obtained iso copy of the game using the command `wit extract [iso name].iso [iso directory to extract to]` then get the English.szs file from /boot/strap/us/ and place it under the /strap/ directory from this repository.

## The Process
1. After downloading ct-code, copy the mod folder in this repository to /ct-code/bad1/bad1data/, replacing the original mod directory here. This is where all of the ASM code that implements the project functionality goes.
2. Replace the .ld files (rmc, rmce, rmcp, rmcj) in /ct-code/ with the .ld files under this repository. This is where all symbols, names, memory addresses and such used for this project go.
3. Open a terminal and cd under the /ct-code/ directory.
4. type `make clean` to erase any previously generated files, then type any of the following: `make all`, `make rmce`, `make rmcp`, `make rmcj` depending on the region to build
5. Under the newly-created /build/ directory, look for the mod1.bin and mod2.bin files. Copy them into the /strap/files/rmcu/rmc[u/e/j]/ directory depending on which region the mod files represent
6. In the /strap/ directory, use the following command from Wiimm's Tools: `wctct create [us/eu/jp]-szs ctcode.txt --ct-dir rmcu --ct-log=2 --images files -od English.szs` to patch the English.szs file.
7. Replace the english.szs file in the extracted files with the newly created one.
8. Patch main.dol under the /sys/ directory of the game files to support ct-code using Wiimm's ISO tools: `wstrt patch --add-ctcode main.dol`
9. Patch main.dol to support Wiimmfi access: `wstrt patch --wiimmfi main.dol`
10. Patch main.dol for the custom online region: `wstrt patch --region=700 main.dol`
11. Patch staticR.rel for the custom online region: `wstrt patch --region=700 StaticR.rel`
12. Copy any modified files from this repository (such as Race.szs, BMG files, etc.) into the game's extracted files
13. Copy the extracted files back into an ISO using command `wit copy [extracted iso directory] [desired ISO name].iso`
