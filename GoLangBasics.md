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







#### A small project repo with 2 directories: Greetings(with greetings.go file) and hello(with hello.go file) and a go.mod file.
the greetings.go file have the function implementation and hello.go file have the callers for greetings.go file.
![image](https://github.com/adarshraj99/GoLang-Terratest-Azure-DataBricks.md/assets/122180050/7e3c6cb6-b343-4ef1-8228-a2642f6d1392)


greetings.go file: 
```
package greetings
//import fmt
import(
    "errors" //Standard Go library to use with errors
    "fmt"
)

// Hello returns a greeting for the named person.
func Hello(name string) (string, error) string {
    // Return a greeting that embeds the name in a message.
    // If no name was given return an error with a message.
    if name == ""{
        return "", errors.New("empty name") //errors.new function takes a string message and returns an error value.
    }
    message := fmt.Sprintf("Hi, %v. Welcome!", name)
    return message, nil //Go can do multiple returns. nil(no error) here is an output of the successful return. Helps the caller function to see the success return.
}
```
hello.go file: 
```
package main
import(
    "fmt"
    "example.com/greetings"
    "log" //To log errors
)
func main(){
    //Set properties of the predefines logger. To print error message prefix, to disable printing, time, file source, line number.
    log.SetPrefix("greetings: ")
    log.SetFlags(0)
    //get a greeting message and print it.
    message, err := greetings.Hello("Adarsh") //error will occur if this found empty.
    // if error occurs print to console and exit program.
    if err != nil {
        log.Fatal(err)
    }
    // If no error was returned, print the returned message to console.message
    fmt.Println(message)
}
```

