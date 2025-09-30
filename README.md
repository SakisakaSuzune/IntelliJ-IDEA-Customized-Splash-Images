This repository contains splash images I created for IntelliJ IDEA, usually in a theme of games characters. Also, an image-changing shortcut for macOS will be updated here.      
这个仓库有我为IntelliJ IDEA创建的个性化启动图案，它们通常以游戏角色为主题。这里还有我为macOS设计的快捷切换方式。
  
---------------------------------  
#### For macOS, the easiest way to change the image is using my shortcut.
#### 对于 macOS，使用我的快捷方式是更改启动图案的最简单方法。
  
---------------------------------  
#### For Windows, you can follow these steps to change the splash image:
###### I. Check the environment variables. If you clearly know that JAVA_HOME is set, please skip this part.
1. Click Start, Control Panel, System, and then Advanced system settings.
2. In the System Properties dialog box, on the Advanced tab, click Environment Variables.
3. Add the JAVA_HOME environment variable:
    4. In the System Variables section, click New.
    5. In the Variable name field, enter JAVA_HOME.
    6. In the **Variable value** field, enter the location where the JDK software is installed (for example, `C:\Program Files\Java\`_<java_version>_)
    7. Click **OK**.
8. Update the PATH environment variable to include the location of the Java executable files:
    9. In the **System Variables** section, select the PATH variable, and click **Edit**.
    10. In the **Variable value** field, insert `%JAVA_HOME%\bin;` in front of all the existing directories. Do not delete any existing entries; otherwise, some existing applications may not run.
    11. Click **OK**.
12. Exit the Control Panel.
###### II. Prepare materials for the changing.
1. Download the image(PNG, bigger than 1280•800px) for changing to a new folder.
2. Copy `C:\Users\xxx\AppData\Local\JetBrains\IntelliJIdea****.**\lib\app.jar` to the created folder.
3. Rename the image to `idea_community_logo@2x.png`(for Community Edition). I currently don't know what name should Ultimate Edition use.
4. Resize `idea_community_logo@2x.png` for 50% of origin, named `idea_community_logo.png`
###### III. Let's use the Terminal.
1. Make sure you have quit the IDEA.
2. In your new created folder, right-click the blank place and then "Open in Terminal".
3. In the terminal, enter following commands:
    1. `jar -uvf app.jar idea_community_logo.png`
    2. `jar -uvf app.jar idea_community_logo@2x.png`
4. After you received `adding: idea_community_logo.png(in = 1451166) (out= 1450875)(deflated 0%)` and `adding: idea_community_logo@2x.png(in = 5464859) (out= 5465860)(deflated 0%)`, close the window.
###### IV. Replace it......sneakily!
1. Copy `app.jar`.
2. Go to `C:\Users\xxx\AppData\Local\JetBrains\IntelliJIdea****.**\lib\`, paste `app.jar` and choose "replace".
###### V. Flush the cache, so the new image can take effect immediately.
1. Go to `C:\Users\xxx\AppData\Local\JetBrains\IntelliJIdea****.**\caches\`
2. Delete the `splash` folder.

Now, try to reopen the IDEA and check the splash image!  
Remember you can always change the size of the image if it doesn't provide a satisfied view.

#### 对于Windows用户，你可以通过下面的步骤替换IDEA的启动画面：
###### I. 检查环境变量。如果您清楚地知道 JAVA_HOME 已设置，可以跳过此部分。
1. 依次单击“开始”、“控制面板”、“系统”和“高级系统设置”。
2. 在“系统属性”对话框的“高级”选项卡上，单击“环境变量”。
3. 添加 JAVA_HOME 环境变量：
    4. 在“系统变量”部分中，单击“新建”。
    5. 在“变量名称”字段中，输入 JAVA_HOME。
    6. 在“变量值”字段中，输入 JDK 软件的安装位置（例如，`C:\Program Files\Java\`_<java_version>_）
    7. 单击“确定”。
8. 更新 PATH 环境变量以包含 Java 可执行文件的位置：
    9. 在“系统变量”部分中，选择 PATH 变量，然后单击“编辑”。
    10. 在“变量值”字段中，在所有现有目录前面插入“%JAVA_HOME%\bin;”。请勿删除任何现有条目，否则某些现有应用程序可能无法运行。
    11. 点击“确定”。
12. 退出控制面板。
###### II. 准备更改所需的材料。
1. 下载要更改的图片（PNG 格式，尺寸大于 1280•800 像素）到新文件夹。
2. 将`C:\Users\xxx\AppData\Local\JetBrains\IntelliJIdea****.**\lib\app.jar`复制到创建的文件夹中。
3. 将图片重命名为`idea_community_logo@2x.png`（适用于社区版）。我目前不知道旗舰版应该使用什么名称。
4. 将 `idea_community_logo@2x.png` 的大小调整为原始大小的 50%，命名为 `idea_community_logo.png`。
###### III. 使用终端。
1. 确保您已退出 IDEA。
2. 在新建的文件夹中，右键单击空白处，然后选择“在终端中打开”。
3. 在终端中输入以下命令：
4. `jar -uvf app.jar idea_community_logo.png`
5. `jar -uvf app.jar idea_community_logo@2x.png`
6. 收到 `adding: idea_community_logo.png(in = ***) (out= ***)(deflated 0%)` 和 `adding: idea_community_logo@2x.png(in = ***) (out= ***)(de​​flated 0%)` 后，关闭窗口。
###### IV. 悄悄地换掉它！
1. 复制 `app.jar`。
2. 前往 `C:\Users\xxx\AppData\Local\JetBrains\IntelliJIdea****.**\lib\`，粘贴 `app.jar` 并选择“替换”。
###### V. 刷新缓存，使新图片立即生效。
1. 前往 `C:\Users\xxx\AppData\Local\JetBrains\IntelliJIdea****.**\caches\`
2. 删除 `splash` 文件夹。

现在，尝试重新打开 IDEA 并检查启动画面！  
还请记得，如果图片大小不符合您的预期，可以随时更改图片大小。
