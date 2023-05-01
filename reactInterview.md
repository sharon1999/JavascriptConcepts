## Qn 1 : You are given an array of objects 

    [
      { name: "India", value: "IN", cities: ["Delhi", "Mumbai"] },
      { name: "Pak", value: "PK", cities: ["Lahore", "Karachi"] },
      { name: "Bangladesh", value: "BG", cities: ["Dhakka", "Chittagong"] }
    ]
    
## Create two dropdowns one to show the countries and other to show the cities 
![image](https://user-images.githubusercontent.com/49652785/235489540-47b35120-f313-47e9-887c-9080d3be7186.png)

```javascript
import  React, { useState } from  "react";
const  Interview  = () => {
const [country, setCountry] =  useState();
const  countries  = [
{ name: "India", value: "IN", cities: ["Delhi", "Mumbai"] },
{ name: "Pak", value: "PK", cities: ["Lahore", "Karachi"] },
{ name: "Bangladesh", value: "BG", cities: ["Dhakka", "Chittagong"] },
];

return (
<div>
  <select  onChange={(e) =>  setCountry(e.target.value)}>
  {countries.map((c, id) => (
    <option  value={c.value}  key={c.value}>
    {c.name}
    </option>
  ))}
  </select>
  {countries
    .filter(function (c) {
    return  c.value  ===  country;
    }).map((co, i) => (
    <select>
    {co.cities.map((c) => (
    <option>{c}</option>
    ))}
    </select>
  ))}
</div>
);
};
 export  default  Interview;
```


