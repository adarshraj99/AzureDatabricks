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
