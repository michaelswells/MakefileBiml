# MakefileBiml
## Biml Makefiles for a sane VS experience

Here's a brief introduction to Biml makefiles with a longer tutorial to follow.

You need a saner way to program Biml, and have .biml files laying around everywhere is a nightmare, especially when it comes to tiering them and adding other functionality.

This method provides a way to organize code easily, import it easily, and make it easy to have even an intern build your Biml!  Because we hook into the VS IDE you'll only be able to have one VS instance open when compiling!

## How to make this work in your world
1. Configure the `Biml\Config.cs` to point at your cloned `BimlRoot` dir 
2. Configure `Biml\BuildTargets` to point at a temp target dir, and your desired package directory (usually one level above your Biml root, aka, your project folder)
3. Change `Biml\CommonTiers\1.Environment.biml` to point at the correct path for your flat files
4. Right click on the Makefile in Visual Studio and click `Generate SSIS Packages`
5. **Note**: Because we are 'hooking' the Visual Studio IDE instance, you should only have one instance of VS open (or else you'll get some bizarre errors) - that would be the instance where you're trying to compile the Biml!
