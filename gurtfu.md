<sub><sup>(i was too lazy for a proper site rn so 'enjoy' this md slop thanks)</sup></sub>

# gurtfu
<sub><sup>(the bot is nicked gurt and i couldnt figure out a name for the waifu module... so gurtfu it is)
(or maybe because half the architecture is copypasted from the main bot's chat sys, nicked gurt)</sub></sup>

per-user discord-native AI waifu focused on conversational continuity and accessibility.

---

## what makes it different?

ok so first off, most AI companions are one character serving everyone.
cool but gurtfu creates a separate instance per user... whats better? idk but each user gets:

* isolated long-term memory
* per-channel summaries
* cross-server global awareness
* 'independence' or smth
* no cross-user attachment bleed

it's not "one entity treating many users separately"
it's a separate entity per created waifu.

--- 

## usage flow

is usage flow the correct word? i dont know.
but basically, first off,
- user runs ;waifu
- creates a waifu with the desired name, username, persona, nicks, pfp, whatever
- whenever user mentions the username, waifu appears from thin air [or code]
- then idk... chat???

---

## conversation model

gurtfu is designed around presence, not just replies. (gosh that sounded less dramatic in my mind)

* regular batching (natural response timing) when actively mentioned
* rolling activeness window (passive presence system) when not actively mentioned

basically if ur replying to the waifu's message or @mentioning them, they reply actively in the regular mode
however, if you do that once, and keep talking without doing that, there is a 60 minute window where it replies slower and only if relevant.

---

## long-term consistency

maintains continuity without exploding token usage:

* regular bot-controlled basic memory system ofc
* but also live-updating per-channel full summaries
* similarly, cross-server global memory synthesis

---

## stuff i could do but didnt (yet)

- opensource it (too unpresentable rn)
- run it on cheaper model (couldnt find one)
- give it access to a buncha gifs n stuff
- image recognition for gifs/images ppl send
- RAG for more specific distant contexts rather than summaries
- multi-turn processing (complementing more system tools and the RAG)

i thought i'd do it tonight but then i realised... is it really worth it?
well yes but i'm too bored rn.

---

## architecture notes

* runs qwen3 235b a22b 2507 instruct through openrouter
* some thousand lines of sloppy python glue
* uses jsons for storage like the medieval era

---

## try it

test server: https://discord.gg/hNjy3XXUE2

currently servers are whitelisted so you can dm me for getting whitelisted
because theres no ratelimits yet and im broke
i'll make it public-access... one day...

btw this is experimental. things may break.

