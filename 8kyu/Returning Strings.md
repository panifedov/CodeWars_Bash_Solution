# CodeWars Bash Solutions

---

## Returning Strings

Make a function that will return a greeting statement that uses an input; your program should return, "Hello, <name> how are you doing today?".

[Make sure you type the exact thing I wrote or the program may not execute properly]
---


### Given Code

```Bash
# run the solution and store its result
 output = run_shell args: ['shell']

 describe "sample test" do
   it "should return \"Hello, <name> how are you doing today?\"" do
     expect(output).to eq('Hello, shell how are you doing today?')
   end
 end

```

---

### Solution

```Bash
#!/bin/bash

greet() {
  local name=$1
  echo "Hello, $name how are you doing today?"
}


if [ -z "$1" ]; then
  echo "Usage: $0 <name>"
  exit 1
fi


greet "$1"

```


[See on CodeWars.com](https://www.codewars.com/kata/55a70521798b14d4750000a4/train/shell)