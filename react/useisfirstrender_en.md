Priya Pandey

To identify the first render, we can use a global variable and the useRef hook. This method allows us to keep track of the initial render of the component.

import {useRef} from 'react';
let val=true;
export function useIsFirstRender(): boolean {
  const isFirst=useRef(true);
  if(val){
    val=false;
    return isFirst.current;
  }
    return val;
}


