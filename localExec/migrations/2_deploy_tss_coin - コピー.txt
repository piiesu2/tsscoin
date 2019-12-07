var TssCoin = artifacts.require("./TssCoin.sol");

module.exports = function(deployer) {
	var initialSupply = 1000;
	deployer.deploy(TssCoin,{gas:2000000});
	
}