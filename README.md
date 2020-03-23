// The Poker Game

let player1 = [];
let player2 = [];
let player3 = [];
let player4 = [];
let player5 = [];
let board = [];

let deckOfCards = [
    "D2", "C2", "H2", "S2", 
    "D3", "C3", "H3", "S3", 
    "D4", "C4", "H4", "S4", 
    "D5", "C5", "H5", "S5", 
    "D6", "C6", "H6", "S6",
    "D7", "C7", "H7", "S7", 
    "D8", "C8", "H8", "S8",  
    "D9", "C9", "H9", "S9",
    "D10", "C10", "H10", "S10", 
    "DQ", "CQ", "HQ", "SQ", 
    "DJ", "CJ", "HJ", "SJ", 
    "DK", "CK", "HK", "SK", 
    "DA", "CA", "HA", "SA"
];

//console.log(deckOfCards); // for debug

// method for get new card from the deck and return new array without pop cart
let getNewCard = deckOfCards => {
    let rand = Math.round(Math.random() * (deckOfCards.length-1));
    let cart = deckOfCards[rand];
    //console.log(cart); // for debug
    deckOfCards.splice(rand, 1);
    return cart;
};


// metod razdachi kart igrokam - 1 krug po 1 karte kajdomu
let distributionOfCards = () => {
    player1.push(getNewCard(deckOfCards));
    player2.push(getNewCard(deckOfCards));
    player3.push(getNewCard(deckOfCards));
    player4.push(getNewCard(deckOfCards));
    player5.push(getNewCard(deckOfCards));
};
// We gave the players two cards
distributionOfCards()
distributionOfCards()


// "In board will be 3 cards"
board.push(getNewCard(deckOfCards));
board.push(getNewCard(deckOfCards));
board.push(getNewCard(deckOfCards));

