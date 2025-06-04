
```cpp
private void OnDrawGizmos()  
{  
    Gizmos.DrawLine(transform.position, transform.position + new Vector3(0, -groundCheckDistance));  
}
```