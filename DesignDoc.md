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

As such, `genomeLength` must but a multiple of 16 where `genomeLength` divided by 16 is number of genes a subject will have and the minimum number of nodes in a subject's brain.

### Deep Simulation Customization

### Simulation Screen

### Subject Brain Map Screen


## New Features

### Step Viewing and Replays

### Customizable Environmental Pressures

### Simulation Statistics Screen

### Accurate Genetic Relativity
Subjects will be colored in such a way that subjects with similar genetics will have a similar color.

#### Possible Approaches-

__Combination Mapping__

Direct comparison of genomes will not yield accurate results because identitcal genomes could be generated in different orders. However, there are a finite number of potential genes regardless of `genomeLength`. As a result there are also a finite, although large, number of combinations of genes. We could precalculate all of these combinations and then map similar combinations to simular positions within the RGB spectrum. All of this could be precalculated or calculated at the beginning of runtime in order to reduce computation times between generations.

__Gene Expressed Colors__

Perhaps we include an additional gene within the subject that simply determines it's color. The advantage would be that offspring would share this color or we could force mutation of this gene when any other gene mutates in order to ensure genetic drift within the color. The disadvantage of this approach would of course be that it would be possible for two differing genomes to contain the same color gene.

__Gene Markers__

The following marker generation method could be used for combination mapping or another genetic similarity algorithim:

> __Gene Format__
> 
> xxxyyyzz zzzzzzzz
>
> __Identifier One:__ xxx
>> Convert xxx to decimal form.
>
> __Identifier Two:__ yyy
>> Convert yyy to decimal form.
>
> __Identifier Three:__ zzzzzzzzzz
>> Convert zzzzzzzzzz to decimal form but only take the sign. In the case of 0, genes with no sink weight will be eliminated and therefore not considered.
>
> __Marker Format__
>
> zxy 
>
> Where z is a sign, x is a decimal number, and y is a decimal number.
>
> __Example__
>
> 10101110 11101010
>
> xxx --> 101 --> 5
>
> yyy --> 011 --> 3
>
> zzzzzzzzzz --> 1011101010 --> 234 --> +
>
> _Resulting Marker:_ __+53__

In this way, markers can be numerically analyzed to determine similarity. For example, +43 and +33 or +43 and +44 could be considered similar but would also be distinct from their negative counterparts.



