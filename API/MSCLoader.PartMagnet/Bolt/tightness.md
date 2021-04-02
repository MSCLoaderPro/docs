# [Bolt](MSCLoader.PartMagnet/Bolt/bolt.md).tightness

public int tightness;

Current tightness. This is increased/decreased as the bolt is screwed.

### Example
```c#
void ChangeBoltSize() 
{
	int boltTightness = gameObject.GetComponent<Bolt>().tightness;
}
```







