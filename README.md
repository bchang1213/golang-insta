# Sorter Example

## How to run & test project? 

Install Dependencies

<i>Go/Dep install steps will be different for pc</i>
```
#if you need homebrew
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
#else 
brew update

brew install go
brew install dep
brew install fswatch
```

Clone the project
``` 
cd $GOPATH
cd go/src
open .
```

In the opened window put the unzipped folder here. You could also mv the folder from your downloads here.

Install/Update vendor files
``` 
#back in terminal
cd dep-ex
dep ensure
```

Run project w/ file watching 
```
make dev
# go to http://localhost:8080
```

Run project w/ out file watching
```
go run cmd/main.go
# go to http://localhost:8080
```

Test project
```
make test
```

# Your Task
## Overview
From the form on page http://localhost:8080/ display their info on the page POST http://localhost:8080/instagram.

Info to display:
* The tag that was searched.
* At least 5 recent pictures with captions.

## Specifics
* Style the page http://localhost:8080/

* In the internal/routes file routes.go route the action at path "/instagram" to the handler method at internal/handlers/index.go:Instagram

* In the internal/handlers file index.go, call utility methods and pass those variables to the template instagram.gohtml.

* In the pkg/utilities file InstagramUtility.go, write a GET request to Instagram and pass that object to the handler.

* Write a unit test for your get Instagram method.
* In the internal/client/templates file instagram.gohtml render a page entirely from jQuery.
