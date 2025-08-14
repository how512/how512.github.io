

# why LLMs suck at mental advice

they truly do, <br>
and, <br>
unless something fundamentally changes, <br>
it's gonna stay this way,

because they are shallow, <br>
trained on massive amounts of text, <br>
but not the intent or reasoning behind it

they don't think when answering, <br>
they offer a "line of best fit" <br>
the best next token, <br>
an average of its training data

but how can it answer to something it was not trained on? <br>
it approximates, <br>
as with all inference, <br>
the next token is approximated based on all its training, <br>
LLMs are good at picking up patterns <br>
(that's the whole point), <br>
so, those approximations can be good, <br>
if common enough in the training data, <br>
but the further you stray from what has seen, the worse it becomes,


so

this is a model, <br>
one that was trained at some point, <br>
and now it's just a huge file of adjusted weights, <br>
it stays the same unless trained further

and this is the inference process, <br>
said model is loaded into a computer, <br>
and supplied context, to find the best next token

what is context? <br>
essentially a text file passed to the model, <br>
containing current dialogue,  <br>
gets bigger the longer you chat,  <br>
but, on each turn, the ever growing file, <br>
is passed to the same fixed model regardless, <br>
tho it knows what parts to "pay attention" to, <br>
for better predictions, <br>
and each model has fixed number of maximum tokens it can operate with

it may contain three "roles"

system, <br>
usually at the top,  <br>
containing generic instructions, <br>
I.e. "you're helpful ai assistant, yada yada" <br>
may be big, small, or non existent
used to steer the model, <br>
but it can't change the "world" the model lives in, <br>
the "world" here being embedding space 
(more on that later)

user, <br>
you, essentially, <br>
contains your messages

and finally <br>
assistant, <br>
where the model generates tokens

but what are those? <br>
LLMs don't understand language the same way we do <br>
they are trained on tokens, <br>
in English, <br>
one token is roughly one word

how text is converted to tokens and vice versa, <br>
is up to tokenizer, <br>
its job is to, well, convert, encode into tokens, <br>
making a dictionary,  <br>
containing all tokens for later decoding,

and that's what LLMs work with,  <br>
not words, but those tokens, <br>
they don't know the letters that make each word, <br>
all they know is tokens,

if trained on enough of those,  <br>
it may respond in a "natural" way,

but it still operates in tokens, <br>
so, for example, <br>
if you make a typo,  <br>
it's gonna be a different token, <br>
form the intended word, <br>
but the model still "understands" what you meant, <br>
how?

now it's time to finally talk about the embedding space

--- 
(WIP | next steps: embedding space)

↓ not ready to read yet

meaning, direction, similar words
typo trained similar on typo context, 
the more common the better
