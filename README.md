## Ali_khatami_Solidity06(from the video of Pattrick Collins)
### Remix fund me

### Sending ETH through a function and reverts

We have created new solidity file which is ```akrkFundMe.sol```<br>

```akrkFundme.sol``` is going to be a contract that allows people to actually fund a collective goods so that people can send etherium or polygon or whatever blockchain<br>
native token into this contract and some owner of those conntract can do whatever they want with those contract<br>

here this contract will get fund from users, withdraw funds and set aminimum funding value in USD<br>

![w30](https://user-images.githubusercontent.com/89090776/231401349-11c1142a-203c-4eb7-9f6b-f1303f851a42.jpg)
Figure1: here the ```value``` represent how much etherium we are sending with our transcations

![w32](https://user-images.githubusercontent.com/89090776/231404780-6bc6446b-dec6-448e-9abe-63c876ee297f.jpg)
figure2: Going to this link https://eth-converter.com/ we can find relation beteen ether,GWEI and WEI.<br>


When we will use ```payable``` keyword with any function it will make it payable with any native blockchain currency and the button created due to that functyion will be red<br>
in color<br>

Just like as our wallet hold funds , contract addresses can hold funds as well.<br>
Smart contract addresses are nearly the same as the wallet addresses<br>

So both smart contract and wallet can hold native blockchain token like etherium

```
//SPDX-License-Identifier:MIT

pragma solidity ^0.8.8;

contract akrkFundMe  {

// we have use payable keyword with the function below to make it payable with any native blockchain currency
    function fund() public payable {

        require(msg.value > 1e18 , "Not send enough");// to get accees to the 'value' at deploy at run transaction tab
        //1e18 is 1 ether, here the value must be greater than 1 ether
        //require is a checker it checks whether the value is greater than 1 ether
        // if not it is going to revert with an error messsage shown above

    }// To send money. We made it public so that anybody can call it



    

}

```

![w33](https://user-images.githubusercontent.com/89090776/231412248-cc110365-6f69-47a3-b6ab-d40822e3a11a.jpg)
Figure1: Output after we deployed


