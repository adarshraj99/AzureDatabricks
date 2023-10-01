* To get the packages : **pkg.go.dev**
* Go packages are available in '**rsc.io**' eg : 'rsc.io/quote/v4'
* To download the go packages: eg: for quote package : '**go get rsc.io/quote**'
* Go use quote module as requirement as well as go.sum file in authenticating the module.
* commmand: '**go mod tidy**': This command run the automatic search of missing packages in codebase and update to correct versions .SO, can be ued to install the used packages.
* command: **go list**: To getlist of all the installed packages.
* In Go, a function whose name starts with a capital letter can be called by a function not in the same package. This is known in Go as an exported name.
* := operator : This is a shortcut for declaring and initializing a variable in one line
```
with := operator:
message := fmt.Sprintf("Hi, %v. Welcome!", name)
```
```
without the := operator:
var message string
message = fmt.Sprintf("Hi, %v. Welcome!", name)
```
* local and git folder dependency: As go.mod file manage dependency. Adding example.con/file1 will add dependency folders in example.com and ca nbe used for live projects. But,for running locally need to change it to local filewith:
```
go mod edit -replace example.com/greetings=../greetings   //greetings is dependant folder her. 
```
After this goto the file which is calling the greetigs from cmd and run below command to get the dependencies of the run file:
```
go mod tidy
```
* To run a file goto folder and run: 
```
go run .
```







### A small project repo with 2 directories: Greetings(with greetings.go file) and hello(with hello.go file) and a go.mod file.

the greetings.go file have the function implementation and hello.go file have the callers for greetings.go file.

#### calling one module function from other module by importing. And, handeling errors:

![image](https://github.com/adarshraj99/GoLang-Terratest-Azure-DataBricks.md/assets/122180050/966bc4e2-f751-4962-b817-ea7096d84278)
![image](https://github.com/adarshraj99/GoLang-Terratest-Azure-DataBricks.md/assets/122180050/4d29a07c-9930-47f5-a306-820b4dfcf8e1)


#### Use of slicing to print outputs at random:  

![image](https://github.com/adarshraj99/GoLang-Terratest-Azure-DataBricks.md/assets/122180050/885d2060-ab71-4e8f-96b8-da883447c1b2)

hello.go will be same file as previous.

outputs: after running the hello.go file 3 times. (as it is random outputs may vary): 

![image](https://github.com/adarshraj99/GoLang-Terratest-Azure-DataBricks.md/assets/122180050/6ce52c04-1344-484f-8fda-44ddab3af61b)

![image](https://github.com/adarshraj99/GoLang-Terratest-Azure-DataBricks.md/assets/122180050/6f152308-ad7a-4db9-931e-83a961b8d16a)






