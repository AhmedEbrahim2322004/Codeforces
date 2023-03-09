Tag:  #syntax

## Comments

```php
  // (//)    single line comment
  // (#)     single line comment
  // (/**/)  multiple line comment
```

## Print statements

**Note: PHP keywords are NOT case sensitive**

   ```php
echo "ahmed";
print "ahmed";
```

**Heredoc** : used to print a block code that contain a lot of elements need to escaping + parsing

```php        
echo <<< "var"
	//Code
var;
```

```php
//EX:
    $name = "ahmed";
    echo <<< "var"
        <ul>
            <li>$name\\</li>
            <li>$name\\</li>
        </ul>
    var;
```

**Nowdoc** : used to print a block code that contain a lot of elements need to escaping
```php
echo <<< 'var'
	//Code
var;
```

```php
//EX:
    echo <<< 'var'
    <ul>
        <li>$name\\</li>
        <li>$name\\</li>
    </ul>
    var;
```

**Note**: ("") -> do parsing and ('') Not

---

## [[Data types]]

same as [[Data types]]

#### Bool 
- true  = 1 *or* any number expect (0)
- false = 0 *or* empty(array,string,...)
```php
 gettype(var)  // return the type of var
 var_dump(var) // print the type of the var
```

  ---
  
## Casting

#### Automatic casting

```php
int + (bool,string) = int
double + (int,bool,string) = double
bool + bool = int
```

#### Type casting
- same as c/c++

---

## [[Variables]]
   - Variables in PHP start with ==**($)**==
   - Variables name should start with (a->z) , (A->Z) , (under score) _
```php
	$name = "ahmed";
```

#### Variable Variable
- Variable Variable take the value of a Variable and use it as a name of another Variable
```php
   $a = "Ahmed";
   $$a = "Ebrahim";
   $$$a = "lotfy";
   echo "Hello, $a $Ahmed $Ebrahim <br>"; // Ahmed Ebrahim lotfy
   echo "Hello, $a ${$a} ${$$a} <br>";    // Ahmed Ebrahim lotfy
 ```

#### Assign by Reference

```php
	$a = "ahmed";
	$b = $a;
	echo "$a $b<br>"; // ahmed ahmed
	$a = "ahmed";
	$b = &$a;
	$b = "mohamed"; // or $a = "mohamed";
	echo "$a $b<br>"; // mohamed mohamed
```
    

---

## [[Constants]]

- Constants are declared by 
```php  
define("Varname",Value)
```
- `Varname` should be uppercase

---

## [[Conditions]]
---
## [[Array]]
- **Note**: array in PHP is 0 based indexing
- we can assign keys for the array elements                 
```php
	["A"=>"ahmed","B"=>"bob","mo"] // mo is index 0
```

- when we assign a numirical key the array continue from it  
```php
	[4=>"ahmed","bob"] //bob index is 5
```

- we can put an array in an array                            
```php
	[4=>"ahmed","numbers"=>["1","2","3"]]
```

- if you assigned the same key for two elements the last element will override

```php
	print_r() // print the array with its information
``` 

```php
    echo "<pre>";
    print_r(["A"=>"ahmed","B"=>"bob","carl","le",9=>"oh","mo"]);
    echo "</pre>";
    
    echo "<pre>";
    print_r([4=>"ahmed","numbers"=>["1","2","3"]]);
    echo "</pre>";
```

---

## Operators

#### Arithmetic operators

- ``(+,-,/,*,%)`` same as c/c++
	**Note:** in division if we divide int over int it can return float
- ``(**)`` is the exponent operator
- (+) before a numerical string convert it to
- (-) before a numerical string convert it to -int (+ > -),(- > +)
```php
    $c = "200";
    echo "<br>";
    echo +"100";
    echo gettype(+"100");
    echo "<br>";
    echo -$c;
    echo gettype(-$c);
    echo "<br>";
```

#### comparison operators

- (`==`) equal return true if the two element are equal no matter what is the type
```php
	(1=="1") -> true
``` 

- (!=) not equal return true if the two element are not equal in value
```php
	(1!=1.0) -> false
```

- (<>) not equal , the same as (!=)

- ``(===)`` identical return true if the two element are equal in value and data type EX: 
```php
	(1===1.0) -> false
```

- ``(!==)`` identical return true if the two element are not equal in value or data type

- (>,<,>=,<=) same as c/c++

- (<=>) spaceship return 
```php
	-1 -> if the first is smaller than the secound EX: (1<=>2) -> -1
	 0 -> if equal                                 EX: (1<=>1) ->  0
	 1 -> if the first is greater than the secound EX: (1<=>0) ->  1
```

#### Logical operators

- (&&) == (and)
- (||) == (or)
- ! not operator
 - xor return true if one or more is true but not all 
```php
 (true xor true)-> FALSE 
 (true xor false)-> TRUE
```
 
####String operators
- (.) concatenate strings with each other with no spaces
- (.=) concatenate strings with each other with no spaces int the same variable
- 
```php
    $x = "Ahmed"." "."Ebrahim";
    echo $x."<br>";
    $y = "Ahmed";
    $y .= " Ebrahim"; // $y = $y . " Ebrahim"
    echo $y;
```

#### Array operators
- (+) Union marge two arrays in one
- ``(==)`` Equal return true if the two arrays have the same value for the same key
- (!=) Not Equal
- ``(===)`` identical return true if the two arrays have the same order of keys and have same datatype for values
- ``(!==)`` Not identical

---

## [[loops]]

#### Foreach
```php
foreach($array as $counter(value)){
	//code
}
foreach($array as $key => $counter(value)){
	//code
}
```

---

## Recourses
- Elzero web school (YouTube playlist)
