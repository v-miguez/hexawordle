# Technical Test - Explanation

This application is divided into two parts: front-end and back-end. The front-end part is located in the `./hexawordle` folder and the back-end part in the `./api` folder.

**Note**: The back-end does not use a database and is made simple to focus on the front-end part; the data is stored in memory and the default word is 'SOLAR' as specified in the `Definition of Done` section below in this file.

## Installation

To run the application, follow these steps:

1. Install dependencies:

```sh
npm install
```

```sh
npm run install-deps
```

## Execution

To start both parts of the application, run the following command from the root folder:

```sh
npm start
```

- The front-end application will be available on port 4200.
- The back-end will be available on port 3000.

## Tests

To run Cypress tests, use the following command in the ./hexawordle folder:

```sh
npm run e2e
```

---

## Definition of Done

For the tests, it is assumed that the secret word is "SOLAR".

#### Incorrect word with no matches

- Start a new game
- Enter the word "MENTE"

✅ Should return "00000" and decrement the number of attempts by 1.

#### Duplicate word

- Start a new game
- Enter the word "MENTE"
- Re-enter the word "MENTE"

❌ Should show an error as the word has been repeated.

#### Word with letters in the wrong place

- Start a new game
- Enter the word "AUREO"

✅ Should return "10101" and decrement the number of attempts by 1.

#### Word with letters in the correct place (partial match)

- Start a new game
- Enter the word "MOLAR"

✅ Should return "02222" and decrement the number of attempts by 1.

#### Correct word

- Start a new game
- Enter the word "SOLAR"

✅ Should return "22222", show a congratulatory message, and not allow the game to continue.

## Requirements

### Basic Requirements

The application must meet the following **basic requirements:**

- [ ] Each game will have a maximum of 6 attempts.
- [ ] Each word will have 5 letters.
- [ ] Duplicate words are not allowed.

> [!TIP]
> Before moving on to the optional requirements, make sure your solution's code is as you would like it. :eye_speech_bubble:

### Optional Requirements

Additionally, as **optional** requirements:

- [ ] Implement light mode and dark mode.
- [ ] Words that do not exist in the RAE are not allowed (Integration with mocked external service).
- [ ] Add a virtual keyboard on the main screen.

