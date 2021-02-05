# Generic Code Templating

The idea of metaL originates from an idea of the generic code templating: any
mainstream programming language we're using any day at work or for a hobby is
limited by its vendors, the huge community which uses it, and a language stack
of tools and libraries. Even if you have enough skills to take something like
CPython implementation and hack it to add some language modifications you want,
you never can use it in production -- these mods make the language incompatible
with the generic branch, and the most important it makes your team developers
incompatible with the rest of community. If you try to use your own hacked
Python or some homebrewed language for work, you will be kicked by your employer
and team as it introduces risk in hiring new developers, adds vendor lock on
uncommon language and tools, and dissipates efforts also on custom language
support.

The idea about code templating is a way of taking the power of custom
highest-level language still having no incompatibles with your production team.
In most cases, nobody locks you on the IDE you use for development, so if you
also add some shadow tool that generates human-readable code in the mainstream
language of your team, you'll have a chance to take the power without risks
shown above.

The problem is how can we make some language especially designed to be such a
magic wand. First of all, it must be very flexible and dynamic, and at the same
time it must not be effective and fast in terms of computation, it should be
just fast enough and not more. Next, it is required that this language must have
the highest extensibility to let you describe and implement any method or
approach of programming you desire. Lisp language dialects are well known at
this position, but they have scary syntax and at the same time are well-known as
esoteric. So, to make such a magic language, we can take the Lisp dynamic
nature, implement its runtime in any language you prefer (Python), cover it with
infix syntax parser which can be extended by a user as he wants, and finally
focus on making jigs and features suitable for describing software systems at
the highest level and simplifying of code generation.

The reverse path is the legacy code analysis from source code to high-level
models. There is a common problem of moving some old software systems to a new
language stack with fixing a lot of architecture bugs. I can't remember any
freeware tool or system which able to provide an environment for sucking in
source code in arbitrary (ancient) languages, which can provide a handy way for
reverse engineering, making software models, detecting used algorithms and
methods, and regenerating software from these refurbished models.
