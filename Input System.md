Create -> Input Actions (Generate C# Class)
Add Control Scheme (Device Type: Keyboard & Mouse)
Create Action Map
Create Action
- Action Type: Value / Button / Pass Through
- Control Type: Vector2

Add Up \ Down \ Right \ Composite
- Composite -> Mode: Digital

Binding Properties
 - Check Scheme
 - Path: Set the binding path (e.g., bind key).

Apply Input Action

```cpp
private PlayerInputSet input;
public Vector2 moveInput { get; private set; };
```



```cpp
/ * Action Maps -> Actions * /
input.Player.Movement.started
input.Player.Movement.performed
input.Player.Movement.canceled
```

### Initialize Input System:
```cpp
private void Awake()  
{  
	input = new PlayerInputSet();  
}
```

### Enable/Disable Input:
```cpp
private void OnEnable()  
{  
    input.Enable();
    
    input.Player.Movement.performed += ctx => moveInput = ctx.ReadValue<Vector2>();  
	input.Player.Movement.canceled += ctx => moveInput = Vector2.zero;
}
```

```cpp
private void OnDisable()  
{  
    input.Disable();  
}
```

### Handle Input in Code:
```cpp
if(moveInput.x != 0){
	// character is moving align x axis
}

if(moveInput.x == 0){
	// character is not moving
}
```