//[1,2,3], [2,3,4], [3,4,5] => [1,5]
let input=[[1,2,3], [2,3,4], [3,4,5]]

const DistinctElements=(input)=>{
  let result=[]
  for(let i=0;i<input.length;i++){
    for(let j=0;j<input[i].length;j++){
    
      result.push(input[i][j])
    }
  }
   let obj={}
   for(let k=0;k<result.length;k++){
     if(obj[result[k]]==undefined){
       obj[result[k]]=1
     }else{
       obj[result[k]]+=1
     }
   }
  // console.log(obj)
  let desiredoutput=[]
  for(let m in obj){
    if(obj[m]==1){
      desiredoutput.push(Number(m))
    }
  }
  console.log(desiredoutput)
}

DistinctElements(input)
