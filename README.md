# 搬家出物清单

一个放在 GitHub Pages 上的出物页面。买家看清单和照片，你在网页上直接编辑，点“发布更新”后自动提交到这个仓库。

## 文件

- `index.html`：页面
- `style.css`：样式
- `data.json`：所有物品和页面信息（网页编辑时会自动改它，一般不用手动碰）
- `photos/`：上传的照片，每张有原图 `xxx.jpg` 和列表用的小图 `xxx_t.jpg`
- `.nojekyll`：让 GitHub Pages 直接发布文件，不经过 Jekyll

## 第一次部署（约 5 分钟）

1. 在 GitHub 新建一个 **Public** 仓库，比如叫 `moving-sale`。
2. 把这个文件夹里的所有文件（包括 `.nojekyll` 和 `photos/`）上传到仓库根目录。
   网页上可以用 “Add file → Upload files” 拖进去，或者用 git push。
3. 仓库 Settings → Pages → Source 选 **Deploy from a branch**，分支选 `main`，目录选 `/ (root)`，保存。
4. 等 1 分钟左右，页面地址是 `https://<你的用户名>.github.io/moving-sale/`。

## 在网页上编辑

1. 打开页面，点最底下的“管理”（或者在地址后面加 `#admin`）。
2. 第一次会让你填 token：
   - 打开 https://github.com/settings/personal-access-tokens/new
   - Repository access 选 **Only select repositories**，只勾这个仓库
   - Repository permissions 里把 **Contents** 设为 **Read and write**，其他不动
   - 有效期可以设到搬家结束之后
3. 进入管理模式后可以添加 / 编辑 / 删除物品、上传照片、改状态、改页面信息。
4. 改完点右下角“发布更新”。所有修改和新照片会合成**一次提交**推到仓库，大约 1 分钟后所有人都能看到。
5. 买家打开的页面每分钟会自动刷新一次状态，不用手动刷新。

Token 只保存在你当前这台设备的浏览器里，不会进仓库。手机和电脑各自连接一次即可。
不用了可以在“页面信息 → 在这台设备上退出管理”删除，或者直接去 GitHub 撤销这个 token。

## 小提示

- 删掉的照片也会在下次发布时从仓库里删除。
- 如果手机和电脑同时改，后发布的那台会提示冲突，可以选择覆盖或载入最新。
- 页面截图和照片都是公开的，联系方式也一样，不要放不想公开的信息。
- iPhone 照片如果是 HEIC 格式读不出来，在相机设置里改成“兼容性最佳”，或者先转 JPG。
