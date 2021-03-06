## 0.6.0

* Adds support for substituting array parameters for an array constructor (`ARRRAY[]`) if there is a flag set on the array (`literalArray`)

## 0.5.0

* Adds support for javascript arrays in queries by splitting them out in to sql arrays in the query and adjusting the params array to include the members of the parameter.

## 0.4.3

* __BUG:__ Fixes normalization of queries with ? params not referencing any params beyond the first.

## 0.4.2

* __BUG:__ Fixes normalization of queries without parameters not carrying over their options if supplied.

## 0.4.1

* __BUG:__ Fixes null bug related to hasCurrent and currentVal for domain transactions.

## 0.4.0

* __BUG:__ different database/server/user combos can now be handled concurrently after rewriting to use stacked prototypes where possible
* Expands the test suite to verify common transactional handling cases
* Drops the hard dependency on when and switches to ES6 promises

## 0.3.1

* __BUG:__ fixes error on passing pre-normalized query though normalize again.

## 0.3.0

* Adds support for ? parameters in addition to $# and $name parameters.
* Positional parameters may be passed as varargs or an array.
* An optional options object may be passed as the last argument to a query method.
* Expands the test suite to cover various methods of parameter handling.

## 0.2.2

* Exposes the connection string on for the db.

## 0.2.1

* __BUG:__ fixes an issue with nested transactions not nesting correctly.
* Adds an initial test suite.

## 0.2.0

* Adds support for stack-based transactions using domains. Any database interaction that takes place within and existing transaction block somewhere up the stack will use the existing transaction unless otherwise specified explicitly using db.newTransaction.

## 0.1.0

* Adds support for named parameters.

## 0.0.1

* Queries return promises, which can be used inside a transactional generator.
* Supports a plain query for a result set object, queryOne for an expected single result, and nonQuery for rowCount-only queries.
