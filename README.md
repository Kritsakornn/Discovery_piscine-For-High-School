# Discovery_piscine-For-High-School
Level 12.46 out of 13.57 levels.

    const TextOnGif = require('text-on-gif');

    (async function(){

        //create a TextOnGif object
        var gif = new TextOnGif({
          file_path: "https://media0.giphy.com/media/Ju7l5y9osyymQ/giphy.gif"
          //path to local file, url or Buffer
        });

        //get as buffer
        var buffer = await gif.textOnGif({
            text: "text on gif sucks",
            get_as_buffer: true
        });

        console.log(buffer);

        //write as file
        await gif.textOnGif({
            text: "text on gif sucks",
            get_as_buffer: false,
            write_path: "gif-with-text.gif"
        });

    })();
