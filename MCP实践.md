在cursor中安装MCP，必须在cmd安装一遍，然后才可以（也不是说必须，如果都不行了，这是最后手段）

---

npm install -g @modelcontextprotocol/server-github

---

目前我安装的MCP有3个:

{
  "mcpServers": {
      "playwright": {
          "command": "npx",
          "args": [
              "@playwright/mcp@latest"
          ]
      },
      "amap-maps": {
          "command": "npx",
          "args": [
              "-y",
              "@amap/amap-maps-mcp-server"
          ],
          "env": {
              "AMAP_MAPS_API_KEY": "<YOUR_AMAP_API_KEY>"
          }
      },
      "github": {
        "command": "npx",
        "args": [
          "-y",
          "@modelcontextprotocol/server-github"
        ],
        "env": {
          "GITHUB_PERSONAL_ACCESS_TOKEN": "<YOUR_GITHUB_TOKEN>"
        }
    }
  }
}


都已经可以正常操作了! 非常Nice

1. 第一个AI使用浏览器访问页面,需要先安装playwright的chrome才可以运行
2. 第二个是高德地图的API信息,可以让AI查看附近的信息
地理编码和逆地理编码
路径规划（驾车、步行、骑行、公交）
天气查询
IP定位
POI（兴趣点）搜索
距离测量
3. 第三个是Github,可以上传或者下载项目,让AI搜索最新的项目