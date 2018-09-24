# mern-classwork-pokedex

### Make Sure You Hanve the Following Checked out:

Server - https://github.com/cs-fullstack-master/mern-pokedex-backend.git
Client - https://github.com/cs-fullstack-master/mern-pokedex-frontend.git

* Add a method to server to get one Pokemon by it's number


const pokeapi2 ='https://pokeapi.co/api/v2/pokemon/300';

router.get('/:pokeID', (req, res) => {
    console.log(`Sending a request to ${pokeapi2}`);

    request(pokeapi2, function (err, response, body) {
        if (err) {
            throw err; // If we get an error then bail
        }
        // Use Express to send the JSON back to the client in the web response
        let jsonResp = JSON.parse(body);
        console.log(setPokemons(jsonResp.results));
        res.send(jsonResp);
    });
});



* Modify the client CSS to format Pokemon names with initial caps
pokemon_name {
  position: absolute;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 20;
  margin: 0;
  background-color: rgba(0, 0, 0, 0.5);
  color: #fff;
  text-align: center;
  font-size: 14px;
  pointer-events: none;
  text-transform: capitalize; /* Number two answer*/
}
