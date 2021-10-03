The table below talks about "developer needs" without having validated them or
discussing whether each separate need has to be addressed by this proposal.
It's purpose is solely to organize these needs with the proposed solutions to
be able to talk about them in a clear and organized way.

The "Proposed Solution" is meant to be a living column showing the status quo
based on the most current proposal.

<table>
<thead>
<tr>
<th>Developer Need</th>
<th>Proposed Solution</th>
<th>Precedents</th>
</tr>
</thead>
<tbody>

<tr>
<td>To apply a series of unary functions to a value in left-to-right order</td>
<td><code>Function.pipe(value, ...fns)</code></td>
<td>

- [`pipe` in fp-ts](https://gcanti.github.io/fp-ts/modules/function.ts.html#pipe)
- [`|>` in F#](https://docs.microsoft.com/en-us/dotnet/fsharp/language-reference/functions/#function-composition-and-pipelining)
- [`|>` in Elixir](https://hexdocs.pm/elixir/Kernel.html#%7C%3E/2)
- [`|>` in Elm](https://package.elm-lang.org/packages/elm/core/latest/Basics#(|%3E))
- [`|>` in Julia](https://docs.julialang.org/en/v1/base/base/#Base.:%7C%3E)
- [`|>` in LiveScript](https://livescript.net/#piping)
- [`Data.Function.&` in Haskell](https://hackage.haskell.org/package/base-4.15.0.0/docs/Data-Function.html#v:-38-)

</td>
</tr>

<tr>
<td>To apply a series of unary async functions to a value in left-to-right order</td>
<td><code>Function.pipeAsync(value, ...fns)</code></td>
<td>
</td>
</tr>

<tr>
<td>To define a function in terms of a series of function calls in left-to-right order</td>
<td><code>Function.compose(...fns.reverse())</code></td>
<td>

- [`flow` in Lodash](https://lodash.com/docs/4.17.15#flow)
- [`pipe` in Ramda](https://ramdajs.com/docs/#pipe)
- [`flow` in fp-ts](https://gcanti.github.io/fp-ts/modules/function.ts.html#flow)
- [`pipe(fns)` in Sanctuary](https://sanctuary.js.org/#pipe)

</td>
</tr>

<tr>
<td>To define a function in terms of a series of function calls in right-to-left order</td>
<td><code>Function.compose(...fns)</code></td>
<td>

- [`compose` in Ramda](https://ramdajs.com/docs/#compose)
- [`flowRight` in Lodash](https://lodash.com/docs/4.17.15#flowRight)

</td>
</tr>

<tr>
<td>To define a function in terms of a series of async function calls in left-to-right order</td>
<td><code>x => Function.pipeAsync(x, ...fns)</code></td>
<td>

- [`pipeP` in Ramda](https://ramdajs.com/docs/#pipeP)
- [`p-pipe` by sindresorhus](https://www.npmjs.com/package/p-pipe)

</td>
</tr>

<tr>
<td>To define a function in terms of a series of async function calls in right-to-left order</td>
<td><code>x => Function.pipeAsync(x, ...fns.reverse())</code></td>
<td>

- [`composeP` in Ramda](https://ramdajs.com/docs/#composeP)

</td>
</tr>

<tr>
<td>To (partially) compose two unary functions in right-to-left order</td>
<td><code>Function.compose.bind(Function, f)(g)(x)</code></td>
<td>

- [`compose` in Sanctuary](https://sanctuary.js.org/#compose)
- [`map` in Sanctuary](https://sanctuary.js.org/#map)
- [`map` in Ramda](https://ramdajs.com/docs/#map)
- [`B` from combinatory logic](https://gist.github.com/Avaq/1f0636ec5c8d6aed2e45)
- [`.` in Haskell](https://hackage.haskell.org/package/base-4.15.0.0/docs/Prelude.html#v:.)

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
- [`K` from combinatory logic](https://gist.github.com/Avaq/1f0636ec5c8d6aed2e45)
- [`const` in Haskell](https://hackage.haskell.org/package/base-4.15.0.0/docs/Prelude.html#v:const)

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
- [`I` from combinatory logic](https://gist.github.com/Avaq/1f0636ec5c8d6aed2e45)
- [`id` in Haskell](https://hackage.haskell.org/package/base-4.15.0.0/docs/Prelude.html#v:id)

</td>
</tr>

</tbody>
</table>
