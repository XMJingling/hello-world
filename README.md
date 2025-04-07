flowchart TD
    A[开始dfs(step)] --> B{step == 10?}
    B -- 是 --> C[检查等式ABC+DEF=GHI]
    C -- 成立 --> D[total++, 打印解]
    C -- 不成立 --> E[返回]
    B -- 否 --> F[循环i从1到9]
    F --> G{book[i]==0?}
    G -- 否 --> F
    G -- 是 --> H["a[step]=i\nbook[i]=1"]
    H --> I["递归dfs(step+1)"]
    I --> J["回溯：book[i]=0"]
    J --> F
    F -- 循环结束 --> E
    E --> K[返回上一层]
