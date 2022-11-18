Check out the [readme](https://github.com/galaxykate/tracery) on the original repo.

Here's an example macro using this module:

```
var greeting = {
	"greeting": "#welcome#, #question#",
	"welcome": ["Hi","Hello","Good #timeofday#"],
	"timeofday": ["morning","afternoon","evening","night"],
	"question":["how are you?","how's it going?","what's going on?"],
}

grammar = tracery.createGrammar(greeting);

message = grammar.flatten("#greeting#")

ChatMessage.create({
	user: game.user._id,
	content: message
});
```
