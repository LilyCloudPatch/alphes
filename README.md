# alphes：LilyPatch 立绘源仓

本仓维护经审核的游戏内立绘 PNG 与逐项锁，不是 plugins 集成发布仓。
艺术由 Dairi 创作，上游打包维护者 DTM9025；不得将素材署名为 LilyPatch 创作。
既有 TH14 内容保持。2026-10-15 用户确认 TH15 功能正常及 Steam 首次中文
分辨率框通过；正式候选完成签名、资源 guard 与自动回归后发布。

TH15 从 DTM9025/DTM commit `6d2e44fb6d6bfd9dcced2b5f8ab9b358e6547530`
的 alphes/th15 导入。100 张 PNG 绑定 th15_100b 原像素哈希、长度、尺寸与位置；
Extra 复用第三/六关的 12 个纹理槽，共 112 次原上传。身体右下锚定裁切，表情
沿同一身体裁切偏移配准；cut-in 和选人图等比适配、居中。原全不透明槽进行 alpha
合成，其他槽整体覆盖；PNG 半透明边缘保留，不发布上游 ANM 或 MSG 脚本。

`face/enemy6/face06bs2.png` 与 `face/enemy6/face06lo.png` 在原版没有同名纹理，
登记为排除项。上游另行修改 ANM/MSG 来实现的额外姿态不属于当前像素替换能力。
TH15 锁为 th15/alphes-lock.json；正常构建只读取本仓，不直接读取 DTM 镜像。
导入/签名组装入口在 LilyPatch/content/tools/alphes_images.py，DB 与测试证据只在
LilyPatch/build/th15/alphes-review；私钥不进入本仓。

素材使用依据沿用项目所有者提供并审核的 Dairi 素材利用規約，原文归档于
LilyPatch/content/upstream-sync/dairi-usage-terms.ja.txt。该依据用于已审核的游戏内
立绘替换包，不授权将素材单独作为自由素材集再分发。发布须保留 Dairi / DTM9025
署名；TH14 与 TH15 分别实测，发布物不得包括游戏原始档案或上游可执行代码。
