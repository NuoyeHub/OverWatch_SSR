# OVERWATCH_SSR

杀敌升级ing  
作者：HUGH#52711  
未完成，欢迎提供意见~  
这里是个测试房，可能随时重开。  
欢迎有兴趣的老哥加我  

## 开发日志
	8月5日
	今天完全开发完抽卡升级部分。天赋部分遇到问题，等待解决，今天不想弄了hhhhhh  
	终于完成天赋文本显示了，我陷入之前60天赋老哥的思想中了，简直了，想通了简直不要太简单！！！！吐了。累死了我了。然后现在开发地图小文本。类似玻璃大炮被自己杀了，就要显示信息提示。  
	8月6日  
	今天完成了很多部分，但是中间经历了一次丢代码的情况，简直了。体验到这种痛苦，尿了。  



## issues
---
	bug  
	1. 美队的盾无效，等待修复

## 元素对应表
---
### SX	属性
   	0	步进生命值（用于调整满级生命值）  
	1	等级  
	2	最大生命值  
	3	攻击  
	4	移动速度  
	5	受到治疗  
	6	造成治疗  
	7	防御  
	8	升级等级（每次击杀最终升级的等级）  
	9	击杀生命  
	10	击杀攻击  
	11	击杀速度  
	12	击杀受到治疗  
	13	击杀造成治疗  
	14	击杀防御  
	15	敌方等级（调用敌方等级，用于击杀升级）  
	16	等级临时存放（用于调整自身等级所获得的击杀升级）  
	17	生命池ID存放  

---

### ZT	状态	
	0	持续伤害（现在空的）
	1	满级提示光柱


---	
### HUDWB		玩家HUD和地图文本
	0	地图文本
	1	玩家文本
	2	满级HUD
	3	不朽之心冷却文本
	4	44号药剂死亡倒数文本
	5	电子羊倒数
	

---
### TF		天赋
	0	天赋1
	1	天赋2

---
### TF_DY	天赋文本调用
	0	天赋文本调用1
	1	天赋文本调用2
	2	不朽之心启动变量
	3	不朽之心属性刷新变量
	4	不朽之心倒计时终止变量

### TIME	倒数时间
	0	不朽之心倒数
	1	44号药剂倒数
	2	电子羊倒数
	

---
### 独立元素
	DD			电刀调用
	TF_Max		天赋最大抽奖值（天赋的随机选项1-tf_max）

---
### 子程序对照表
	SX_CSH		属性初始化
	SX_SX		属性刷新
	WB			头顶文本
	HUD			玩家hud
	SX_HUD		属性hud
	TF			天赋初始化
	SM_BD		生命值变动
	TF_XGDY		天赋效果调用
	
---
### TF_WB	天赋玩家文本 “*”代表规则中是空的，可以删除。  
	0		空
	1		玻璃大炮——攻击力提高500%，攻击有25%可能秒杀自己。
			pong！awsl
	2		斯塔缇克电刃——攻击是会连锁伤害周围的敌方。
			兹~爽！
	3	*	非酋：没有任何属性。
			老倒霉蛋了
	4	*	败血症：伤口无法凝结，受到伤害后会持续掉血。
			啊啊啊啊，创可贴！！！
	5		不朽之心：死亡后会复活，cd60。
			这心怎么看起来干巴巴的？
	6	*	扁酒壶：攻击力提高100%，防御力降低50%。
			对于某些人来说，这就是生活意义。
	7	*	超级标志：全属性提高30%。
			我 就 是 超 人 ！
	8		纵火狂：攻击赋带燃烧效果。
			fffffffff
	9		44号药剂：按蹲+互动，不死效果30秒，结束立即死亡。
			这也太难喝了！
	10		变异橘子：血量调高100%，败血症失效。
			嗯，我可不像得败血症。
	11		彩票：获得777颗弹药！
			你感到如此的幸运...和孤独。
	12		单片眼镜：攻击沉默敌人
			空气中的阿蒙成分增多了...
	13		电子羊：可以额外进行一次跳跃cd4
			仿生人也会做梦吗？
	14		伽马射线：子弹穿透墙面
			没有什么可以阻挡你了！
