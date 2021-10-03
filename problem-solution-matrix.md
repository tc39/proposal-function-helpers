<table>
<thead>
<tr>
<th>Problem Description</th>
<th>Proposed Solution</th>
<th>Precedents</th>
</tr>
</thead>
<tbody>

<tr>
<td>To apply a series of unary functions to a value</td>
<td><code>Function.pipe(value, ...fns)</code></td>
<td>

- [`pipe` in fp-ts](https://gcanti.github.io/fp-ts/modules/function.ts.html#pipe)

</td>
</tr>

<tr>
<td>To apply a series of unary async functions to a value</td>
<td><code>Function.pipeAsync(value, ...fns)</code></td>
<td>
</td>
</tr>

<tr>
<td>To define a function in terms of a series of function calls</td>
<td><code>Function.compose(...fns.reverse())</code></td>
<td>

- [`flow` in Lodash](https://lodash.com/docs/4.17.15#flow)
- [`pipe` in Ramda](https://ramdajs.com/docs/#pipe)
- [`flow` in fp-ts](https://gcanti.github.io/fp-ts/modules/function.ts.html#flow)

- [`compose(...fns.reverse())` in Ramda](https://ramdajs.com/docs/#compose)

</td>
</tr>

<tr>
<td>To define a function in terms of a series of async function calls</td>
<td>-</td>
<td>

- [`composeP` in Ramda](https://ramdajs.com/docs/#composeP)
- [`pipeP` in Ramda](https://ramdajs.com/docs/#pipeP)

</td>
</tr>

<tr>
<td>To (partially) compose two unary functions</td>
<td><code>Function.compose.bind(Function, f)(g)(x)</code></td>
<td>

- [`compose` in Sanctuary](https://sanctuary.js.org/#compose)
- [`map` in Sanctuary](https://sanctuary.js.org/#map)
- [`map` in Ramda](https://ramdajs.com/docs/#map)

</td>
</tr>

<tr>
<td>To create a function that always returns the same value</td>
<td><code>Function.constant(value)</code></td>
<td>

- [`constant` in lodash](https://lodash.com/docs/4.17.15#constant)
- [`always` in Ramda](https://ramdajs.com/docs/#always)
- [`K` in Sanctuary](https://sanctuary.js.org/#K)
- [`constant-function` in stdlib](https://stdlib.io/docs/api/latest/@stdlib/utils/constant-function)

</td>
</tr>

<tr>
<td>A function that returns its input unchanged to be used as an argument to HOFs</td>
<td><code>Function.identity</code></td>
<td>

- [`identity` in lodash](https://lodash.com/docs/4.17.15#identity)
- [`identity` in Ramda](https://ramdajs.com/docs/#identity)
- [`I` in Sanctuary](https://sanctuary.js.org/#I)
- [`identity-function` in stdlib](https://stdlib.io/docs/api/latest/@stdlib/utils/identity-function)

</td>
</tr>

</tbody>
</table>
