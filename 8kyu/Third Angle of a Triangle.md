# CodeWars Bash Solutions

---

## Third Angle of a Triangle


You are given two interior angles (in degrees) of a triangle.

Write a function to return the 3rd.

Note: only positive integers will be tested.

https://en.wikipedia.org/wiki/Triangle

### Given Code

```Bash
def other_angle(a, b)
  (run_shell args: [a, b]).to_i
end
describe "Fixed tests" do
  it "Testing for 30 and 60" do expect(other_angle(30, 60)).to eq(90) end
  it "Testing for 60 and 60" do expect(other_angle(60, 60)).to eq(60) end
  it "Testing for 43 and 78" do expect(other_angle(43, 78)).to eq(59) end
  it "Testing for 10 and 20" do expect(other_angle(10, 20)).to eq(150) end
end

```

---

### Solution

```Bash
a=$1
b=$2
echo $((180-a-b))
```


[See on CodeWars.com](https://www.codewars.com/kata/5a023c426975981341000014/train/shell)