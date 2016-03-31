OCaml 2016 -- The State of the Hump
============================================

Its 2016 and we all know functional programming is the path forward,
from ReactJS to Elixir, MirageOS to Docker, Facebook flow to Elm, this
style of programming is clearly being widely adopted and needed.

This is my biased viewpoint coming from working in a startup in San
Francisco and from running the OCaml meetup group in Silicon
Valley. It's an expression of my frustations from the current
environment, from speaking to absolute programming beginners to
experienced JavaScript programmers and every variant of C in
between. It is not a criticism of any one person or organiztion,
rather it comes from a love of the community and OCaml itself.

Getting to the Next Stage
===============================

Tools like `opam` and `merlin` were desparately needed and got us to
what past the what I'd call the first hump, but now we need to get
past the second hump; to capture that group of programmers that just
need to have a `json` based HTTP request to work (1 line of code in
Python, at least 10 in OCaml + talk about monads).

What's missing for wide spread adoption
=================================================

(I'm talking about the average Silicon Valley tech startup, companies
that fundamentally just take JSON requests and persist them to
Postgres. This story in OCaml is severly lacking.)

Here's the TODO list, order doesn't mean priority.

These issues also overlap with why a typical SV startup might hesitate
to pick OCaml.

1. An actual ORM. Wrong or right they get stuff done. A nice feature
   would be something that used a PPX extension to generate type safe
   SQL and functorized over a backend, starting with
   `Postgresql`. Just hasn't been done. There are things that
   approximate this but they have various short comings in their own
   way.

2. Typical middleware needed for web application backends. We need
   something like `nodejs`'s express. Something that instantly handles
   30k+ connections, like I can in 30 lines of node `JavaScript`.

3. Documentation, documentation, documentation. We have amazing tools
   like `js_of_ocaml` but the documentation is lacking and only the
   most determined hackers stay.

4. A web framework in the spirit of Django or Rails. (And please not
   something that reachs `Yesod` levels of mental abstraction)

5. `js_of_ocaml` or `bucklescript` bindings to `ReactJS`, that would
   be ideal.

6. namespaces. This is a problem right now, name something `dispatch.ml`
   and use a transistive dependency that also defines dispatch. Boom.
   
7. A friendlier attitude towards web development. Many people still
   think web coding is lame or not serious. That's wrong, web
   programming is amazing and much innovation comes out of web
   programming.

8. Core libs like `Lwt` need love and care, simply not enough hands to
   go around at the moment.
   
9. Marketing. Haskell blows us out of the water in name recognition,
   no reason why we can't have that level of recogition as well.

10. The build situation is pretty bad, we have too many build tools
    with no consensus on building code. Explaining all of them at once
    to programmers coming from interpreted languages is a big time suck.