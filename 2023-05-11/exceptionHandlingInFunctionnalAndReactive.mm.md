# Exception handling in functionnal and reactive programming

## functionnal VS imperative

- more easy to read etc. (IMO, not all time)

## exception

- exception handling is an imperative style programming idea
- functionnal programming and exception handling are mutually exclusive

### with functionnal code
- deal with it down stream
- treat errors as a form of data

## live coding

- example with a little java main application 
  - code interface
  - use union of data
  - `public sealed interface Try<T> permits Success, Failure ..`