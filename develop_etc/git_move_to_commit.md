## Git MoveToCommit 

특정 커밋시점으로 이동하는방법!! 지금 리펙토링중인데.. 하다보니 사이드이펙트가 났는데, 어떤 시점에서 사이드 이펙트가 나기시작했는지 확인할 때 사용하기 적절하다.

#### 사용 예시

예시 1. 지금 있는 현재브랜치에서 커밋 시점을 뒤로 가고 싶을 때, 뒤에 숫자만 바꿔주면 된다.

```
//하나 뒤의 커밋으로 이동하기
git checkout HEAD~1

```


예시 2. 특정 커밋 위치로 이동하기, 뒤에 해당 커밋의 앞에 6자리만 적어주면 된다.

```
git checkout 8553f2
```

위의 2가지 방법으로 이동 후에 branch를 확인하면 아래와 같이 나오는데.

```
* (HEAD detached at 4e0e095)
  master
  develop
...

```

현재위치가 임시로 해더를 움직여둔 상태로 보면 된다. 그래서 다시 원래 있던 브랜치로 돌아가고 싶으면 checkout을 통해 해당 브랜치로 돌아가면된다.