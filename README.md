# 🚀 ImmortalWrt 软路由固件

基于 ImmortalWrt 编译的 x86_64 软路由固件

## 📦 包含插件

| 插件 | 说明 |
|------|------|
| FRP 客户端 | 内网穿透工具 |
| 网络加速 | BBR/tproxy 加速 |
| OpenClash | 去广告/代理管理 |
| LuCI | Web 管理界面 |
| Samba4 | 文件共享 |
| UPnP | 自动端口转发 |
| NAS 支持 | EXT4/NTFS/vfat 文件系统 |

## 📥 下载

### 方式 1：Release 页面（推荐）

访问 [Releases](https://github.com/20721/openwrt-firmware/releases) 下载最新固件

### 方式 2：手动触发编译

1. 进入 [Actions](https://github.com/20721/openwrt-firmware/actions)
2. 点击 "Build ImmortalWrt"
3. 点击 "Run workflow"
4. 等待编译完成（约 2-3 小时）
5. 在 Artifacts 或 Release 下载

## 🔧 自定义配置

### 修改插件

编辑 `.config` 文件，添加或删除：
```
CONFIG_PACKAGE_插件名=y    # 启用
# CONFIG_PACKAGE_插件名 is not set    # 禁用
```

### 添加新插件

1. 在 `feeds.conf` 添加插件源
2. 在 `.config` 启用插件
3. 提交并推送
4. 触发编译

## 📁 文件说明

| 文件 | 说明 |
|------|------|
| .config | 固件配置 |
| feeds.conf | 插件源配置 |
| .github/workflows/build.yml | 编译工作流 |

## 🔄 发布新版本

```bash
git tag v1.0.0
git push origin v1.0.0
```

## ⚠️ 注意事项

- 编译耗时约 2-3 小时
- GitHub Actions 每月免费额度 2000 分钟
- 建议使用本地编译测试配置后再云编译

## 📄 许可证

GPL-2.0

## 👤 作者

瓶子 <pzxsky@gmail.com>
