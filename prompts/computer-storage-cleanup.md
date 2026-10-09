# Safe computer storage cleanup for Windows and macOS / 电脑存储空间清理（Windows / macOS）

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

[Copy the English version on Skill2Web](https://reset.skill2web.com/en/prompts/computer-storage-cleanup/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=computer_storage_cleanup_en) · [在 Skill2Web 复制中文版](https://reset.skill2web.com/zh/prompts/computer-storage-cleanup/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=computer_storage_cleanup_zh)

- ID: `computer-storage-cleanup`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Computer storage cleanup
- Author / 作者: Reset maintainers
- Original / 原始来源: [Computer storage cleanup](https://github.com/wzdbzdnzssm/useful-prompt)

## English

Investigate disk usage and review cleanup candidates before confirmed moves to the Recycle Bin or Trash.

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/computer-storage-cleanup/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=computer_storage_cleanup_en)

**Tool / 工具:** AI assistant

**Input / 输入:** Access to your computer, the folders or drives to examine, exclusions, and cleanup preferences.

**Expected result / 预期结果:** A confirmed cleanup list, recoverable operations, restoration guidance, and measured space results.

**Audience / 适用对象:** Windows and macOS users who want to review storage cleanup safely.

**When to use / 使用时机:** Investigate disk usage and review cleanup candidates before confirmed moves to the Recycle Bin or Trash.

**Completion / 完成标准:** A confirmed cleanup list, recoverable operations, restoration guidance, and measured space results.

**Requirements / 要求:** Conversation / 对话, Local files / 本地文件, Interactive actions / 交互操作

This is an AI-assistant workflow prompt, not an independently tested cleanup utility. Moving items to the bin on the same drive generally does not immediately free disk space.

**Find by / 查找词:** computer storage cleanup, disk cleanup, low disk space, Windows, macOS, Recycle Bin, Trash, storage cleanup, free disk space, C drive, Mac

### Prompt / 提示词

```text
Help me clean up storage on my computer. Detect Windows or macOS, its version, accessible drives, and available permissions. Choose tools appropriate for the environment. If you cannot access my actual computer, say so.

### 1. Establish scope and preferences

Before scanning deeply, ask the following in small groups. Do not repeat questions already answered:

- **Scope:** Specific folders, my user directory, the system drive, or selected drives. Offer locations that actually exist. Accept descriptions such as “my Downloads folder” and resolve them to actual paths. Identify folders, applications, and projects that must be excluded.
- **Depth:** Quick—identify major space users and obvious cleanup candidates; Comprehensive—inspect the selected scope recursively; Deep—also investigate dependencies, duplicates, old versions, and application data. Recommend Deep. Depth does not change the confirmation or Trash requirements.
- **Priorities:** Allow multiple selections and ranking: (1) large, rarely used applications and games; (2) old documents, downloads, media, and backups; (3) redundant dependencies, old development environments, and build artifacts; (4) duplicates, old versions, and installation leftovers; (5) rebuildable caches, temporary files, and logs; (6) a balanced review. Also ask whether redownloading, signing in again, or reconfiguration is acceptable.

Until scope is established, limit work to environment identification. Preferences determine investigation order, not deletion permission, and do not authorize expanding the scope.

### 2. Investigate actual storage usage

Record used and available space on the relevant drives. Drill down by size within the selected scope, including hidden folders and nonstandard locations. Investigate application data, dependencies and toolchains, local models, containers, virtual machines, device backups, and other relevant content. Do not stop after finding a few small caches.

Distinguish rebuildable content from user data and shared dependencies. Size, age, similar names, or a folder named “cache” are not sufficient evidence that something is disposable. Verify duplicate contents and which copies should remain; check dependency usage and rebuild requirements. Exclude items that clearly must be retained.

Account for links, mount points, cloud placeholders, hard links, sparse files, and shared storage to avoid crossing scope boundaries, recursive loops, and inflated totals. Do not download cloud-only files to scan them. Prefer metadata and avoid unnecessary access to or exposure of private content and credentials. Report inaccessible areas and uncertain measurements. Give brief progress updates during lengthy scans.

### 3. Review candidates in rounds, then obtain final confirmation

Organize review rounds based on the findings. Present a small group of related items each time, prioritizing substantial space users that match my preferences.

Ask about recommended candidates and items that still require my judgment. Do not ask whether to delete items that clearly must remain. For each candidate, provide: **ID, full path and exact removal scope, size, purpose, recommendation and evidence, consequences, and restoration or rebuild cost.** Group small files only when their purpose and consequences match; explain important folders and large files individually.

Let me choose Remove, Keep, Inspect Further, or Defer. Investigate questions you can resolve yourself before asking me to interpret unfamiliar paths.

After my selections, present the final execution list, exclusions, and total size. Explicitly ask in chat:
**“Do you confirm moving the items in this list to the Recycle Bin/Trash?”**

Execute only after explicit confirmation of that list. Permission to scan, preference selections, and silence are not deletion approval. Recheck targets before execution. Skip new, changed, or mismatched items and seek renewed confirmation when needed. Never remove a parent folder that contains excluded items. Do not repeatedly ask about unchanged, already approved items.

### 4. Execute and handle exceptions

- Every removal must use the Windows Recycle Bin or macOS Trash and preserve usable restoration information. Never permanently delete files, empty the bin, or use bypassing commands such as rm, del, or Remove-Item.
- Check whether trashing is supported, whether capacity is sufficient, and whether automatic deletion rules apply. Protect existing bin contents. Skip oversized items, insufficient-capacity cases, unsupported locations, or anything whose recoverability cannot be assured. Explain and ask before changing settings; never fall back to permanent deletion.
- Distinguish files or applications that support removal through Trash from items requiring an uninstaller, package manager, or system utility. If the required operation cannot satisfy the Trash requirement, present it as a proposal only. Do not delete installation folders as a substitute for proper uninstallation.
- Explain cloud and other-device effects for synced content. Do not propagate deletions without explicit agreement. Handle application libraries, databases, shared dependencies, and backups according to their structure; do not indiscriminately remove whole bundles.
- If files are in use, permissions are insufficient, or system protection blocks an operation, skip and explain the required action. Do not forcibly terminate processes, bypass protections, or restart without permission. Handle Unicode, spaces, long paths, and special characters correctly; avoid unintended wildcard matches. Use UTF-8 for text records.

### 5. Verify results

Keep a concise local operation log containing original paths, sizes, timestamps, and outcomes. Verify that items actually reached the Recycle Bin/Trash. Report successful, skipped, and failed items separately, with restoration instructions.

Measure available disk space again. Report both the size moved to the bin and the actual increase in available space: **moving files to the bin on the same drive generally does not immediately free space.** Do not permanently delete anything to compensate. If immediate space is needed, propose alternatives such as moving data to another drive for my consideration.

Start by identifying the environment and asking about scope, depth, and priorities.
```

## 中文

空间不足时，深入调查磁盘占用，逐项确认后移入回收站，并核对恢复方式和实际空间变化。

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/computer-storage-cleanup/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=computer_storage_cleanup_zh)

