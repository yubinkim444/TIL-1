## Git Cherry-Pick

놀랍게도 깃으로 Cherry-Pick을 처음 써봤다. 뭔가 중간에 특정 커밋을 수정하는 건줄 알았는데 완전히 다른 기능이었다;

체리픽은 다른 브랜치에 있는 변경사항을 커밋단위로 현재 브랜치에 이관?하는 기능이다. 내가 경험했던 상황은 A브랜치에서 로컬에 커밋작업을 하다 리모트에서 이번 릴리즈 버전에 맞게 새로 브랜치를 땄다. 그래서 A브랜치에서 작업하고 있던 로컬 커밋들을 B로 이관해야할 일이 생겼는데 이때 사용하면 된다.

#### 사용 예시

A의 커밋을 B 브랜치로 옮기고 싶을 때 B브랜치에서 A브랜치의 커밋을 체리픽하면 된다.

```
//특정 커밋만 가져올 때
git cherry-pick master
```

```
//특정 커밋범위를 가져올 때
//커밋해쉬 hash1 이후의 커밋부터 hash2까지 가져온당

git cherry-pick [commitHash1]..[commitHash2]

git cherry-pick da7bf655c7b50098cd9b7c6c3c19af43124b736e..85d7bd0dac6f33a677405217fe5824b1bce38de8

```

자세한 사항은 [Git_Cherry_Pick](https://git-scm.com/docs/git-cherry-pick)문서를 읽어보도록 하자!