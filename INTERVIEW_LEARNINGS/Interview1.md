i# This is the first interview that I started seeing from Anurag Procodrr for react interview 

## Question 1) How can we render two components without using react fragments and div ?

 *** Ans ) We can render two components using Arrays we have to wrap the element inside the array then render that array or use the spread operator to do so . Arrays act as a grouping mechanism for sibling elements.
They satisfy React's requirement for a single returnable entity.  ***

 ```
// first way 
const ComponentA = () => <p>Component A</p>;
const ComponentB = () => <p>Component B</p>;

const ParentComponent = () => {
  return [
    <ComponentA key="1" />,
    <ComponentB key="2" />,
  ];
};

export default ParentComponent;

 ```
```

//second way  using the concept of spread operator
const ComponentA = () => <p>Component A</p>;
const ComponentB = () => <p>Component B</p>;

const ParentComponent = () => {
  const additionalComponents = [<ComponentA key="1" />, <ComponentB key="2" />];

  return [...additionalComponents];
};

export default ParentComponent;

```. 
