### 今日の成果
 
```c
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>
#include <err.h>

static void child()
{
  printf("i'm child! my pid is %d!\n", getpid());
  exit(EXIT_SUCCESS);
}

static void parent(pid_t pid_c)
{
  printf("I'm parent, my pid is %d and the pid of my child is %d\n", getpid(), pid_c);
}

int main()
{
  pid_t ret;
  ret = fork();
  if (ret == -1)
    err(EXIT_FAILURE, "fork() failed");
  if (ret == 0) {
    child();
  } else {
    parent(ret);
  }

  err(EXIT_FAILURE, "should't reach heare");
}

```

---

### 結局makefileって？

（この数時間での理解なので違っているかも）

- `ソースコード=>実行ファイル` の流れの設計図みたいな？
  - 依存関係とかをおさえてある
  - 毎回毎回再コンパイル、再リンクする手間を省いてくれる

---

### 今後の目標

- ひとまずきっちり読み切る
- 遅延評価の恩恵をあまり実感できていないのでもう少し調べたい

---

