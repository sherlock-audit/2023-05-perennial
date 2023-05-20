
# Perennial contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
Perennial is deployed on Ethereum and Arbitrum mainnets
___

### Q: Which ERC20 tokens do you expect will interact with the smart contracts? 
DSU and USDC
___

### Q: Which ERC721 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Which ERC777 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Are there any FEE-ON-TRANSFER tokens interacting with the smart contracts?

None
___

### Q: Are there any REBASING tokens interacting with the smart contracts?

None
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED?
Protocol admin (Controller.owner): TRUSTED
___

### Q: Is the admin/owner of the protocol/contracts TRUSTED or RESTRICTED?
TRUSTED
___

### Q: Are there any additional protocol roles? If yes, please explain in detail:
Product Coordinator - these are owners of the products who can update product parameters
___

### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
None
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
Malicious product coordinators can steal user funds _from their own product_. We are aware that malicious coordinators have a large amount of power with respect to funds deposited towards their products, however, if they can adversely affect **other products/collateral outside their product** we want to be are of this.
___

### Q: Please provide links to previous audits (if any).

https://drive.google.com/file/d/1WPPDUAAxgQhvY38jiKutRogqQoPtoBKF/view?usp=drivesdk

https://github.com/equilibria-xyz/perennial-mono/tree/master/packages/perennial/audits

Comprehensive Veridise audit is being finalized now and will be added soon
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)?
Off-chain liquidators, OpenZeppelin defender tasks which periodically sync the vaults if they get far out of balance
___

### Q: In case of external protocol integrations, are the risks of external contracts pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality.
We want to be aware of issues that might arise from Chainlink or DSU integrations
___



# Audit scope


