# 图南画桥命名与节点规格

## 项目名

- 正式名称：`图南画桥`
- 所属品牌：`图南绘画工作室`
- ComfyUI 节点分类：`图南画桥`
- 工具节点分类：`图南画桥/工具`

## 五个正式节点

- `图南PS桥接器`
- `图南PS发送器`
- `图南选区还原`
- `图南智能缩放`
- `图南蒙版微调`

## 内部节点 ID

- `TuNanPSBridge`
- `TuNanPSSender`
- `TuNanSelectionRestore`
- `TuNanSmartResize`
- `TuNanMaskRefine`

## 当前架构

- Python 入口文件是 [__init__.py](/I:/BaiduSyncdisk/uxp-comfyui-bridge-project/comfyui-nodes/__init__.py)
- 主节点定义在 [tunan_bridge_nodes.py](/I:/BaiduSyncdisk/uxp-comfyui-bridge-project/comfyui-nodes/tunan_bridge_nodes.py)
- 工具节点定义在 [tunan_tool_nodes.py](/I:/BaiduSyncdisk/uxp-comfyui-bridge-project/comfyui-nodes/tunan_tool_nodes.py)
- 运行时状态和桥接服务在 [tunan_runtime.py](/I:/BaiduSyncdisk/uxp-comfyui-bridge-project/comfyui-nodes/tunan_runtime.py)
- 当前 ComfyUI 前端入口在 [tunan-frontend.js](/I:/BaiduSyncdisk/uxp-comfyui-bridge-project/comfyui-nodes/web/tunan-frontend.js)

## 当前策略

- 已经切换到新的 `图南画桥` 命名体系，不再保留旧 `Tunan*` 节点名兼容层
- ComfyUI 只从 `web` 目录加载前端扩展，旧 `js` 目录不再作为运行入口
- 旧前端已经归档到 [archive/legacy_frontend_20260315](/I:/BaiduSyncdisk/uxp-comfyui-bridge-project/comfyui-nodes/archive/legacy_frontend_20260315)，仅供参考，不应作为新的前端重构基础
- 允许直接重写 [tunan-frontend.js](/I:/BaiduSyncdisk/uxp-comfyui-bridge-project/comfyui-nodes/web/tunan-frontend.js)，也允许在 `web` 目录内拆分文件

