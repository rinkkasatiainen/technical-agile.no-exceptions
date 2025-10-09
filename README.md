# No Exceptions

This is code exercise aiming to learn to get rid of exceptional code, that is, code that relies on exception handling.

The 'incoming boundary' of the capability is [signup-to-session.js](./src/attend-to-a-session/routes/signup-to-session.js).
The calling code currently expects that this code will throw errors if it's not following the 'happy flow'.

For this contract, there exists an [Acceptance Test](./test/acceptance.test.js) that tests all the errors thrown and the
happy case.

# Exercise flow:
## Plan ahead.

1. Discuss for 5 minutes what are the consequences of code where exceptions are thrown.
2. Let's gather our learnings
3. There's two approaches on this: bottom-up vs 'top-down'. 
   - bottom up: meaning starting at [session.js](./src/attend-to-a-session/domain/session.js)
   - start at 'incoming boundary' [signup-to-session.js](./src/attend-to-a-session/routes/signup-to-session.js)
4. What are the implications of choosing first of the other. 

## Start coding

Make sure that you keep on green. Existing tests can be red for only a brief moment.
If you want extra challenge, do this with 'parallel change' approach (also known as 
'expand-migrate-contract')

## For extra challenge:

- Use 'expand-migrate-contract' approach (if it's known for you.)
- make sure the existing tests never break.

# Getting started

## Installation:

1. Run `yarn` or `npm install`, whichever you prefer (yarn is used by default, but you may choose what you want)
2. Run tests (`yarn test` or `npm run test`) and see all tests green.

## Optional, eslint rules

1. You can check that eslint is configured by running `yarn lint` that runs linting - it should have no issues.


# Questions?

- should the 'user not found' scenario be actually a 'UserNotFoundError' - I see that a lot in production codes.