[root @ 914838c1cb2532325ecf5659807f9fca61d635e9](https://github.com/equilibria-xyz/root/tree/914838c1cb2532325ecf5659807f9fca61d635e9)
- [root/contracts/accumulator/types/Accumulator6.sol](root/contracts/accumulator/types/Accumulator6.sol)
- [root/contracts/accumulator/types/UAccumulator6.sol](root/contracts/accumulator/types/UAccumulator6.sol)
- [root/contracts/control/unstructured/CrossChainOwnable/UCrossChainOwnable.sol](root/contracts/control/unstructured/CrossChainOwnable/UCrossChainOwnable.sol)
- [root/contracts/control/unstructured/CrossChainOwnable/UCrossChainOwnable_Arbitrum.sol](root/contracts/control/unstructured/CrossChainOwnable/UCrossChainOwnable_Arbitrum.sol)
- [root/contracts/control/unstructured/CrossChainOwnable/UCrossChainOwnable_Optimism.sol](root/contracts/control/unstructured/CrossChainOwnable/UCrossChainOwnable_Optimism.sol)
- [root/contracts/control/unstructured/CrossChainOwner/UCrossChainOwner.sol](root/contracts/control/unstructured/CrossChainOwner/UCrossChainOwner.sol)
- [root/contracts/control/unstructured/CrossChainOwner/UCrossChainOwner_Arbitrum.sol](root/contracts/control/unstructured/CrossChainOwner/UCrossChainOwner_Arbitrum.sol)
- [root/contracts/control/unstructured/CrossChainOwner/UCrossChainOwner_Optimism.sol](root/contracts/control/unstructured/CrossChainOwner/UCrossChainOwner_Optimism.sol)
- [root/contracts/control/unstructured/UInitializable.sol](root/contracts/control/unstructured/UInitializable.sol)
- [root/contracts/control/unstructured/UOwnable.sol](root/contracts/control/unstructured/UOwnable.sol)
- [root/contracts/control/unstructured/UReentrancyGuard.sol](root/contracts/control/unstructured/UReentrancyGuard.sol)
- [root/contracts/curve/CurveMath18.sol](root/contracts/curve/CurveMath18.sol)
- [root/contracts/curve/CurveMath6.sol](root/contracts/curve/CurveMath6.sol)
- [root/contracts/curve/types/JumpRateUtilizationCurve.sol](root/contracts/curve/types/JumpRateUtilizationCurve.sol)
- [root/contracts/curve/types/JumpRateUtilizationCurve18.sol](root/contracts/curve/types/JumpRateUtilizationCurve18.sol)
- [root/contracts/curve/types/JumpRateUtilizationCurve6.sol](root/contracts/curve/types/JumpRateUtilizationCurve6.sol)
- [root/contracts/curve/types/UJumpRateUtilizationCurve18.sol](root/contracts/curve/types/UJumpRateUtilizationCurve18.sol)
- [root/contracts/curve/types/UJumpRateUtilizationCurve6.sol](root/contracts/curve/types/UJumpRateUtilizationCurve6.sol)
- [root/contracts/number/NumberMath.sol](root/contracts/number/NumberMath.sol)
- [root/contracts/number/types/Fixed18.sol](root/contracts/number/types/Fixed18.sol)
- [root/contracts/number/types/Fixed6.sol](root/contracts/number/types/Fixed6.sol)
- [root/contracts/number/types/PackedFixed18.sol](root/contracts/number/types/PackedFixed18.sol)
- [root/contracts/number/types/PackedUFixed18.sol](root/contracts/number/types/PackedUFixed18.sol)
- [root/contracts/number/types/UFixed18.sol](root/contracts/number/types/UFixed18.sol)
- [root/contracts/number/types/UFixed6.sol](root/contracts/number/types/UFixed6.sol)
- [root/contracts/storage/UStorage.sol](root/contracts/storage/UStorage.sol)
- [root/contracts/token/types/Token18.sol](root/contracts/token/types/Token18.sol)
- [root/contracts/token/types/Token6.sol](root/contracts/token/types/Token6.sol)
- [root/contracts/token/types/TokenOrEther18.sol](root/contracts/token/types/TokenOrEther18.sol)

[perennial-mono @ b06d5145db62a312dd88dfcafef0f8e2166c5e32](https://github.com/equilibria-xyz/perennial-mono/tree/b06d5145db62a312dd88dfcafef0f8e2166c5e32)
- [perennial-mono/packages/perennial-oracle/contracts/ChainlinkFeedOracle.sol](perennial-mono/packages/perennial-oracle/contracts/ChainlinkFeedOracle.sol)
- [perennial-mono/packages/perennial-oracle/contracts/ChainlinkOracle.sol](perennial-mono/packages/perennial-oracle/contracts/ChainlinkOracle.sol)
- [perennial-mono/packages/perennial-oracle/contracts/types/ChainlinkAggregator.sol](perennial-mono/packages/perennial-oracle/contracts/types/ChainlinkAggregator.sol)
- [perennial-mono/packages/perennial-oracle/contracts/types/ChainlinkRegistry.sol](perennial-mono/packages/perennial-oracle/contracts/types/ChainlinkRegistry.sol)
- [perennial-mono/packages/perennial-oracle/contracts/types/ChainlinkRound.sol](perennial-mono/packages/perennial-oracle/contracts/types/ChainlinkRound.sol)
- [perennial-mono/packages/perennial-vaults/contracts/balanced/BalancedVault.sol](perennial-mono/packages/perennial-vaults/contracts/balanced/BalancedVault.sol)
- [perennial-mono/packages/perennial-vaults/contracts/balanced/BalancedVaultDefinition.sol](perennial-mono/packages/perennial-vaults/contracts/balanced/BalancedVaultDefinition.sol)
- [perennial-mono/packages/perennial/contracts/collateral/Collateral.sol](perennial-mono/packages/perennial/contracts/collateral/Collateral.sol)
- [perennial-mono/packages/perennial/contracts/collateral/types/OptimisticLedger.sol](perennial-mono/packages/perennial/contracts/collateral/types/OptimisticLedger.sol)
- [perennial-mono/packages/perennial/contracts/controller/Controller.sol](perennial-mono/packages/perennial/contracts/controller/Controller.sol)
- [perennial-mono/packages/perennial/contracts/controller/UControllerProvider.sol](perennial-mono/packages/perennial/contracts/controller/UControllerProvider.sol)
- [perennial-mono/packages/perennial/contracts/incentivizer/Incentivizer.sol](perennial-mono/packages/perennial/contracts/incentivizer/Incentivizer.sol)
- [perennial-mono/packages/perennial/contracts/incentivizer/types/ProductManager.sol](perennial-mono/packages/perennial/contracts/incentivizer/types/ProductManager.sol)
- [perennial-mono/packages/perennial/contracts/incentivizer/types/Program.sol](perennial-mono/packages/perennial/contracts/incentivizer/types/Program.sol)
- [perennial-mono/packages/perennial/contracts/interfaces/types/Accumulator.sol](perennial-mono/packages/perennial/contracts/interfaces/types/Accumulator.sol)
- [perennial-mono/packages/perennial/contracts/interfaces/types/PackedAccumulator.sol](perennial-mono/packages/perennial/contracts/interfaces/types/PackedAccumulator.sol)
- [perennial-mono/packages/perennial/contracts/interfaces/types/PackedPosition.sol](perennial-mono/packages/perennial/contracts/interfaces/types/PackedPosition.sol)
- [perennial-mono/packages/perennial/contracts/interfaces/types/PayoffDefinition.sol](perennial-mono/packages/perennial/contracts/interfaces/types/PayoffDefinition.sol)
- [perennial-mono/packages/perennial/contracts/interfaces/types/PendingFeeUpdates.sol](perennial-mono/packages/perennial/contracts/interfaces/types/PendingFeeUpdates.sol)
- [perennial-mono/packages/perennial/contracts/interfaces/types/Position.sol](perennial-mono/packages/perennial/contracts/interfaces/types/Position.sol)
- [perennial-mono/packages/perennial/contracts/interfaces/types/PrePosition.sol](perennial-mono/packages/perennial/contracts/interfaces/types/PrePosition.sol)
- [perennial-mono/packages/perennial/contracts/interfaces/types/ProgramInfo.sol](perennial-mono/packages/perennial/contracts/interfaces/types/ProgramInfo.sol)
- [perennial-mono/packages/perennial/contracts/multiinvoker/MultiInvoker.sol](perennial-mono/packages/perennial/contracts/multiinvoker/MultiInvoker.sol)
- [perennial-mono/packages/perennial/contracts/multiinvoker/MultiInvokerRollup.sol](perennial-mono/packages/perennial/contracts/multiinvoker/MultiInvokerRollup.sol)
- [perennial-mono/packages/perennial/contracts/periphery/CoordinatorDelegatable.sol](perennial-mono/packages/perennial/contracts/periphery/CoordinatorDelegatable.sol)
- [perennial-mono/packages/perennial/contracts/product/Product.sol](perennial-mono/packages/perennial/contracts/product/Product.sol)
- [perennial-mono/packages/perennial/contracts/product/UParamProvider.sol](perennial-mono/packages/perennial/contracts/product/UParamProvider.sol)
- [perennial-mono/packages/perennial/contracts/product/UPayoffProvider.sol](perennial-mono/packages/perennial/contracts/product/UPayoffProvider.sol)
- [perennial-mono/packages/perennial/contracts/product/types/accumulator/AccountAccumulator.sol](perennial-mono/packages/perennial/contracts/product/types/accumulator/AccountAccumulator.sol)
- [perennial-mono/packages/perennial/contracts/product/types/accumulator/VersionedAccumulator.sol](perennial-mono/packages/perennial/contracts/product/types/accumulator/VersionedAccumulator.sol)
- [perennial-mono/packages/perennial/contracts/product/types/position/AccountPosition.sol](perennial-mono/packages/perennial/contracts/product/types/position/AccountPosition.sol)
- [perennial-mono/packages/perennial/contracts/product/types/position/VersionedPosition.sol](perennial-mono/packages/perennial/contracts/product/types/position/VersionedPosition.sol)


