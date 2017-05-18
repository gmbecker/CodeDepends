## change to inputs in, e.g, rownames(cov) = NULL

When handling non-simple RHS in assign-handler, any variable indicated as an
update is also indicated as an input for that expression.

in the above example, cov will NOT be listed as an output (only an update and input)


## getVariableDepends and getSectionDepends now accept ...

The ... is passed directly to getInputs (and in getVariableDepends'
case, to getSectionDepends) when creating the default info value. This
allows users to, e.g., specify a collector, or formulaInputs=TRUE
directly int he call to the get*Depends functions.

## getVariables now works correctly.

*functions* argument is now ignored unless inputs is TRUE (user defined
functions created in that block are already captured as ouputs by
defualt)
