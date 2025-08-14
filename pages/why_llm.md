

# why LLMs suck at mental advice

they truly do, <br>
and, 
unless something fundamentally changes,
it's gonna stay this way,

because they are shallow,
trained on massive amounts of text, 
but not the intent or reasoning behind it

they don't think when answering,
they offer a "line of best fit"
the best next token,
an average of its training data

but how can it answer to something it was not trained on?
it approximates,
as with all inference,
the next token is approximated based on all its training,
LLMs are good at picking up patterns
(that's the whole point),
so, those approximations can be good,
if common enough in the training data,
but the further you stray from what has seen, the worse it becomes,


so

this is a model,
one that was trained at some point,
and now it's just a huge file of adjusted weights,
it stays the same unless trained further

and this is the inference process,
said model is loaded into a computer,
and supplied context, to find the best next token

what is context?
essentially a text file passed to the model,
containing current dialogue, 
gets bigger the longer you chat, 
but, on each turn, the ever growing file,
is passed to the same fixed model regardless,
tho it knows what parts to "pay attention" to,
for better predictions,
and each model has fixed number of maximum tokens it can operate with

it may contain three "roles"

system,
usually at the top, 
containing generic instructions,
I.e. "you're helpful ai assistant, yada yada"
may be big, small, or non existent
used to steer the model,
but it can't change the "world" the model lives in,
the "world" here being embedding space 
(more on that later)

user,
you, essentially,
contains your messages

and finally
assistant,
where the model generates tokens

but what are those?
LLMs don't understand language the same way we do
they are trained on tokens,
in English,
one token is roughly one word

how text is converted to tokens and vice versa,
is up to tokenizer,
its job is to, well, convert, encode into tokens,
making a dictionary, 
containing all tokens for later decoding,

and that's what LLMs work with, 
not words, but those tokens,
they don't know the letters that make each word,
all they know is tokens,

if trained on enough of those, 
it may respond in a "natural" way,

but it still operates in tokens,
so, for example,
if you make a typo, 
it's gonna be a different token,
form the intended word,
but the model still "understands" what you meant,
how?

now it's time to finally talk about the embedding space

--- 
(WIP | next steps: embedding space)

↓ not ready to read yet

meaning, direction, similar words
typo trained similar on typo context, 
the more common the better
