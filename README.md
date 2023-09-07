[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11754814&assignment_repo_type=AssignmentRepo)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

This function finds the highest valued number by first recursively slicing the array until it only has one 
element, and then it goes back up the recursive calls where the array was sliced with a different element at the 0th position, 
and compares the foo element with the 0th element. In the first comparison foo is the last element of the original array and then it 
becomes the highest valued number at that specific recursive call.