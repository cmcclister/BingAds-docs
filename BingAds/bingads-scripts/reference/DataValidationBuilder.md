# DataValidationBuilder
Provides methods for building a data validation rule in a spreadsheet.

|Method|Return Type|Description|
|-|-|-
build|[DataValidation](./DataValidation)|Builds a data validation rule from the definition in this builder.<br />
requireNumberBetween|[DataValidationBuilder](./DataValidationBuilder)|Specifies the data validation rule to require a number between the provided values, including the values themselves.<br />
setAllowInvalid|[DataValidationBuilder](./DataValidationBuilder)|Specifies whether a warning is shown when the entered data fails validation or whether to reject the entered data.<br />
setHelpText(String helpText)|[DataValidationBuilder](./DataValidationBuilder)|Specifies the help text that is shown when the user hovers the mouse cursor over the cell where the data validation rule is set.<br />
