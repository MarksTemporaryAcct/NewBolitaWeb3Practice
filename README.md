# BOLITA

Players et on the last 3 digits of the days positive covid cases

Bet amount defaults to 5 finney sent as msg.value

At 15:00 the application will get the latest covid data, and set the last 3 digits as the winning numbers, at which point: 
	+Winners will be paid out (with event emitted)
	+Bets will be cleared (with event emitted)
	+Betting will be opened again for tomorrow's number (with event emitted)
	
Contract should be deployed with some ETH to payout winners

Currently only supports 1 digit betting and 1 bet per day

## ABOUT
Popup.js is the core file that:
- successfully runs a clock (to trigger the setWinningNumber at 15:00)
- uses the numbered circles on popup.html to update the input field's values
- sends get request to covidtracking API
- maps correct smart contract functions to the corresponding buttons

## Dependencies

Use NPM for the following libraries:

```bash
npm install --save web3
```
```bash
npm install ganache-cli
```

## Usage
The homepage is popup.html. On form submit from betting on 1 digit, you are taken to results.html

Currently, results.html is used for testing.

Run the devtools with preserve logging = true to watch the console for outputs
'Get the latest winning numbers' will be used to test call to bolita.sol's setWinningNumber()
'GET CNN NUMBERS' will get the positive cases, and parse the last 3 digits.


Run ganache-cli/Testrpc with the command:
```bash
ganache-cli
```

## Outstanding Issues:
1. content security policy related updates needed to work as a chrome extension