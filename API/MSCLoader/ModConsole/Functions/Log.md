# [ModConsole](API/MSCLoader/ModConsole.md).Log

*public static void <b>Log</b>(string <b>text</b>);*  
*public static void <b>Log</b>(object <b>obj</b>);*  
*public static void <b>Log</b>(IList <b>list</b>, bool <b>printAllElements</b> = true);*

#### Description

Logs a string, object or list into the ModConsole window, and also to the output_log.txt.

Supports [Unity Rich Text](https://docs.unity3d.com/500/Documentation/Manual/StyledText.html)

#### Parameters

Name | Description | Type | Default
---- | ----------- | ---- | -------
text | String to log | <font color=#4170a7>string</font> | N/A
obj | Object that gets converted into a string and logged | <font color=#4170a7>object</font> | N/A
list | List that gets converted into a string and logged | <font color=#aac397>IList</font> | N/A
printAllElements | Should all elements in the list get logged? | <font color=#4170a7>bool</font> | <font color=#4170a7>true</font>

#### Example

```csharp
public override void PreLoad() 
{
    ModConsole.Log("YEEHAW");

    Transform hoss = GameObject.Find("HOSS").transform;
    ModConsole.Log(hoss);

    int[] provisions = { 1, 0, 12, 5, 7, 4 };
    ModConsole.Log(provisions);
}
```