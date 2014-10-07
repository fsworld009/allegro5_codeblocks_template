About this repository
===
This is a Code::Blocks project template for Allegro 5 development under Windows 7.
The purpose of this repository is to provide developers an easier way to set up Allegro 5 projects in Code::Blocks.
Please read the instructions below to setup your project.

Please note that this project setup may break in further versions of Allegro 5.

Version info
===
 - Code::Blocks 13.12
 - Allegro 5.0.10 Windows binaries from http://allegro.cc


Setup Guide
===
 - 1. git clone this repository
```
 git clone https://github.com/fsworld009/allegro5_codeblocks_template.git
 ```
 - 2. change folder name to your project name, assume it is called MyAllegroProject
 - 3. change allegro5_codeblocks_template.cbp to MyAllegroProject.cbp
 - 4. use a text editor to edit allegro5_codeblocks_template.cbp
 - 5. replace every string allegro5_codeblocks_template by MyAllegroProject
 - 6. open project with Code::Blocks.
 - 7. Under project tab on the left, right click your project and click Build Options
 - 8. click MyAllegroProject on the left
 - 9. On the right, click search directories -> compiler, change ```C:\allegro5\include``` to your allegro5 installation folder with "\include" at the end.
 - 10. click linker, change ```C:\allegro5\lib``` to your allegro5 installation folder with "\lib" at the end.
 - 11. go to your MinGW installation folder, search which folder contains libgdiplus.a, then change ```C:\mingw\lib``` to that folder.
 - 12. click "OK" to save setting.
 - 13. click file -> Save project to save your setting
 - 14. Build the project and run it.
 - 15. delete .git foler and create your own repository.

For step 6 to 13, if you're comfortable with xml you can just edit MyAllegroProject.cbp and change correnspponding settings.
 
Additional Info
===
 - Make sure you use the same version of MinGW to compile your project. It's better to avoid mixing up different gcc vertions of Allegro binaries and MinGW.
 - If you get error messages like ```undefined reference to `__gxx_personality_v0'``` or ```undefined reference to `_Unwind_Resume'``` when linking, you need a MinGW that uses dwarf for exception handling instead of sjlj.
  (source: http://stackoverflow.com/questions/10419801/undefined-reference-to-unwind-resume-and-gxx-personality-v0)
