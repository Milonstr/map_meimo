# map_meimo

《丧尸末日》角色卡的真实地图数据，由 `tools/citydata.py` 生成，角色卡通过 jsDelivr 读取：

`https://cdn.jsdelivr.net/gh/Milonstr/map_meimo@main/data/`

## 结构

- `data/index.json`：已有城市列表
- `data/<城市>/index.json`：该城市的区与小区名索引 `[名称, 区, 纬度, 经度, 楼栋数]`
- `data/<城市>/<区>.json`：
  - `p`：地点 `[名称, 类型, 纬度, 经度, 地址]`
  - `c`：小区 `{n, la, lo, a, g:边界, b:[[层数, 楼名, 轮廓]]}`，轮廓为相对小区中心的 1e-5 度整数

坐标均为 WGS84。

## 数据来源与许可

- 地图数据 © OpenStreetMap contributors，按 [ODbL](https://opendatacommons.org/licenses/odbl/) 提供
- 部分地点来自高德开放平台（使用时需遵守其服务条款）
