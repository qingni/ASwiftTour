<img src="https://swift.org/assets/images/swift.svg" alt="Swift logo" height="70" >

# The Swift Programming Language 

> 相关资源的整理：[https://github.com/ShannonChenCHN/iOSDevLevelingUp/issues/14](https://github.com/ShannonChenCHN/iOSDevLevelingUp/issues/14)

## Contents
- [The Basics](#the-basics)
- [Basic Operators](#basic-operators)
- [Strings and Characters](#strings-and-characters)
- [Collection Types](#collection-types)
- [Control Flow](#control-flow)
- [Functions](#functions)
- [Closures](#closures)
- [Enumerations](#enumerations)
- [Classes and Structures](#classes-and-structures)
- [Properties](#properties)
- [Methods](#methods)
- [Subscripts](#subscripts)
- [Inheritance](#inheritance)
- [Initialization](#initialization)
- [Deinitialization](#deinitialization)
- [Automatic Reference Counting](#automatic-reference-counting)
- [Optional Chaining](#optional-chaining)
- [Error Handling](#error-handling)
- [Type Casting](#type-casting)
- [Nested Types](#nested-types)
- [Extensions](#extensions)
- [Protocols](#protocols)
- [Generics](#generics)
- [Access Control](#access-control)
- [Advanced Operators](#advanced-operators)


## [The Basics](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID309)
- Overview
    - Fundamental C and Objective-C Types(Int, Double, Float, Bool, String, Array, Set, Dictionary)
    - Variables and Constants
    - Advanced Types(like tuples)
    - Optional Types
    - Type Safety
- Constants and Variables
    - Declaring Constants and Variables
        - Constants
        - Variables
    - Type Annotations
        - What is Type Annotations
        - When to Use
    - Naming Constants and Variables
        - Can Contain
        - Cannot Contain
    - Printing Constants and Variables
        - Function for Print
        - String Interpolation

- Comments
    - Single-line comments
    - Multiline comments

- Semicolons
    - When to Use

- Integers
    - What is Integer
        - Definition
        - Signed and Unsigned 
        - Bit Forms(8, 16, 32, 64)
    - Integer Bounds
    - Int
        - Int Type is a Value Type(Structure)
        - Size
        - When to Use
    - UInt
        - Size
        - When to Use

- Floating-Point Numbers
    - Double
    - Float

- Type Safety and Type Inference
    - Type Safety
    - Type Inference

- Numeric Literals
    - Integer literals
        - decimal 
        - binary
        - octal
        - hexadecimal
    - Floating-point literals
        - decimal
        - hexadecimal
        - exponent

- Numeric Type Conversion
    - Integer Conversion
    - Integer and Floating-Point Conversion
    
- Type Aliases
    
- Booleans

- Tuples
    - What is Tuples
    - Creating a Tuple
    - Decompose

- Optionals
    - What is Optionals
    - How about Optionals in C or Objective-C
    - nil in Swift and Objective-C
    - If Statements and Forced Unwrapping
    - Optional Binding
    - Implicitly Unwrapped Optionals

- Error Handling
    - What is Error Handling
    - Do, Try, Catch and Throws 

- Assertions
    - What is Assertions
    - Debugging with Assertions
    - When to Use

## [Basic Operators](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-ID60)
- Overview
    - What is Operator
    - What Beyond C
        - Assignment Operator
        - Detecting and Disallowing Value Overflow
        - Range Operators
        - Advanced Operators

- Terminology
    - Unary
    - Binary
    - Ternary

- Assignment Operator(`=`)
    - The assignment operator in Swift does not itself return a value

- Arithmetic Operators
    - Addition(`+`)
        - String Concatenation(`"a" + "b"`)
    - Substraction(`-`)
    - Multiplication(`*`)
    - Division(`/`)
    - Disallowing Overflow
    - Remainder Operator(`%`)
    - Unary Minus Operator
    - Unary Plus Operator

- Compound Assignment Operators
    - Combine Assignment (`=`) with Another Operation
    - `++` is not supported in Swift

> **Note**                       
For a complete list of the compound assignment operators provided by the Swift standard library, see *[Swift Standard Library Operators Reference](https://developer.apple.com/reference/swift/swift_standard_library_operators)*.

- Comparison Operators
    - Swift supports all standard C comparison operators
        - Equal to (`a == b`)
        - Not equal to (`a != b`)
        - Greater than (`a > b`)
        - Less than (`a < b`)
        - Greater than or equal to (`a >= b`)
        - Less than or equal to (`a <= b`)
    - Swift also provides two identity operators (`===` and `!==`) for object Comparison
    - Tuple Comparison

- Ternary Conditional Operator
    - Form: `question ? answer1 : answer2`
    - Use the ternary conditional operator with care

- Nil-Coalescing Operator
    - Form: `a ?? b`
    - Underlying Expression: ` a != nil ? a! : b`

- Range Operators
    - Closed Range Operator(`a...b`)
    - Half-Open Range Operator(`a..<b`)

- Logical Operators
    - Logical operators modify or combine the **Boolean** logic values true and false
    - Logical NOT Operator(`!a`)
    - Logical AND Operator(`a && b`)
    - Logical OR Operator(`a || b`)
    - Combining Logical Operators: The Swift logical operators `&&` and `||` are left-associative
    - Readability is always preferred over brevity, use parentheses where they help to make your intentions clear

## [Strings and Characters](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-ID285)
- Overview
    - What is String
    - Unicode-compliant
    - Lightweight and Readable in Syntax
    - String Concatenation
    - String Interpolation
    - Every string is composed of encoding-independent Unicode characters
    - Swift’s String type is bridged with Foundation’s NSString class

- String Literals

- Initializing an Empty String
    - Assign an empty string literal to a variable(`var emptyString = ""`)
    - Initialize a new `String` instance with initializer syntax(`var anotherEmptyString = String()`)

- String Mutability
    - Variable -> Mutable(`var variableString = "Horse"`)
    - Constant -> Immutable(`let constantString = "Highlander"`)

- Strings Are Value Types
    - Copy-by-default String behavior
    - Swift’s compiler optimization on copying

- Working with Characters
    - String -> Characters：Access the individual `Character` values by `String`'s property `characters`
    - Characters -> String: `String` values can be constructed by passing an array of Character values as an argument to its initializer

- Concatenating Strings and Characters
    - Add `String` values together with operator `+`
    - Append a `String` value to a `String` by using operator `+=`
    - Append a `Character` value to a `String` bu using `append()` method

- String Interpolation
    > “*String interpolation* is a way to construct a new `String` value from a mix of constants, variables, literals, and expressions by including their values inside a string literal. "

- Unicode
    - What is Unicode?
        > Unicode is an international standard for encoding, representing, and processing text in different writing systems. It enables you to represent almost any character from any language in a standardized form, and to read and write those characters to and from an external source such as a text file or web page. 
    - Unicode Scalars
        - Swift’s native String type is built from Unicode scalar values
        - A Unicode scalar is a unique 21-bit number for a character or modifier
    - Special Characters in String Literals
        - String literals can include the following special characters
            - The escaped special characters `\0` (null character), `\\` (backslash), `\t` (horizontal tab), `\n` (line feed), `\r` (carriage return), `\"` (double quote) and `\'` (single quote)
            - An arbitrary Unicode scalar, written as `\u{n}`, where `n` is a 1–8 digit hexadecimal number with a value equal to a valid Unicode code point
    - Extended Grapheme Clusters
        - Every instance of Swift’s `Character` type represents a single extended grapheme cluster
        - An extended grapheme cluster is a sequence of one or more Unicode scalars that (when combined) produce a single human-readable character

- Counting Characters
    - To retrieve a count of the Character values in a string, use the count property of the string’s characters property
    - Swift’s use of extended grapheme clusters for Character values means that string concatenation and modification may not always affect a string’s character count

- Accessing and Modifying a String
    - String Indices
        - Each `String `value has an associated index type, `String.Index`, which corresponds to the position of each `Character` in the string
        - Swift strings cannot be indexed by integer values
        - Properties and Methods: `endIndex`, `startIndex`, `indices`, `index(before:)`, `index(after:)`, `index(_:offsetBy:)`
    - Inserting and Removing
        - Methods: `insert(_:at:)`, `insert(contentsOf:at:)`, `remove(at:)`, `removeSubrange(_:)`

- Comparing Strings
    - String and Character Equality(`==`, `!=`)
    - Prefix and Suffix Equality(` hasPrefix(_:)`, `hasSuffix(_:)`)
    > Two String values (or two Character values) are considered equal if their extended grapheme clusters are canonically equivalent. Extended grapheme clusters are canonically equivalent if they have the same linguistic meaning and appearance, even if they are composed from different Unicode scalars behind the scenes.
- Unicode Representations of Strings
    - UTF-8 Representation
    - UTF-16 Representation
    - Unicode Scalar Representation

## [Collection Types](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/CollectionTypes.html#//apple_ref/doc/uid/TP40014097-CH8-ID105)
- Generic Collections
    - What is generic type
- Mutability of Collections
    - Variable -> Mutable
    - Constant -> Immutable
    - It is good practice to create immutable collections in all cases where the collection does not need to change
- Arrays
    - Swift’s `Array` type is bridged to Foundation’s `NSArray` class.
    - Array Type Shorthand Syntax
        - Array type: `Array<Element>`
        - Array Type Shorthand: `[Element]`
    - Creating an Empty Array(`var someInts = [Int]()`)

    - Creating an Array with a Default Value(`var threeDoubles = Array(repeating: 0.0, count: 3)`)
    - Creating an Array by Adding Two Arrays Together
        - Using addition operator (+)
    - Creating an Array with an Array Literal(`[value 1, value 2, value 3]`)
    - Accessing and Modifying an Array
        - `count`
        - `isEmpty`
        - `append(_:)` : add new item
        - `+=` :  append an array
        - `var firstItem = shoppingList[0]`:
        - `shoppingList[0] = "Six eggs"`
        - `shoppingList[4...6] = ["Bananas", "Apples"]`
        - `shoppingList.insert("Maple Syrup", at: 0)`
        - `let mapleSyrup = shoppingList.remove(at: 0)`
        - `let apples = shoppingList.removeLast()`
    - Iterating Over an Array
        - Normal Iteration
        - `enumerated()` method

- Sets
    - Swift’s `Set` type is bridged to Foundation’s `NSSet` class.
    - Hash Values for Set Types: A type must be hashable in order to be stored in a set
    - Set Type Syntax: `Set<Element>`
    - Creating and Initializing an Empty Set(`var letters = Set<Character>()`)
    - Creating a Set with an Array Literal(`var favoriteGenres: Set<String> = ["Rock”]`)
    - Accessing and Modifying a Set
        - `count`
        - `isEmpty`
        - `insert(_:)`
        - `remove(_:)`
        - `removeAll()`
        - `contains(_:)`
    - Iterating Over a Set
        -  use the `sorted()` method

- Performing Set Operations
    - Fundamental Set Operations
        - `intersection(_:)` 
        - `symmetricDifference(_:)` 
        - `union(_:)`
        - `subtracting(_:)`
    - Set Membership and Equality
        - “is equal” operator (`==`) 
        - `isSubset(of:)`
        - `isSuperset(of:)`
        - `isStrictSubset(of:)` and `isStrictSuperset(of:)`
        - `isDisjoint(with:)`

- Dictionaries
    - Swift’s `Dictionary` type is bridged to Foundation’s `NSDictionary` class.
    - Dictionary Type Shorthand Syntax
        - Full form: `Dictionary<Key, Value>`
        - Shorthand form: `[Key: Value]`
    - Creating an Empty Dictionary(`var namesOfIntegers = [Int: String]()`)
    - Creating a Dictionary with a Dictionary Literal(`[key 1: value 1, key 2: value 2, key 3: value 3]`)
    - Accessing and Modifying a Dictionary
        - `count`
        - `isEmpty`
        - `airports["LHR"] = "London"`
        - `updateValue(_:forKey:) `
        - `let airportName = airports["DUB"]`
        - `airports["DUB"] = nil`
        - `removeValue(forKey:)`
    - Iterating Over a Dictionary
        - iterate over the key-value pairs in a dictionary with a for-in loop
        - `keys` and `values`
        - `sorted()`


## [Control Flow](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID120)
- For-In Loops
    - Usage: Iterate over a sequence, such as ranges of numbers, items in an array, or characters in a string
    - Ignore the values by using an underscore in place of a variable name

- While Loops
    - `While`
    - `Repeat-While`

- Conditional Statements
    - If
    - Switch
        - No Implicit Fallthrough
            - `switch` statements not fall through the bottom of each case and into the next one by default.
            - The body of each case must contain at least one executable statement.
        - Interval Matching(`case: 1..<5:`)
        - Tuples
            - Wild pattern: underscore character (`case (_, 0):`)
            - If multiple matches are possible, the first matching case is always used.
        - Value Bindings(`case (0, let y):`)
        - Where(`case let (x, y) where x == y:`)
        - Compound Cases(`case "a", "e":`)

- Control Transfer Statements
    - Continue
    - Break
        - Break in a Loop Statement
        - Break in a Switch Statement
            > Because Swift’s switch statement is exhaustive and does not allow empty cases, it is sometimes necessary to deliberately match and ignore a case in order to make your intentions explicit. You do this by writing the break statement as the entire body of the case you want to ignore.
    - Fallthrough
        > Note: The fallthrough keyword does not check the case conditions for the switch case that it causes execution to fall into. 
    - Labeled Statements
        -  if you have multiple nested loops, it can be useful to be explicit about which loop the continue statement should affect.
        - Usage: mark a loop statement or conditional statement with a statement label. 
- Early Exit
    - You use a `guard` statement to require that a condition must be true in order for the code after the guard statement to be executed.
    - Any variables or constants that were assigned values using an optional binding as part of the condition are available for the rest of the code block that the `guard` statement appears in.
- Checking API Availability
    - Availability condition: `if #available(platform name version, ..., *)`

## [Functions](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Functions.html#//apple_ref/doc/uid/TP40014097-CH10-ID158)

- Defining and Calling Functions
    ```
    func greet(person: String) -> String {}
    ```

- Function Parameters and Return Values
    - Functions Without Parameters
    ```
        func sayHelloWorld() -> String {}
    ```
    - Functions With Multiple Parameters
    ```
        func greet(person: String, alreadyGreeted: Bool) -> String {}
    ```
    - Functions Without Return Values
    > Functions without a defined return type return a special value of type Void. This is simply an empty tuple, which is written as ().
    - Functions with Multiple Return Values
        - Use a **tuple** type as the return type
        - Because the tuple’s member values are named as part of the function’s return type, they can be accessed with dot syntax.
    - Optional Tuple Return Types
        - Placing a question mark after the tuple type’s closing parenthesis, `(Int, Int)? `
        - An optional tuple type such as (Int, Int)? is different from a tuple that contains optional types such as (Int?, Int?)

- Function Argument Labels and Parameter Names
    - General rules
        - Each function parameter has both an argument label and a parameter name.
        - The **argument label** is used when calling the function
        - The **parameter name** is used in the implementation of the function
        - By default, parameters use their parameter name as their argument label
    - Specifying Argument Labels
        ``` func greet(person: String, from hometown: String) -> String {}
            print(greet(person: "Bill", from: "Cupertino"))
        ```
    - Omitting Argument Labels
        ``` func someFunction(_ firstParameterName: Int, secondParameterName: Int) {}
            someFunction(1, secondParameterName: 2)
        ```
    - Default Parameter Values
        - Assigning a value to the parameter after that parameter’s type
        - If a default value is defined, you can omit that parameter when calling the function.
        ```
        func someFunction(parameterWithoutDefault: Int, parameterWithDefault: Int = 12) {}
        someFunction(parameterWithoutDefault: 3, parameterWithDefault: 6)
        someFunction(parameterWithoutDefault: 6)
        ```

    - Variadic Parameters
        - A variadic parameter accepts zero or more values of a specified type
        - Write variadic parameters by inserting three period characters (...) after the parameter’s type name
        - The values passed to a variadic parameter are made available within the function’s body as an array of the appropriate type
        - A function may have at most one variadic parameter
    - In-Out Parameters
        - Function parameters are constants by default
        - If you want a function to modify a parameter’s value, and you want those changes to persist after the function call has ended, define that parameter as an in-out parameter instead
        - You write an in-out parameter by placing the `inout` keyword right before a parameter’s type
        - You can only pass a **variable** as the argument for an in-out parameter. You cannot pass a constant or a literal value as the argument
        - You place an ampersand (&) directly before a variable’s name when you pass it as an argument to an in-out parameter
        - In-out parameters cannot have default values, and variadic parameters cannot be marked as `inout`

- Function Types
    - General rules
        - Every function has a specific function type, made up of the parameter types and the return type of the function
        - The type of the function below is `() -> Void`
        ```
        func printHelloWorld() {
            print("hello, world")
        }
        ```
    - Using Function Types
        - You use function types just like any other types in Swift.
        ```
            var mathFunction: (Int, Int) -> Int = addTwoInts
        ```
    - Function Types as Parameter Types
        ``` func printMathResult(_ mathFunction: (Int, Int) -> Int, _ a: Int, _ b: Int) { } ```
    - Function Types as Return Types
        ```
        func chooseStepFunction(backward: Bool) -> (Int) -> Int {
            return backward ? stepBackward : stepForward
        }
        ```
- Nested Functions

## [Closures](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html#//apple_ref/doc/uid/TP40014097-CH11-ID94)

- Closure Expressions
    - The Sorted Method
    - Closure Expression Syntax
    - Inferring Type From Context
    - Implicit Returns from Single-Expression Closures
    - Shorthand Argument Names
    - Operator Methods
- Trailing Closures
- Capturing Values
- Closures Are Reference Types
- Escaping Closures
- Autoclosures

## [Enumerations](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Enumerations.html#//apple_ref/doc/uid/TP40014097-CH12-ID145)
- Enumeration Syntax
- Matching Enumeration Values with a Switch Statement
- Associated Values
- Raw Values
    - Implicitly Assigned Raw Values
    - Initializing from a Raw Value
- Recursive Enumerations

## [Classes and Structures](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/ClassesAndStructures.html#//apple_ref/doc/uid/TP40014097-CH13-ID82)
- Comparing Classes and Structures
    - Definition Syntax
    - Class and Structure Instances
    - Accessing Properties
    - Memberwise Initializers for Structure Types
- Structures and Enumerations Are Value Types
- Classes Are Reference Types
    - Identity Operators
    - Pointers
- Choosing Between Classes and Structures
- Assignment and Copy Behavior for Strings, Arrays, and Dictionaries
    


## [Properties](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Properties.html#//apple_ref/doc/uid/TP40014097-CH14-ID254)
- Stored Properties
    - Stored Properties of Constant Structure Instances
    - Lazy Stored Properties
    - Stored Properties and Instance Variables
- Computed Properties
    - Shorthand Setter Declaration
    - Read-Only Computed Properties
- Property Observers
- Global and Local Variables
- Type Properties
    - Type Property Syntax
    - Querying and Setting Type Properties

## [Methods](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Methods.html#//apple_ref/doc/uid/TP40014097-CH15-ID234)
- Instance Methods
    - The self Property
    - Modifying Value Types from Within Instance Methods
    - Assigning to self Within a Mutating Method
- Type Methods


## [Subscripts](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Subscripts.html#//apple_ref/doc/uid/TP40014097-CH16-ID305)
- Subscript Syntax
- Subscript Usage
- Subscript Options


## [Inheritance](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Inheritance.html#//apple_ref/doc/uid/TP40014097-CH17-ID193)
- Defining a Base Class
- Subclassing
- Overriding
    - Accessing Superclass Methods, Properties, and Subscripts
    - Overriding Methods
    - Overriding Properties
        - Overriding Property Getters and Setters
        - Overriding Property Observers
    - Preventing Overrides

## [Initialization](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-ID203)
- Setting Initial Values for Stored Properties
    - Initializers
    - Default Property Values
- Customizing Initialization
    - Initialization Parameters
    - Parameter Names and Argument Labels
    - Initializer Parameters Without Argument Labels
    - Optional Property Types
    - Assigning Constant Properties During Initialization
- Default Initializers
    - Memberwise Initializers for Structure Types
- Initializer Delegation for Value Types
- Class Inheritance and Initialization
    - Designated Initializers and Convenience Initializers
    - Syntax for Designated and Convenience Initializers
    - Initializer Delegation for Class Types
    - Two-Phase Initialization
    - Initializer Inheritance and Overriding
    - Automatic Initializer Inheritance
    - Designated and Convenience Initializers in Action
- Failable Initializers
    - What is Failable Initializers
    - Failable Initializers for Enumerations
    - Failable Initializers for Enumerations with Raw Values
    - Propagation of Initialization Failure
    - Overriding a Failable Initializer
    - The init! Failable Initializer
- Required Initializers
- Setting a Default Property Value with a Closure or Function

## [Deinitialization](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Deinitialization.html#//apple_ref/doc/uid/TP40014097-CH19-ID142)
- How Deinitialization Works
- Deinitializers in Action

## [Automatic Reference Counting](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AutomaticReferenceCounting.html#//apple_ref/doc/uid/TP40014097-CH20-ID48)
- How ARC Works
- ARC in Action
- Strong Reference Cycles Between Class Instances
- Resolving Strong Reference Cycles Between Class Instances
    - Weak References
    - Unowned References
    - Unowned References and Implicitly Unwrapped Optional Properties
- Strong Reference Cycles for Closures
- Resolving Strong Reference Cycles for Closures
    - Defining a Capture List
    - Weak and Unowned References

## [Optional Chaining](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/OptionalChaining.html#//apple_ref/doc/uid/TP40014097-CH21-ID245)
- Optional Chaining as an Alternative to Forced Unwrapping
- Defining Model Classes for Optional Chaining
- Accessing Properties Through Optional Chaining
- Calling Methods Through Optional Chaining
- Accessing Subscripts Through Optional Chaining
    - Accessing Subscripts of Optional Type
- Linking Multiple Levels of Chaining
- Chaining on Methods with Optional Return Values


## [Error Handling](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/ErrorHandling.html#//apple_ref/doc/uid/TP40014097-CH42-ID508)
- Representing and Throwing Errors
- Handling Errors
    - Propagating Errors Using Throwing Functions
    - Handling Errors Using Do-Catch
    - Converting Errors to Optional Values
    - Disabling Error Propagation
    - Specifying Cleanup Actions


## [Type Casting](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/TypeCasting.html#//apple_ref/doc/uid/TP40014097-CH22-ID338)
- Defining a Class Hierarchy for Type Casting
- Checking Type
- Downcasting
- Type Casting for Any and AnyObject


## [Nested Types](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/NestedTypes.html#//apple_ref/doc/uid/TP40014097-CH23-ID242)
- Nested Types in Action
- Referring to Nested Types


## [Extensions](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Extensions.html#//apple_ref/doc/uid/TP40014097-CH24-ID151)
- Extension Syntax
- Computed Properties
- Initializers
- Methods
    - Mutating Instance Methods
- Subscripts
- Nested Types


## [Protocols](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-ID267)
- Protocol Syntax
- Property Requirements
- Method Requirements
- Mutating Method Requirements
- Initializer Requirements
    - Class Implementations of Protocol Initializer Requirements
    - Failable Initializer Requirements
- Protocols as Types
- Delegation
- Adding Protocol Conformance with an Extension
    - Declaring Protocol Adoption with an Extension
- Collections of Protocol Types
- Protocol Inheritance
- Class-Only Protocols
- Protocol Composition
- Checking for Protocol Conformance
- Optional Protocol Requirements
- Protocol Extensions
    - Providing Default Implementations
    - Adding Constraints to Protocol Extensions

## [Generics](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID179)
- The Problem That Generics Solve
- Generic Functions
- Type Parameters
- Naming Type Parameters
- Generic Types
- Extending a Generic Type
- Type Constraints
    - Type Constraint Syntax
    - Type Constraints in Action
- Associated Types
    - Associated Types in Action
    - Extending an Existing Type to Specify an Associated Type
- Generic Where Clauses
- Extensions with a Generic Where Clause

## [Access Control](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AccessControl.html#//apple_ref/doc/uid/TP40014097-CH41-ID3)
- Modules and Source Files
- Access Levels
    - Guiding Principle of Access Levels
    - Default Access Levels
    - Access Levels for Single-Target Apps
    - Access Levels for Frameworks
    - Access Levels for Unit Test Targets
- Access Control Syntax
- Custom Types
    - Tuple Types
    - Function Types
    - Enumeration Types
        - Raw Values and Associated Values
    - Nested Types
- Subclassing
- Constants, Variables, Properties, and Subscripts
    - Getters and Setters
- Initializers
    - Default Initializers
    - Default Memberwise Initializers for Structure Types
- Protocols
    - Protocol Inheritance
    - Protocol Conformance
- Extensions
    - Adding Protocol Conformance with an Extension
- Generics
- Type Aliases


## [Advanced Operators](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-ID28)
- Bitwise Operators
    - Bitwise NOT Operator
    - Bitwise AND Operator
    - Bitwise OR Operator
    - Bitwise XOR Operator
    - Bitwise Left and Right Shift Operators
        - Shifting Behavior for Unsigned Integers
        - Shifting Behavior for Signed Integers
- Overflow Operators
    - Value Overflow
- Precedence and Associativity
- Operator Methods
    - Prefix and Postfix Operators
    - Compound Assignment Operators
    - Equivalence Operators
- Custom Operators
    - Precedence for Custom Infix Operators
