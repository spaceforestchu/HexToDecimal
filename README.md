# HexToDecimal

    function hexToDec (hex) {
     var answer = 0; var i; var counter = 0; 
     
     var array = hex.toLowerCase().split("").reverse();
     
     var newArray = [];
    for(i = array.length-1; i >= 0; i--){
        
        if(array[i] === "a"){
           newArray.push(10);
        } else if(array[i] === "b"){
            newArray.push(11);
        } else if(array[i] === "c"){
            newArray.push(12);
        } else if(array[i] === "d"){
            newArray.push(13);
        }else if(array[i] === "e"){
            newArray.push(14);
        }else if(array[i] === "f"){
            newArray.push(15);
        }else if("012345679".indexOf(array[i]) > -1){
            newArray.push(array[i]);
        }
    }
        for( i = newArray.length-1; i >= 0; i--){
            answer += newArray[i] * Math.pow(16, counter);
            counter++;
        }
        return answer;
    }
    
    hexToDec("f0")
