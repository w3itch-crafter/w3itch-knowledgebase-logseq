- 目前测试了两个位置
	- `/usr/share/minetest/games`
		- 不同用户执行`gametest --gameid list`都能找到放在这里的游戏
	- `$HOME/.minetest/games`
		- 不同用户执行`gametest --gameid list`，只有对应自己HOME下的游戏才会被列出来
- 关于gameid
	- 会按照 `games/<GAME>` 这个 GAME 目录名来得出其对应的gameid
		- 目前知道：
			- 如果是`xxx_game`这种以`_game`结尾的格式，那对应的gameid是`xxx`，比如默认的`minetest_game`，其gameid就是`minetest`
			- 如果是不以结尾的，gameid会和目录名相同