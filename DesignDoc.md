# G.E.N.E.S. 2
Generational Evolution Non-Euclidian Simulation

## Returning Features
### Random Genome Generation and Parsing-
Generate a random binary string of length `genomeLength` and parse it using the following:
> ### Format
> __xxxyyyzz zzzzzzzz__
>> __Key__
>>
>> "xxx" = Source Node Type Identifier in Binary
>>
>> "yyy" = Sink Node Type Identifier in Binary
>>
>> "zzzzzzzzzz" = Sink Weight in Binary
>>
>
>>    
>> __Binary Conversion of Sink Weight__
>>
>> The 10 digit binary string is converted to decimal using a bias of 512 which results in an initial range of [511, -512]. This range is then shrunk to [0.998, -1] by dividing by 512 and rounding to the nearest ten thousandth.
> ### Example
> __00111111 10100111__
>
> __-or-__
>
> __001 111 1110100111__
>
>> __Decoded__
>>
>> 001 = Source Node Type 1
>>
>> 111 = Sink Node Type 7
>>
>> 1110100111 = Sink Weight of -0.174

### Deep Simulation Customization

### Simulation Screen

### Subject Brain Map Screen


## New Features

### Step Viewing and Replays

### Customizable Environmental Pressures

### Simulation Statistics Screen



