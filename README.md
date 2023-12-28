import inquirer from "inquirer";
type anyType = {
    userGuess: number
}
const sysTemGeneratedNum = Math.floor(Math.random() * 10);

const ansWer:anyType = await inquirer.prompt([
    {
        type: "Name",
        name:"userGuess",
        message:"Write Your Guess b/w 1 to 10:"
    }
])

const {userGuess} = ansWer;
console.log(userGuess,"userGuess",sysTemGeneratedNum ,"System")
if(userGuess === sysTemGeneratedNum){
    
    console.log("Yeaaa Your answer is correct \n You Win")
}else{
    console.log("Pleae Try Again Better Luck Next Time")
}
