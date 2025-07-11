好的！现在我们以 `branch_2.1` 和 `branch_2.2` 为例，假设你想将 `branch_2.1` 的提交 **rebase** 到 `branch_2.2` 上。

### **目标：**

* 你有两个分支 `branch_2.1` 和 `branch_2.2`。
* 你希望将 `branch_2.1` 上的提交应用到 `branch_2.2` 上。

### **步骤 1：确保你处于正确的分支**

首先，切换到 `branch_2.2`，这是你想要将 `branch_2.1` 的提交 **rebase** 到的分支。

```bash
git checkout branch_2.2
```



### **步骤 2：执行 `rebase` 操作**

在 `branch_2.2` 上执行 `rebase` 操作，将 `branch_2.1` 的提交应用到当前分支：

```bash
git rebase branch_2.1
```

这个命令会将 `branch_2.1` 上的所有提交应用到 `branch_2.2` 上，保持历史记录的线性结构。

### **步骤 3：处理冲突（如果有）**

如果在 `rebase` 操作过程中出现冲突，Git 会停止并提示你解决冲突。

1. **查看冲突文件**：

   使用 `git status` 查看哪些文件有冲突：

   ```bash
   git status
   ```

   这会列出冲突的文件。

2. **解决冲突**：

   打开冲突文件，手动解决冲突，并删除冲突标记（`<<<<<<<`, `=======`, `>>>>>>>`）。

3. **添加解决冲突后的文件**：

   解决冲突后，使用 `git add` 将已解决的文件标记为已解决：

   ```bash
   git add <conflicted-file>
   ```

4. **继续 `rebase` 操作**：

   使用以下命令继续 `rebase` 操作：

   ```bash
   git rebase --continue
   ```

   Git 会继续将剩余的提交应用到 `branch_2.2` 上。


