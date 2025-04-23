# Exp02-RollABall

## AIM:
To develop a 3D application for Roll A Ball in unity.

## ALGORITHM:
1. Create a new project.
2. Click Heirarchy -> 3D object -> Select the plane -> 3DObject -> Sphere.
3. Define the physics properties of the surface (Rigidbody).
4. Assets -> Create -> # Script
5. Create a folder name Coding and create a C# file to add the coding in it.
6. To add our C# Script file to our selected object, click on the C# Script file and drag it to our selected objects in the Hierarchy window nad run the application.
7. Stop.


## PROGRAM:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Move : MonoBehaviour
{
    public float xForce = 5.0f;
    public float zForce = 5.0f;
    public float yForce = 100.0f;
    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f, y = 0.0f, z = 0.0f;
        if (Input.GetKey(KeyCode.A))
        {
           x = x - xForce; 
        }
        if (Input.GetKey(KeyCode.D))
        {
           x = x + xForce; 
        }
        if (Input.GetKey(KeyCode.W))
        {
           z = z + zForce; 
        }
        if (Input.GetKey(KeyCode.S))
        {
           z = z - zForce; 
        }
        if (Input.GetKeyDown(KeyCode.Space))
        {
           y = yForce;
        }
        

        GetComponent<Rigidbody>().AddForce(x,y,z);
    }
}
```

## OUTPUT:

![Screenshot 2025-04-23 113236](https://github.com/user-attachments/assets/17d37cc5-ad03-4769-85f8-a500131a1f99)

![Screenshot 2025-04-23 113253](https://github.com/user-attachments/assets/b13d5891-1318-469e-b20b-776a2c94abc8)

## RESULT:
Thus, a 3D application for RollABall objects in unity is developed successfully.
