# wp-shortscore-api

There are two APIs available to access the contents of SHORTSCORE: One for the SHORTSCORES and one for the recent GAMES. 

## SHORTSCORE API

json read-only api for shortscore data by shortscore id (comment id)

API endpoint is this: `https://shortscore.org/?get_shortscore=[shortscore_id]`

The Shortscore ID is the wordpress comment id. 

### example request

https://shortscore.org/?get_shortscore=374 

will output

{
   shortscore: {
       id: "374",
       author: "stefan",
       userscore: "10",
       summary: "To keep it short: One of the best games, I&#039;ve ever played.",
       url: "http://shortscore.org/game/dark-souls/#comment-374"
   },
   game: {
       id: "745",
       title: "Dark Souls",
       url: "http://shortscore.org/game/dark-souls/",
       shortscore: "9.5",
       count: "4"
   }
}

### what can I do with it?

Don't worry. We got you covered with a full featured wordpress plugin for easy integration:
https://github.com/MarcDK/wp-shortscore 

## GAMES API

https://shortscore.org/wp-json/shortscore/v1/list-recent-rated-games/?offset=0&paged=1&per_page=10

[...]