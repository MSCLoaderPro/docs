# [Bolt](MSCLoader.PartMagnet/Bolt/bolt.md).BoltSize

public [BoltSize](MSCLoader.PartMagnet/Bolt/BoltSizeenum.md) BoltSize { get; set; }

Returns and sets the Bolt size with an enumeration of the game's available tool sizes.

### Example
```cs
void ChangeBoltSize() 
{
	gameObject.GetComponent<Bolt>().BoltSize = BoltSize.Bolt6mm;
}
```







