# UdonList

List implementation for UdonSharp.

## Example

```cs
using UnityEngine;
using UdonSharp;
using Koyashiro.UdonList;

public class UdonListSample : UdonSharpBehaviour
{
    public void Start()
    {
        var list = UdonStringList.New(); // []
        list.Add("first"); // ["first"];
        list.Add("second"); // ["first", "second"]
        list.Add("third"); // ["first", "second", "third"]

        Debug.Log(list.Count()); // 3
        Debug.Log(list.GetItem(0)); // "first"
        Debug.Log(list.GetItem(1)); // "second"
        Debug.Log(list.GetItem(2)); // "third"
    }
}
```
