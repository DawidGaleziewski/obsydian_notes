there is never "always do x". Some algorithms will have better [[spatial complexity]] some will have better [[computational complexity]] and others times it does not matter or the most important factor is [[clean code]]

It is important to analyze best case scenario and worst case and wonder how often each will occure in the use case.

There can be multiple good choices as well.

Sometimes we do not want to ignore coefficiant like $3x^2$.

It is rearly a good idea to trade off readability for eaither [[spatial complexity]] or [[computational complexity]]

If you can use build-in javascrip methods like .sort() it is better to do so. Due to fact that javascript engienes like v8 can cheat and use C under to hood.

Also scaling problems are good problems to have, it is sometimes better to noit sacriface the speed of implementation.
