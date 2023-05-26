using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class teleport : MonoBehaviour
{ 
    public Vector3 targetPosition; // The position where you want the sphere to move

// Start is called before the first frame update
void Start()
{
    targetPosition = new Vector3(-5f, 80f, 0f);
}

// Update is called once per frame
void Update()
{
}

// Upon collision with another GameObject, another GameObject will turn green
private void OnTriggerEnter(Collider other)
{
    // Move the ball to the new location!
    Debug.Log("HIT DETECTED!");

    GameObject.FindWithTag("ball").transform.position = targetPosition;
}
}
