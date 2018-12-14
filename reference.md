# Reference Manual

## Onboard LED

`led` method controls onboard LED. 
`led` has one parameter(0 or 1) which means LED off or on.

Example:

```ruby
while true
  led 1
  sleep_ms 500
  led 0
  sleep_ms 500
end
```

## Onboard Button

`sw` method returns current onboard button status. If the button is pressed, `sw` returns 1 otherwise returns 0.

Example:

```ruby
if sw() == 1 then
  led 1
else
  led 0
end
```

## Digital Output

`output` method controls output voltage of P3.0 to P3.7 on board.
`output` has two parameters, first parameter(0 to 7) means pin number P3.0 to P3.7 and second parameter(0 or 1) means output voltage(low or high).

Example:

```ruby
while true
  output 2,0
  output 0,1
  sleep_ms 500
  output 0,0
  output 1,1
  sleep_ms 500
  output 1,0
  output 2,1
  sleep_ms 500
end
```

## PWM Output

`pwm` method controls PWM(Pulse Width Modulation) signal of P0.0 to P0.3.
`output` has two parameters, first parameter(0 to 3) means pin number P0.0 to P0.3 and second parameter(0 to 255) means duty ratio of PWM.

Example:

```ruby
for i in 0..255 do
  pwm 0, i
  sleep_ms 10
end
```

## ADC Input

`adc` method returns adc value of P.



