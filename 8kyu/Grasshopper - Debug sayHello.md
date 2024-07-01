# CodeWars Bash Solutions

---

## Grasshopper - Debug sayHello


Debugging sayHello function
The starship Enterprise has run into some problem when creating a program to greet everyone as they come aboard. It is your job to fix the code and get the program working again!
---
```
Hello, Mr. Spock
```

### Given Code

```Bash
def testit(arg)
  output = run_shell args: [arg]
  describe 'Basic tests' do
     it "Hello, #{arg}" do
       expect(output).to include("Hello, #{arg}")
     end
   end
end
testit("Mr. Spock")
testit("Captain Kirk")
testit("Liutenant Uhura")
testit("Dr. McCoy")
testit("Mr. Scott")

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


[See on CodeWars.com](https://www.codewars.com/kata/5625618b1fe21ab49f00001f/train/shell)