## Dependencies

> Explicitly declare and isolate dependencies

**An app never relies on implicit existence of system-wide packages**. It declares all dependencies, completely and exactly, via a dependency declaration manifest. Furthermore, it uses a dependency isolation tool during execution to ensure that no implicit dependencies “leak in” from the surrounding system. The full and explicit dependency specification is applied uniformly to both production and development.

- For golang code, we use [go dep](https://github.com/golang/dep) and [go
  module](https://github.com/golang/go/wiki/Modules) to mangage dependencies.
- For javascript code, we use [npm](https://www.npmjs.com) to mangage
  dependencies.
- For iOS / macOS app, we use [Carthage](https://github.com/Carthage/Carthage)
- For Android, we use Gradle which is a built-in tool in Android.

Every dependency should be pin a clear version for stability and should be cloned into the code repo.
