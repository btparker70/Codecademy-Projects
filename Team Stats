const team = {
  _players: [
    {
      firstName: 'Alec',
      lastName: 'Dells',
      age: 21
    },
    {
      firstName: 'Derrek',
      lastName: 'Lerowitz',
      age: 19
    },
    {
      firstName: 'Blair',
      lastName: 'Jones',
      age: 18
    }
  ],
  _games: [
    {
      opponent: 'Flying Pigs',
      teamPoints: 3,
      opponentPoints: 2
    },
    {
      opponent: 'Sneaky Snakes',
      teamPoints: 2,
      opponentPoints: 2
    },
    {
      opponent: 'Berlin Walls',
      teamPoints: 0,
      opponentPoints: 1
    }
  ],
  get players() {
    return this._players;
  },
  get games() {
    return this._games;
  },
  addPlayer(firstName, lastName, age) {
    let player = {
      firstname: firstName,
      lastname: lastName,
      age: age
    };
    return this._players.push(player);
  },
  addGame(opponentName, teamPoints, opponenetPoints) {
    let game = {
      opponentName: opponentName,
      teamPoints: teamPoints,
      opponenetPoints: opponenetPoints
    };
    return this._games.push(game);
  }
};

team.addPlayer('Steph', 'Curry', 28);
team.addPlayer('Lisa', 'Leslie', 44);
team.addPlayer('Bugs', 'Bunny', 76);
console.log(team._players);

team.addGame('Apes', 2, 1);
team.addGame('Blobs', 3, 4);
team.addGame('Gotens', 7, 2);

console.log(team._games);
