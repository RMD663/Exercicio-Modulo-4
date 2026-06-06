# Unity-Exercicio-Modulo-4

Codigo da Atividade
``` C#
using UnityEngine;
using UnityEngine.InputSystem;
using UnityEngine.Rendering;


public enum ANIMAL
{
    DOG,
    CAT,
    BIRD,
}

public class Animals : MonoBehaviour
{

    public ANIMAL animal;

    void Start()
    {
        
    }

    void Update()
    {
        ProcessInput();
    }


    void ProcessInput()
    {
        if (Keyboard.current == null) return;

        if (Keyboard.current.aKey.wasPressedThisFrame)
        {
            animal = ANIMAL.CAT;
            PrintAnimal();
        }
        else if (Keyboard.current.sKey.wasPressedThisFrame)
        {
            animal = ANIMAL.DOG;
            PrintAnimal();
        }
        else if (Keyboard.current.dKey.wasPressedThisFrame)
        {
            animal = ANIMAL.BIRD;
            PrintAnimal();
        }
    }
    
    void PrintAnimal()
    {
        switch (animal)
        {
            case ANIMAL.CAT:
                Debug.Log("Cat was selected");
                break;
            case ANIMAL.DOG:
                Debug.Log("Dog was selected");
                break;
            case ANIMAL.BIRD:
                Debug.Log("Bird was selected");
                break;
            default:
                Debug.Log("Invalid value");
                break;
        }
    }
}
```


```
