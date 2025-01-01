This example demonstrates a subtle issue with `Enum.each` and the `throw` macro in Elixir. When `throw` is used inside an `Enum.each` function, the execution is immediately halted, and subsequent operations within that same iteration's function call are not executed.  This might lead to unexpected behaviour where cleanup operations or messages scheduled to be printed might not run as expected.