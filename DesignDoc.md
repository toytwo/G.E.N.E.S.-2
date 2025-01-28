# G.E.N.E.S. 2
Generational Evolution Non-Euclidian Simulation

## Old Features
### Random Genome Generation and Parsing-
Generate a random binary string of length `genomeLength` and parse it using the following format:
> ### Format
> __xxxyyyzz zzzzzzzz__
>> __xxz__ = Source Node Type Identifier
>>
>> __yyy__ = Sink Node Type Identifier
>>
>> __zz__ = Sink Weight in Binary (signed int with a bias)
> ### Example
> __00111111 10100111__
>> 001 = Source Node Type 1
>> 111 = Sink Node Type 7
>> 1110100111 = Sink Weight of 8



