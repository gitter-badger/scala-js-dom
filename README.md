scala-js-dom
============

Provides a nice statically typed interface to the DOM such that it can be called from Scala code without resorting to `js.Dynamic`.

Also contains useful extension methods in `org.scalajs.dom.extensions`, which allow the DOM api to be used in a more idiomatic and fluent way. The goal of this project is to provide a thin-but-idiomatic-scala interface to modern browser APIs. In particular:

- Deprecated properties/methods/types will not be present.
- IE-only, Chrome-only, FF-only, and in general browser-specific attributes will not be present.
- The name of a Scala type should map directly to the name of the corresponding Javascript type.
- Any type which is a Javascript type (e.g. you can `instanceof` in javascipt) should be a Scala `class`; any other interface which isn't a Javascript type should be a `trait`.
- Read-only members should be `def`, and not-directly-instantiable classes should have `private` constructors.
- `org.scalajs.dom` contains DOM class/member stubs, while `org.scalajs.dom.extensions` contains implicit conversions and useful Scala types (e.g. `Color`) to make usage of the DOM more idiomatic Scala.

See [scala-js-game-2](https://github.com/lihaoyi/scala-js-game-2) ([live demo](http://lihaoyi.github.io/scala-js-game-2/))and [scala-js-games](https://github.com/lihaoyi/scala-js-games) for an example of its use. There remain lots more cleanup to do, but this should be a reasonable place to start from. Pull requests/forks are welcome!

License
-------

Documentation marked "MDN" is thanks to Mozilla Contributors
at https://developer.mozilla.org/en-US/docs/Web/API and available
under the Creative Commons Attribution-ShareAlike v2.5 or later.
http://creativecommons.org/licenses/by-sa/2.5/

This should not affect you, as a user of the library, as long as you don't
modify these MDN materials (e.g. you leave them as is, or replace them
wholesale). In particular, packaging this library with MDN materials unchanged
is fine for any purpose (including commercial) according to the
CC-Attribute-ShareAlike License.

Everything else (e.g. the code) is under the MIT License

The MIT License (MIT)

Copyright (c) 2013 Li Haoyi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
