const sdk = require('node-appwrite');

// Init SDK
let client = new sdk.Client();

let avatars = new sdk.Avatars(client);

client
    .setProject('5df5acd0d48c2') // Your project ID
;

let promise = avatars.getQR('[TEXT]');

promise.then(function (response) {
    console.log(response);
}, function (error) {
    console.log(error);
});