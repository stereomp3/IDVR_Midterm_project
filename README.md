# IDVR_Midterm_project

需要安裝的套件:

* Meta XR All-in-One SDK
* AI NavigationTextMeshPro
* Animation Rigging



如果安裝遇到問題，再密我看缺甚麼套件





主要的場景為 StartScene 和 Stage1

StartScene 可以調整設定，然後進入到 Stage1

ClimbTest 為測試用場景，可以不用理他



> 目前的 stage:

1. Level 1 Hill
2. Level 2 Taking Step
3. Level 3 Run and Jump
4. Level 4 Teleport
5. Level 5 Climbing (new): 爬梯子
6. Level 6 Climbing&Jump (new): 跑+跳+抓 
7. Level 7 beat enemy (new): 可以撿地上的石頭丟敵人，有三種大小的石頭



目前的 seat inplace

* 基本功能一樣
* 跑: 左腳全起或是右腳全起
* 跳: 雙腳全起



> EMS 刺激的地方:

* 上坡下坡: 相關設定在 Player&GameManager>GameManager，player_stay 2 代表現在在有波的地方，player_up_down 1 為往上 2 為往下
* 上下樓梯: 相關設定在 Player&GameManager>GameManager，player_stay 1 代表現在在有樓梯的地方，player_up_down 1 為往上 2 為往下
* 撿石頭? 爬? 跳?
* any else ...



> 選項設定:

* StartScene>MainMenu>Gane Menu UI>Canvas>Layout>Options 可以添加選項，使用 SetOptionFromUI.cs 去根據內容調整數值，可以把值放入到 Player&GameManager>GameDataManager 裡面





> 開啟 state machine:

* 因為 state machine 一直跑掉，所以目前使用 joystick 控制人物並測試，按下 B 鍵可以跳。如果要開啟 stateMachine 功能，可以到 Player&GameManager>stateMachine 把沒勾選的 scipt 全部勾選，然後到 Player&GameManager>OVRCameraRig>TrackingSpace>CenterEyeAnchor>Canvas 開啟 Canvas 並把裡面的東西放入到 stateMachine State Visualizer 裡面



> 加上 transition 效果

* Player&GameManager>OVRCameraRig>TrackingSpace>CenterEyeAnchor>FaderScreen 可以調他的動畫就可以了，詳細可以參考 Player&GameManager>SceneManager，裡面轉場會用到這個效果





> Avator: 

* 想嘗試加上去的話可以做做看



> 調整怪物數值

* 到資料夾 Assets>Midtern>SO 裡面會有 Scriptable Object 可以調整，基本上只有 HP 、 ATK 死亡特效和特效顏色有作用，其他的目前沒有用到

