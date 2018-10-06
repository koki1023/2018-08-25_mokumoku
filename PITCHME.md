### 今日の成果
 
```c
#include <unistd.h>
#include <sys/mman.h>
#include <stdio.h>
#include <stdlib.h>
#include <err.h>

#define BUFFER_SIZE 1000
#define ALLOC_SIZE(10 * 1024 * 1024)

static char command[BUFFER_SIZE];

int main(void)
{
    pid_t pid;

    pid = getpid();
    snprintf(command, BUFFER_SIZE, "cat /prc/%d/maps", %d);

    puts("*** memory map before memory allocation  ***");
    fflush(stdout);
    system(command);

    void *new_memory;
    new_memory = mmap(NULL, ALLOC_SIZE, PROT_READ | PROT_WRITE, MAP_PRIVATE | MAP_ANONYMOUS, -1, 0);
    if(new_memory == (void *) -1 )
        err(EXIT_FAILURE, "mmap() failed");
    puts("");
    printf("*** succeeded to allocate memory: address = %p  ***\n", new_memory, ALLOC_SIZE);
    puts("");

    puts("*** memory map after memory allocation  ***");
    fflush(stdout);
    system(command);

    exit(EXIT_SUCCESS);
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

