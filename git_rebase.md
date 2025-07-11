好的！现在我们以 `branch_2.1` 和 `branch_2.2` 为例，假设你想将 `branch_2.1` 的提交 **rebase** 到 `branch_2.2` 上。

### **目标：**

* 你有两个分支 `branch_2.1` 和 `branch_2.2`。
* 你希望将 `branch_2.1` 上的提交应用到 `branch_2.2` 上。

### **步骤 1：确保你处于正确的分支**

首先，切换到 `branch_2.2`，这是你想要将 `branch_2.1` 的提交 **rebase** 到的分支。

```bash
git checkout branch_2.2
```

