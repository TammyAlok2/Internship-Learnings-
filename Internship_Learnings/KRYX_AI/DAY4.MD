# Greetings :
 Thanks a lot god for everything . 

## Date : 21/02/25 :

### Leanring CSS Properties 
- How to make the div in the center and in the popup form 

```
import React from "react";
import styled from "styled-components";

const StylePopSection = styled.div`

.popup-section{
display:flex;
align-items:center;
justify-content:center;
  background-color: #00000059;
  border-radius: 10px;
  position :fixed;
  z-index: 100;
  inset:0;

  &__main{
 width:50rem;
 background-color:#ffffff;
 border-radius:10px;
 border:2px solid black;
 padding:1rem;


  }

}
  
`;

const PopupSection = (props) => {
  const {data,setData } = props;
  console.log(data)
  return (
    <StylePopSection>
      <div className="popup-section">
      <div className="popup-section__main">
        <div className="popup_section__title">
          <h1>{data[0]}</h1>
          <button onClick={()=>setData(null)}>Close</button>
        </div>

        <div className="popup-section__content">
        {data[1]}
        </div>
      </div>
      </div>
    </StylePopSection>
  );
};

export default PopupSection;

```


- Learn about inset property : 
  this property make top : 0 , bottom : 0, left:0, right:0 simulatenously . 

