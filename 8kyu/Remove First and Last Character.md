# CodeWars Bash Solutions

---

## Remove First and Last Character


It's pretty straightforward. Your goal is to create a function that removes the first and last characters of a string. You're given one parameter, the original string. You don't have to worry about strings with less than two characters.

### Given Code

```Bash
output = run_shell args: ['abc']

 describe "Solution" do
   it "should return the argument passed in excepting the first and last characters" do
     expect(output).to eq('b')
   end
 end

```

---

### Solution

```Bash
arg=$1
echo "${arg:1:-1}"
```


[See on CodeWars.com](https://www.codewars.com/kata/56bc28ad5bdaeb48760009b0/train/shell)