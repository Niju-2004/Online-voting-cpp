# Voting System

This C++ program simulates a voting system for different levels of elections: National, State, and Village. It uses object-oriented programming principles to manage voter data and tally votes for various political parties.

## Features

- **Voter Data Collection**: Collects voter details such as name, voter ID, and address.
- **Voting**: Allows voters to cast their votes for different political parties.
- **Vote Tallying**: Tallies the votes and displays the results.
- **Leading Party**: Determines the leading party based on the votes.

## Classes

### Voting (Base Class)

- **Protected Members**:
  - `name`: Voter's name.
  - `voterid`: Voter's ID.
  - `address`: Voter's address.

- **Public Members**:
  - `getdata()`: Collects voter details.
  - `voting()`: Placeholder for voting function.
  - `tot_votes()`: Placeholder for tallying votes.
  - `leading()`: Placeholder for determining the leading party.

### National (Derived Class)

- **Additional Members**:
  - `state`: State name.
  - `AITC`, `BSP`, `BJP`, `CPI`, `INC`, `NCP`: Vote counts for respective parties.

- **Public Members**:
  - `getdata()`: Overrides base class method to include state name.
  - `voting()`: Allows voting for national-level parties.
  - `tot_votes()`: Displays the total votes for each party.
  - `leading()`: Determines the leading party.

### State (Derived Class)

- **Additional Members**:
  - `city`: City name.
  - `JD`, `AAP`, `AIADMK`, `DMK`, `NPF`, `AIFC`: Vote counts for respective parties.

- **Public Members**:
  - `getdata()`: Overrides base class method to include city name.
  - `voting()`: Allows voting for state-level parties.
  - `tot_votes()`: Displays the total votes for each party.
  - `leading()`: Determines the leading party.

### Village (Derived Class)

- **Additional Members**:
  - `vill`: Village name.
  - `CPI`, `CCPI`, `DMDK`, `IIDP`, `IJK`, `INL`: Vote counts for respective parties.

- **Public Members**:
  - `getdata()`: Overrides base class method to include village name.
  - `voting()`: Allows voting for village-level parties.
  - `tot_votes()`: Displays the total votes for each party.
  - `leading()`: Determines the leading party.

## Main Function

- Prompts the user to choose the level of election (National, State, Village).
- Collects the number of voters.
- For each voter, collects data, allows voting, tallies votes, and determines the leading party.

## Usage

1. Compile the program using a C++ compiler:
   ```sh
   g++ -o voting_system voting_system.cpp
   ```
2. Run the compiled program:
   ```sh
   ./voting_system
   ```
3. Follow the on-screen instructions to enter voter details and cast votes.

## Example

```sh
enter your choice:

1. National
2. State
3. Village
1

enter no of voters
2

enter voter details:

enter name:
John Doe

enter vote_id
12345

enter address:
123 Main St

enter state name:
California

enter choice :

1.All India Trinamool Congress
2.Bahujan Samaj Party
3.Bharatiya Janata Party
4.Communist Party of India
5.Indian National Congress
6.Nationalist Congress Party
3

voted for Bharatiya Janata Party

your Voting has completed

total Voting results:
for All India Trinamool Congress=0
for Bahujan Samaj Party=0
for Bharatiya Janata Party=1
for Communist Party of India=0
for Indian National Congress=0
for Nationalist Congress Party=0
```

## Note

- The `leading()` function in the `National`, `State`, and `Village` classes currently returns an integer representing the maximum votes. It should ideally return the name of the leading party.
- The program can be extended to include more features such as saving voter data to a file, handling invalid inputs more gracefully, and providing a more user-friendly interface.
