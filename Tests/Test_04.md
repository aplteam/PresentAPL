# Test Code Block testing

## Single number

[Data]: scalar=3.14

```
q←#.⎕NS''
q.⎕FX 'r←PI' 'r←3.14'
q.PI
```

⍎⍎#.PresentAPL.PresentAPL.CheckSlide ¯1⍎⍎

## Vector with two items

* This
* That
* Bla

[Data]: vector=5050 3628800

```
      (+/⍳100)(×/⍳10)
```

⍎⍎#.PresentAPL.PresentAPL.CheckSlide⍎⍎

## 2 x 3 Matrix 

[Data]: matrix=[1 2 3 ⋄ 4 5 6 ]

```
      2 3⍴⍳6
```

⍎⍎#.PresentAPL.PresentAPL.CheckSlide⍎⍎

## String

[Data]: string='Hello world'

```
      'Hello world'
```

⍎⍎#.PresentAPL.PresentAPL.CheckSlide⍎⍎

## String with function call

[Data]: string='Hello world'

```
      {'Hello ',⍵}'world'
```

⍎⍎#.PresentAPL.PresentAPL.CheckSlide⍎⍎

## Multiple lines

[Data]: multiple=3.14 'Hello world' [1 2 3 ⋄ 4 5 6]

```
      3.13
      'Hello world'
      2 3⍴⍳6
```

⍎⍎#.PresentAPL.PresentAPL.CheckSlide⍎⍎

