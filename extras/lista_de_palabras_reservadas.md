# Lista de palabras reservadas
| Palabra reservada | Descripción |
|---|----|
| `class` | Definir una clase
| `deinit` | Un desin
| `enum` 
| `extension`
| `func` 
| `import`
| `let`
| `init`
| `protocol`
| `static`
| `struct`
| `subscript`
| `typealias`
| `var`


deinit	A deinitializer is called immediately before a class instance is deallocated.
enum	defines a common type for a group of related values and enables you to work with those values in a type-safe way within your code.
extension	an extension can extend an existing type to make it adopt one or more protocols.
func	self-contained chunks of code that perform a specific task.
import	importing dependencies files.
init	an instance method with no parameters
let	define constant variable
protocol	is used to declare methods and properties that are independent of any specific class.
static	accessible without needing an instantiation of the class.
struct	defines a physically grouped list of variable to be placed under one name in a block of memory.
subscript	classes, structures, and enumerations can define subscripts, which are shortcuts for accessing the member elements of a collection, list, or sequence.
typealias	define an alternative name for an existing type
var	variable

Statements
break	
case	
continue	
default	
do	
else	
fallthrough	causes program execution to continue from one case in a switch statement to the next case.
if	
in	
for	
return	
switch	
where	
while	

Expressions and Types
as	
dynamicType	a dynamicType expression consists of an expression, mimediately follow by .dynamicType.
is	
new	
super	
self	
__COLUMN__	int, the column number in which it begins.
__FILE__	String, the name of the file in which it appears.
__FUNCTION__	String, the name of the declaration in which it appears.
__LINE__	The line number on which it appears.

Reserved in particular contexts
precedence	gives some operators higher priority then others.
associativity	operator associativity defines how operators of the same precedence are grouped together either grouped from the left, or grouped from the right.
didSet	observer is called immediately after the new value is set.
willSet	observer is called just before the value of the variable or property is set.
infix	is a binary operator that is written between its two operands, such as addition operator (+) in the expression 1+ 2.
inout	variable parameters, can only be changed within the function itself.
mutating	for a method to modify the instance it belongs to or any properties of that instance.
nonmutating	
none	
operator	an operator declaration introduces a new infix, prefix, or postfix operator into your program and is declared using the contextual keyword operator.
left	<<
right	>>
override	overriding
postfix	s a unary operator that is written immediately after its operand, such as the prefix increment operator (++) is in the expression i++.
prefix	is a unary operator that is written immediately before its operand, such as the prefix increment operator (++) is in the expression ++i.
unowned	like weak reference, but an unowned reference is assumed to always have a vale.
unowned(safe)	
unowned(unsafe)	
set	setter
get	getter