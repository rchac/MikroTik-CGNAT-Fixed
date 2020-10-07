# tools

MikroTik's wiki offers an almost-functional script to implement CG-NAT.
The only changes needed to make it work are to add 
```
:global sqrt
```
into the top of the second function, and to change 
```
:for i from=0 to=$x do={
```
to
```
:for i from=0 to=($x + 1) do={
```
The script on the wiki does not create the xxx jump rule for the last /30 of addresses due to the counter mistake. With these two changes it works correctly.
