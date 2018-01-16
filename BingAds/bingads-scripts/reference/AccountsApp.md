# AccountsApp
This is the top-level object for managing multiple accounts in the Bing Ads system.

|Method|Return Type|Description|
|-|-|-
accountLabels|[AccountLabelSelector](./AccountLabelSelector)|Returns a selector of all account labels defined in the current customer shell.<br />
accounts|[BingAdsAccountSelector](./BingAdsAccountSelector)|Returns a selector of all accounts accessible to the current user under the current customer shell.<br />
createAccountLabel(String name)|void|Creates a new account label.<br />
ownedAccounts|[BingAdsAccountSelector](./BingAdsAccountSelector)|Returns a selector of all accounts owned by this customer shell.<br />
linkedAccounts|[BingAdsAccountSelector](./BingAdsAccountSelector)|Returns a selector of all accounts linked to, but not owned, by this customer shell.<br />
select(BingAdsAccount account)|void|Selects a BingAdsAccount object as the next account and sets it as the current account. This is the account that is returned by BingAdsApp.<br />
