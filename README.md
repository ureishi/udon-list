# UdonList

List implementation for UdonSharp.

## Example

String list exmaple.  
You can also make UdonList\<int\>, UdonList\<float\>, UdonList\<bool\>, UdonList\<object\> and so on.

```cs
using UnityEngine;
using UdonSharp;
using Koyashiro.UdonList;

public class UdonListSample : UdonSharpBehaviour
{
    public void Start()
    {
        var list = UdonList<string>.New(); // Same as C# "new List<string>();"
        list.Add("first");     // ["first"]
        list.Add("second");    // ["first", "second"]
        list.Add("third");     // ["first", "second", "third"]
        list.Remove("second"); // ["first", "third"]

        // List to array
        var convertedArray = list.ToArray();

        // Array to list
        var convertedList = UdonList<string>.New(convertedArray);

        // Alternative foreach
        for (var i = 0; i < convertedList.Count(); i++)
        {
            Debug.Log(list.GetItem(i)); // "first", "third"
        }
    }
}
```

## Remarks

## Reference

### Constructors
<table>
   <tr>
     <td nowrap><code>UdonList&lt;T&gt;.New()</code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code>UdonList&lt;T&gt;.New(T[] collection)</code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code>UdonList&lt;T&gt;.New(int capacity)</code></td>
     <td> </td>
   </tr>
</table>

### Properties
<table>
   <tr>
     <td nowrap><code> int Capacity </code></td>
     <td> <code>Capacity()</code>, <code>SetCapacity(int capacity)</code> </td>
   </tr>
   <tr>
     <td nowrap><code> int Count </code></td>
     <td> <code>Count()</code> </td>
   </tr>
   <tr>
     <td nowrap><code> T Item </code></td>
     <td> <code>GetItem(int index)</code>, <code>SetItem(T item)</code> </td>
   </tr>
</table>

### Methods
<table>
   <tr>
     <td nowrap><code> void Add(T item) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void AddRange(T[] collection) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void Clear() </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> bool Contains(T item) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void CopyTo(int index, T[] array, int arrayIndex, int count) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void CopyTo(T[] array, int arrayIndex) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> int EnsureCapacity(int capacity) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> object[] GetRange(int index, int count) </code></td>
     <td> ! </td>
   </tr>
   <tr>
     <td nowrap><code> int IndexOf(T item) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> int IndexOf(T item, int index) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> int IndexOf(T item, int index, int count) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void Insert(object[] list, int index, T item) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void InsertRange(int index, T[] collection) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> int LastIndexOf(T item) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> int LastIndexOf(T item, int index) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> int LastIndexOf(T item, int index, int count) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> bool Remove(T item) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void RemoveAt(int index) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void RemoveRange(int index, int count) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void Reverse() </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void Reverse(int index, int count) </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void Sort() </code></td>
     <td> <code>where T : IComparable</code> </td>
   </tr>
   <tr>
     <td nowrap><code> void Sort(int index, int count) </code></td>
     <td> <code>where T : IComparable</code> </td>
   </tr>
   <tr>
     <td nowrap><code> T[] ToArray() </code></td>
     <td> </td>
   </tr>
   <tr>
     <td nowrap><code> void TrimExcess() </code></td>
     <td> </td>
   </tr>
</table>



