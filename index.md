# Hello Heading 1!
![Rise and Shine Gordan Freeman](https://images.alphacoders.com/105/1053010.jpg)

```c
float Q_rsqrt( float number )
{
	long i;
	float x2, y;
	const float threehalfs = 1.5F;

	x2 = number * 0.5F;
	y  = number;
	i  = * ( long * ) &y;                       // evil floating point bit level hacking
	i  = 0x5f3759df - ( i >> 1 );               // what the fuck?
	y  = * ( float * ) &i;
	y  = y * ( threehalfs - ( x2 * y * y ) );   // 1st iteration
//	y  = y * ( threehalfs - ( x2 * y * y ) );   // 2nd iteration, this can be removed

	return y;
}
```

- [x] it's a beautiful day outside.
- [x] birds are singing, flowers are blooming...
- [x] on days like these, kids like you...
- [ ] Should be burning in hell.
