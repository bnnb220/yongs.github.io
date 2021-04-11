---
title: "깃허브 페이지 사용"
---
github 페이지를 만들어 보았다.

# test

## test

### test

## 1 ##
```
void Start()
{
    offset = tr.position - player.position;
}

void LateUpdate()
{
    Vector3 newPos = player.position + offset;
    tr.position = Vector3.Slerp(tr.position, newPos, smoothness(float));
}
```

Camera follows player depends on ths smoothness. (camera only views one way.)


## 2 ##

{
    offset = new Vector3(player.position.x, player.position.y + 8.0f, player.position.z + 7.0f);
}

void LateUpdate()
{
    var t = Quaternion.AngleAxis (Input.GetAxis("Mouse X") * speed, Vector3.up);
    offset =  t * offset;
    transform.position = player.position + offset; 
    transform.LookAt(player.position);
}

Quaternion.AngleAxis -> rotate this based on Vector3.up axis.
LookAt -> camera always look player.

