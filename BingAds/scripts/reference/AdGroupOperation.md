# AdGroupOperation
Represents the definition of an ad group constructed via [AdGroupBuilder](./AdGroupBuilder). The ad group is only stored in the system when any of the methods on this object are invoked or when the script finishes execution, whichever comes first. For more efficiency, store the operation objects in an array and only invoke its methods when all operations have been constructed.

|Method|Return Type|Description|
|-|-|-
[getErrors]('#getErrors')|String[]|Returns an empty array if the ad group was successfully created, otherwise returns the errors encountered during the execution of this operation.<br />
[getResult]('#getResult')|[AdGroup](./AdGroup)|Returns the newly created `AdGroup`, otherwise returns `null` if this operation failed to execute.<br />
[isSuccessful]('#isSuccessful')|boolean|Returns <br />

<a name="getErrors"></a>
## getErrors
Returns an empty array if the ad group was successfully created, otherwise returns the errors encountered during the execution of this operation.


<a name="getResult"></a>
## getResult
Returns the newly created `AdGroup`, otherwise returns `null` if this operation failed to execute.


<a name="isSuccessful"></a>
## isSuccessful
Returns 

