# Platform Engineering Interview: Rust

## The Problem

We would like you to come up with a new binary file format for storing configuration files. Your configuration is defined in a Rust struct that could have boolean, integer, string, or array typed properties. Let's take the following example file:

```json
{
    "property 1": "a",
    "property 2": 100,
    "property 3": false,
    "property 4": [
        "hello", 200, true
    ]
}
```

We want you to come up with a highly _compact_ representation for this configuration file, that absolutely minimizes the amount of space taken up. You should not use an existing tool or system, e.g. protobufs, etc. We want to see you write a serializer / deserializer yourself. Your system can be written as a set of two methods that convert to and from a Rust struct to this file, e.g.:

```rs
pub trait MyFormat<S> {
    fn serialize(file: Vec<u8>) -> S;
    fn deserialize(data: S) -> Vec<u8>;
}
```

Your goal should be to use as compact of a representation as possible, while still maintaining the ability to read and write to arbitrary schema types. Note that your schema does not have to be "self describing", i.e. you do not need the file to be read by any arbitrary application. Your goal is to maintain correctness as well as compactness. In doing so, there is not one single answer. Certain approaches will be compact for certain schemas, while not for others. So feel free to make all your assumptions about these schemas clear.

## Questions

1. How would you think about code maintainability here. Don't write any tests, but give some ideas for how a test suite could confirm the correctness of this code at compile time or test time.
2. What if you wanted to make the schema self-describing. How would you change your implementation?
3. What if you wanted to prioritize speed rather than compactness? What if you wanted to prioritize both equally?
4. How would you modify your code to support direct access? In other words, could you read a single property without deserializing the entire file?
5. How would you extend your solution to further property types and increasing levels of nesting?

## Resources to solve this problem

You are totally free to use any resources you can imagine, including tutorials you find online, etc. You may also feel free to use LLMs or AIs of any kind, though most of this problem is about your approach and opinions rather than the standard best practice. Can you include ideas and techniques that come from past work you've done? Is there a certain type of system for which you have a particularly awesome solution?

## What are we looking for?

Our goal is to see if you understand the basic capabilities of Rust, and that you have a creative mind for problem solving that shines through in your solutions. 

## What are we not looking for?

1. Tests (you don't need to write any, though it's often to write them as you work! You can leave in whatever ones your have if you want, though we won't look at them).
2. Derive/Proc Macros (you don't need to make your solution totally, 100% ergonomic, just come up with the core strategy).
3. Documentation (you don't need to extensively comment your code beyond what is helpful to you, nor do you need to write out an extensive README beyond addressing the question and describing the solution)
