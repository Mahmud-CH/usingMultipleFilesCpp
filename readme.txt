the way it works
in tasks.json inside the args section

I changed the "${file}"
to "${workspeceFolder}"

what the "${workspaceFolder}" does is it 
gives the directory of the file you're complining
up to the folder and then I added the files
I wanted to compile together like this

"${workspaceFolder}/main.cpp",
"${workspaceFolder}/otherFile.cpp"

and thats it

you can make it so that it always compiles to the same .exe file
by changing the "${fileDirname}\\${fileBasenameNoExtension}.exe"

to "${workspaceFolder}/insertName.exe"

you cold not insert a name it would still work
it would just compile like this ".exe"


the way I did it at the start was by 
giving it the directory to the file like this

"D:desktop/code/cpp/multipleFiles/main.cpp",
"D:desktop/code/cpp/multipleFilesexportingFiles/otherFile.cpp",
(this makes it so that both the files compile together)

"-o",
"D:desktop/code/cpp/multipleFilesexportingFiles/main.exe"
(this just to change the compiled .exe file to always be main.exe)

Note:
I could not make it so that it works without
me having to enter the files every time it didn't work

this is what i tried:
"${workspaceFolder}\\*.cpp", "${workspaceFolder}\\**.cpp",and
${fileDirname}\\**.cpp

it kept giving me the same error of not being able to find the 
D:desktop/code/cpp/multipleFilesexportingFiles/*.cpp 

I don't know how to make it stop loking for a *.cpp file and 
to just compile all the files that have .cpp in them.