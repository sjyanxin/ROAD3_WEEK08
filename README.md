# Casino.sol

A random number casino for use on Ethereum blockchains.

[Click here for a detailed explanation](https://blog.logrocket.com/build-random-number-generator-blockchain/).

yarn  hardhat console --network optimismTest
# check whether this is your metamask account
signer = await ethers.getSigner();


# check your balance
balance0 = await ethers.provider.getBalance((await ethers.getSigner()).address)
BigNumber { value: "48335146483888624" }

#start compile contract
factory = ethers.getContractFactory("Casino")
# get bytecode info
factory = await factory
# deploy your contract
casino = await factory.deploy()



const valA = ethers.utils.keccak256(0xBAD060A7)
const hashA = ethers.utils.keccak256(valA)
const valBwin = ethers.utils.keccak256(0x600D60A7)
tx1 = await casino.proposeBet(hashA,{ value: 1e5})

tx2 = await casino.acceptBet(hashA, valBwin, {value: 1e5})