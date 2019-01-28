定时任务内容|定时表达式|任务名
:--|:--|:--
(每天0:00)OCR判断用户是否是忠实用户|@Scheduled(cron = "0 0 0 * * ?")|ocrVerify()
(每天0:10)小任务发奖励|@Scheduled(cron = "0 10 0 * * ?")|duocaiPullReward()
(每天0:44)拉取友盟用户数据到中间表|@Scheduled(cron = "0 44 0 * * ?")|getUmengUserCountData()
(每天0:50)计算项目统计数据到中间表 |@Scheduled(cron = "0 50 0 * * ?") |getProjectStatisticsData()
(每天1:00)检测关闭SSI问卷 |@Scheduled(cron = "0 0 1 * * ?") |executeSSIShutDown()|
(每天1:30)检查第三方问卷是否可以设置暂停状态 |@Scheduled(cron = "0 30 1 * * ?") |checkThirdPartySurveyStatus()
(每天1:40)向dataSpring上传用户信息 |@Scheduled(cron = "0 40 1 * * ?") |executePushDataSpringUser()
(每天2:00)更新没有邀请码的用户邀请码 |@Scheduled(cron = "0 0 2 * * ?") |updateInvitationCode()
(每天3:50)执行检查5天内未公众号(点击答卷菜单)或登录APP的用户(扣2分) |@Scheduled(cron = "0 50 3 * * ?") |deductionUserIntegral()
(每天4:00)向SSI上传用户信息 |@Scheduled(cron = "0 0 4 * * ?") |execute()
(每天04:30)拉取用户微信标签 |@Scheduled(cron = "0 30 4 * * ?") |addWechatTagsAuto()
(每天5:00,9:00,13:00,17:00,21:00)获取BorderLessList问卷 |@Scheduled(cron = "0 0 5,9,13,17,21 * * ?") |executeBorderLessList()
(每天8:10)拉取微信用户数据到中间表|@Scheduled(cron = "0 10 8 * * ?")|getWechatUserCountData()
(每天10:00)定时推送签到提醒信息 |@Scheduled(cron = "0 0 10 * * ?") |userSignInNotification()
(每30分)检查项目问卷IR |@Scheduled(cron = "* */30 * * * ?") |checkProjectSurveyIR()
(每1小时)定时更新最新的50条提现记录到缓存中 |@Scheduled(cron = "0 0 */1 * * ?") |cachingTakeMoneyInfo()
(每周三(12:00)发送消息【 恭喜师父，本周徒弟贡献出炉了，快去看看哦。】 |@Scheduled(cron = "0 0 12 * * WED") |apprenticeContribute()
(每周日23:50)计算最佳师傅周榜 |@Scheduled(cron = "0 50 23 * * SUN") |rankOfWeek()

