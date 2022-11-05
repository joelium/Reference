# Solidity Refernce

## Version compatibility

**State Solidity version at the start**
```solidity
pragma solidity >=0.5.0 <0.6.0;
```


## Creating contracts

```solidity
contract ContractName {
	//contents
}
```


## Variabless
Syntax
> datatype variableName = value;

```solidity
contract ContractName {
	// This will create an variable permanently stored on the blockchain
	uint myVariableName = 100;
}
```


## Functions
Syntax
```solidity
function functionName(datatype stored** _parameterName, datatype stored** _parameterName, ...) functionAccess*** {
	//function body
}
```
** Only required for reference types: arrays, structures, mappings, strings. Options: memory, ###  
*** "public": Can be used by other contracts, "private": Can only be used by your contract.
    Functions are public by default.

Example:  

```solidity
function myFunction(string memory _varName1, uint _varName2) public {
	//function body
}
```


## Data types

**uint**  
Unsigned integer. Alias for uint256, a 256-bit unsigned integer.  

**Arrays**  
Public - Public arravs can be read from by other contracts

Fixed array - fixed length array

```solidity
// datatype[length] name;
// Example:
uint[5] public myFixedArray;
myStructure[10] myOtherFixedArray;
```

Dynamic array  - array of no fixed length

```solidity
// datatype[] name;
// Example:
uint[] public myDynamicArray;
myStructure[] myOtherDynamicArray;
```

Adding to an array

```solidity
// array.push(value);
uint[] myArray;
myArray.push(1);
myArray.push(1);
myArray.push(2);
myArray.push(3);
// myArray no equals [1, 1, 2, 3]
```

### Structures

Complex data type. Has multiple properties:

```solidity
contract ContractName {
	// A structure with two properties: an integer and a string
	struct MyStructureName {
		uint myUnsignedInteger;
		string myString;
	}
	
	// Create a variable of the new data type
	MyStructureName myNewVar = MyStructureName(100, "My string");
}
```

**


## Maths operators

'+' addition  
'-' subtraction  
'*' multiplication  
'/' division  
'**' to the power of  
'%' modulus  
 > 13 % 5 = 3  
 > 5 goes into 13 twice with a remainder of 3
