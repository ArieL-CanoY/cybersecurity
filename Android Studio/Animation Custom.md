Folder Path:
	res > anim > fileAnim.xml
```xml
<set>
	<alpha
		android:fromAlpha="0"
		android:toAlpha="1"
		android:duration="500"/>

	<translate
		android:fromYDelta="-200%"
		android:toYDelta="0%"
		android:duration="500"/>
</set>
```

# Explanation
- alpha - opacity
	- fromAlpha - 0 for 0% opacity
	- toAlpha - 1 for 100% opacity
	- duration - milliseconds duration from 0% to 100% opacity
- translate - move position
	- fromYDelta = -200% is position 2 times above the current position
	- toYDelta = 0% is position where you set the view
	- duration - milliseconds duration from 200% to 0% position




















