# [ModConsole](API/MSCLoader/ModConsole.md).ExecuteCommand

*public static void <b>ExecuteCommand</b>(string <b>commandString</b>);*  

#### Description

Executes a command by its string.

#### Parameters

Name | Description | Type
---- | ----------- | ----
commandString | command to Execute. | <font color=#4170a7>string</font>

#### Example

```csharp
public override void Load() 
{
    ModConsole.ExecuteCommand("clear"); //clears the Console.
}
```