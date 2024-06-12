# Assessment_ETH-PROOF : Beginner EVM Course

this repository is created to upload the code , readme file and output of the final assessment of the course ETH PROOF: Beginner EVM Course.
## Description

in this repository there is a code related to the final assessment of the course" ETH PROOF: Beginner EVM Course". in the final assesment of this cousre we use solidity language to create a new token named = DEWACOIN , which nick name is "DC"  using the variables to assign the name and nick name and the total supply of this token. further i use the mapping function to map the wallet address with the unsighned integer(which only store +ve value ) which store the token value in that account . furter i created two function "mint" & "burn" function to add new token to the wallet adress and to delete or burn the tokens.in both the functions we  keep updating the total supply to check the remaing tokens in the account . also we use an condition in burn function in which if the total supply is less then the number of token we want to burn , then the function get executed but left the total supply unchanged . 
this is the total short overview of the given code . 

## Getting Started

### Installing

* Download the code from github which is writeen in solidity language .
* The file which contain the code is " newToken.sol ".

### Executing program

* copy the code from the code file.
*open [@remixIDE](https://remix.ethereum.org/) in your browser . it is besically an IDE to run this code .
*create a new file as "newToken.sol" and paste entire code in that file and compile the code . 
* then deploy the code clicking on etherium icon and copy and paste the default wallet address in the deployed mint function and the value of token you want to mint and transect the fucntiuon to execute.
same for burn function .
* paste the wallet adress into the balances function and call it to know the amount of available token in your wallet addresss.
* press the buttons "TokenName" ,"TokenNickName" , "totalSupply" to get the output of the name of the coin , its nick name and token remain in the supply respectively.

*the main code is given below:
```
contract MyToken {

    // public variables here
    string public tokenName ="DEWACOIN";
    string public tokenNickName="DC";
    uint public totalSupply=0;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function mint(address _walletaddress , uint _value) public {
          totalSupply += _value;
          balances[_walletaddress] += _value;
    }
    // burn function
 function burn(address _walletaddress , uint _value) public {
        if(balances[_walletaddress] >= _value){
            totalSupply -= _value;
            balances[_walletaddress] -= _value;
        }
    }
}
```

## Help
for any help and query drop an email on:
(abhinesh2162@gmail.com)


## Authors

Abhinesh Kumar  
[@Linkedin](https://www.linkedin.com/in/kumarabhinesh/)
