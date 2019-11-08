# proposal-use-strict-versioning
Allow to specify target ES version for `"use strict"`

ex.: `"use strict es6";`

# Motivation
As a main focus for all ES realisations is not to break backwards compatibility – it is hard for implementators to bring new language feature because of legacy code they need to support across all diferent browser engines.

It'll be much easier to guard new feature realisation with **language version switch** and implement proposals while ignore problems that backward compatability brings.

And then all of the end-users will be forced to knowlingly specify version of specification they target with their code. 

# Potential problems
- instead of only one `"use strict"` check this proposal implies that we have in a number of magnitude more so it could became hard to support in a longer perspective
- now end-users must knowlingly review and verify that their code will run the same way if they target higher spec. version

# Other aproach
Instead of bringing **version switches** we could use **feature switches** wich could function the same way `--harmony` flags works in node

ex. `"use promise-try, pipline-operator";`
