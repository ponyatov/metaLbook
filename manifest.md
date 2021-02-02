# metaL manifest

https://www.notion.so/metaL-manifest-f7c2e3c9f4494986a620f3a71cf39cff

- **no-syntax language** defined over **executable data structures**
    - there are no syntax parser and source code files
    - any composite data structure can be
      [Active](https://www.notion.so/metalang/Active-41b3cfc2de9e46538ff689a08ab98164)
      by using **EDS-interpreter** which executes it programmatically

- the most universal data structure is the **[object graph](https://en.wikipedia.org/wiki/Object_graph)** of frames
    - frame concept is taken from [Marvin Minsky's
      frames](https://web.media.mit.edu/~minsky/papers/Frames/frames.html)
      [[minsky](https://web.media.mit.edu/~minsky/papers/Frames/frames.html)]
      *extended with ordered storage*
    - any
      [Object](https://www.notion.so/metalang/Object-2639c9b82f13498cb95c5aaa5e6e752a)
      must have these fields:
        - `class:type` tag holds the type of any object in runtime (low-cased
          class name)
            - host languages with RTTI/reflection are able to hold references to
              class as is
            - low-level host languages such as C++ should reference to static
              class name string
        - `scalar:value`single **scalar value**: object name, string, number,..
          (in host-language type)
        - `dict:slot{}` **associative array** *of names* which were bound to
          subgraphs
        - `vector:nest[]` **ordered storage** for nested subgraphs
        - `set:par||` **parent elements** (required for [attribute
          grammar](https://en.wikipedia.org/wiki/Attribute_grammar) attributes
          computation and parent nodes addressing from children nodes)
            - `ref ~ len(par)` reference counter not used directly, as `par`
              registry takes its role and must be recounted to check is the
              current object used anywhere
        - `int32:gid` **unique global storage id** — fast 32-bit
          [xxhash](http://cyan4973.github.io/xxHash/) over object contents
            - **metaL** looks very intently to the [UnisonWeb
              concept](https://www.unisonweb.org/talks) about immutable global
              storage which holds shared objects by its content hashes
        - optional behavior-specific fields
    - any graph combined from the **Object-inherited nodes** has unified
      interfaces for its building and manipulations
- the main method of programming is the **generative metaprogramming**
    - the **metaL method** is the sandwich of three languages:
        - **host language** in which most work is going and other language
          layers implemented /Python/
        - the [metaL]ayer implemented by executable data structures
          interpretation (homoiconic object graph)
        - **target languages**: all projects use not less than 3..5 programming
          and scripting languages, and config file formats
    - **frame graph** is an universal unified data structure for **arbitrary
      knowledge representation**
        - *source code in any languages* in a form analogous to AST and attribute grammar trees (extended to cyclic attributed no-syntax graphs)
        - *generic program representation* and procedures for graph transformations
        - domain and source code *models* ([Model-Driven Engineering](https://en.wikipedia.org/wiki/Model-driven_engineering))
        - any application-specific data
    - programmer writes target application model by combining software model
      elements
        - every graph node class knows how to compiler itself into source code in target languages, or into other graph node types which able to do it in turn
        - all models are shared between projects which programmers do over time, so
            * projects and its dedicated components can be classified and inherited

- the programmer builds his own version of the metaL system from scratch
    - all required knowledge to write minimal reference implementation should be
      described in a manual step by step
        - first steps are easy enough to make your custom language system usable
          without familiarity with [classical
          books](https://www.notion.so/metalang/7c1984c0cb7b4b25ac91158aca8d644b)
          such as [SICP], [PLAI], [TAPL], and [dragon]
        - the desire of using more effective programming methods stimulates you
          in learning more complex concepts from classical & modern CS.    
    - the programming process is free in the selection of programming paradigms,
      methods, and approaches -- anything that some programmer is able to
      implement at a metaLevel, can be used with the condition of personal
      understanding of how it works
    - resulting target code can be distributed to the working group as is,
      without forcing anybody to dive into senior-level concepts, cryptic
      language, and disclosure of programming methods were used
        - metaL can be used as a [secret
          weapon](http://www.paulgraham.com/avg.html) and personal know-how
          without inflicting risks on the employer and working team
        - the more effective development tool suggests you investigate into
          leveling-up your skills and makes you more valuable to the labor
          market
        - your programming knowledge and skills are represented in a computer
          form thus it is machine-readable, executable, and transformable
        - metaL can be treated as a
          [CASE](https://en.wikipedia.org/wiki/Computer-aided_software_engineering)
          system without braindead GUI, but it is some sort of *language-based*
          self-bootstrapping
          [RAD](https://en.wikipedia.org/wiki/Rapid_application_development)
