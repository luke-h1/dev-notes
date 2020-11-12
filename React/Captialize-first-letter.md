## Capitalize first letter of a str react


* Usually in Vanilla js you can use the charAt and slice method to achieve making the first letter of a string uppercase. This however will not work with props. 

* To get around this issue you will have to write a function that takes in a string and does the above. 

## Example: 


````
const component = ({item}) => { 
  const {value} = item; 

  const capitalizeFirstLetter = (str) => { 
    return str.charAt(0).toUpperCase() + str.slice(1)
  } 
  return ( 
    <>
    {capitalizeFirstLetter(value)}    
    </>
  )
}
````



Function: 
```
const capitalizeFirstLetter = (str) => { 
    return str.charAt(0).toUpperCase() + str.slice(1)
  }

```