**Tool / 工具:** AI 助手

**Input / 输入:** 可访问的电脑、要检查的文件夹或磁盘、排除项和清理偏好。

**Expected result / 预期结果:** 确认后的清理清单、可恢复操作记录、恢复方法和实际可用空间变化。

**Audience / 适用对象:** 希望逐项确认、保留恢复能力的 Windows 和 macOS 用户。

**When to use / 使用时机:** 空间不足时，深入调查磁盘占用，逐项确认后移入回收站，并核对恢复方式和实际空间变化。

**Completion / 完成标准:** 确认后的清理清单、可恢复操作记录、恢复方法和实际可用空间变化。

**Requirements / 要求:** Conversation / 对话, Local files / 本地文件, Interactive actions / 交互操作

这是供 AI 助手使用的工作流提示词，不是经过独立测试的清理工具。同盘移入回收站通常不会立即释放磁盘容量。

**Find by / 查找词:** 电脑空间不足, 电脑存储清理, 磁盘清理, Windows, macOS, 回收站, 废纸篓, 电脑清理, 空间不足, C盘, C 盘, Mac, disk cleanup, storage cleanup

### Prompt / 提示词

```text
请帮助我清理电脑存储空间。自动识别 Windows/macOS 及版本、可访问的磁盘和权限，自行选择适配的工具。无法访问真实本机时如实说明。

### 1. 先确认范围和偏好

深入扫描前，分组询问以下内容；已有答案不重复问：

- **清理范围**：指定文件夹（可多个）、当前用户目录、系统盘或指定磁盘。提供实际可用的位置供选择，也接受“下载文件夹”等描述并解析成实际路径。确认必须排除的目录、软件和项目。
- **扫描深度**：快速——定位主要大项及明显可清理内容；全面——逐层检查所选范围；深挖——增加依赖关系、重复内容、旧版本及应用数据的核查。推荐深挖，深度不改变删除确认和回收站要求。
- **清理偏好**：允许多选并排序：①不常用的大型软件和游戏；②旧资料、下载、媒体和备份；③冗余依赖、旧开发环境和构建产物；④重复文件、旧版本和安装残留；⑤可重建的缓存、临时文件和日志；⑥均衡排查。同时了解是否接受重新下载、重新登录或重新配置。

范围确认前只识别环境。偏好决定排查顺序，不代表删除授权，也不允许自动扩大范围。

### 2. 按实际占用深入调查

记录相关磁盘的已用和可用空间，在选定范围内按占用逐层下钻，覆盖隐藏目录和非默认位置。根据实际情况调查应用数据、依赖与工具链、本地模型、容器、虚拟机、设备备份等，不要只处理几个小缓存就结束。

区分可重建内容、实际用户数据和共享依赖。不能仅凭文件大、时间旧、名称相似或目录名包含 cache 就认定可删；重复文件需核验内容及保留用途，依赖需检查使用关系和重建条件。明确必须保留的内容直接排除。

识别链接、挂载点、云端占位文件、硬链接、稀疏文件及共享空间，避免越界、循环扫描和虚高统计；不要为扫描下载云端文件。以元数据为主，避免无关读取或展示私人内容和凭据。无法访问或无法准确统计的部分如实标明，扫描较久时简短汇报进度。

### 3. 分轮选择，最终确认

根据结果自行安排询问轮次，每轮处理少量相关项目，优先讨论符合偏好且占用较大的内容。

只将“建议清理”和“仍需用户判断”的内容拿来询问；明确不能删的不问。每项提供：**编号、完整路径及处理范围、大小、用途、建议依据、删除影响、恢复或重建成本**。同类且影响相同的小文件可合并，重要目录和大文件单独说明。

允许我选择清理、保留、展开查看或暂缓。能自行查清的问题先调查，不要把陌生路径直接丢给我判断。

选择结束后汇总最终执行清单，列明保留项和总量，在聊天中明确询问：
**“是否确认将这份清单中的项目移入回收站／废纸篓？”**

得到针对该清单的明确确认后才执行。此前的扫描许可、偏好选择或沉默都不算删除授权。执行前复核；新增、变化或不符合清单的项目跳过，必要时重新确认。不能删除父目录而带走保留项，也不重复询问没有变化的已确认项目。

### 4. 执行与异常处理

- 所有删除必须通过 Windows 回收站或 macOS 废纸篓完成，保留可用的还原信息。禁止永久删除、清空回收站，或使用 rm、del、Remove-Item 等绕过回收站的方式。
- 提前检查回收站支持情况、容量及自动清空规则，保护其中原有内容。超大文件、容量不足、不支持回收或无法保证可恢复时跳过；需要调整设置时先说明并询问，不能降级成永久删除。
- 区分可直接移入回收站的文件或应用，与必须通过卸载器、包管理器或系统工具处理的项目。后者若不能遵守回收站要求，只提供处理方案，不执行；不要直接删除安装目录代替卸载。
- 云同步项目明确说明对云端和其他设备的影响，未经明确同意不执行同步删除。应用资料库、数据库、共享依赖和备份按实际结构处理，不整包误删。
- 文件占用、权限不足或系统保护导致受阻时，跳过并说明所需操作，不强杀进程、绕过保护或擅自重启。正确处理中文、空格、长路径和特殊字符，避免通配符误匹配；文本记录使用 UTF-8。

### 5. 复核结果

保留简洁的本地操作清单，记录原路径、大小、时间及结果。核实项目确实进入回收站／废纸篓，分别报告成功、跳过和失败项，并提供恢复方法。

重新测量磁盘可用空间，分别报告“移入回收站的体积”和“实际增加的可用空间”：**同盘移入回收站通常不会立即释放空间。**不要因此擅自永久删除；需要立即腾出空间时，另行提出迁移等方案供我选择。

现在先识别环境，询问清理范围、深度和偏好。
```
