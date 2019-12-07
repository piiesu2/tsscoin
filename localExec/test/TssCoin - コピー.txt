var TssCoin = artifacts.require("./TssCoin.sol");

contract('TssCoin', function(accounts) {

	it("should put 1000 TssToken in the first account", function() {
		return TssCoin.deployed().then(function(instance) {
			return instance.balanceOf.call(accounts[0]);
			
		}).then(function(balance) {
			assert.equal(balance.valueOf(), 100000000000000000000, "100000000000000000000 wasn't in the first account.");
		});
	});
});
