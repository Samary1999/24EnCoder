# 核心价值观加密器

核心价值观加密在线工具

用社会主义核心价值观对字符串进行对称加解密

纯前端实现，没有任何美化，仅作为学习使用

Github线上Demo暂不支持自定义字典，自定义字典请去原仓库下载代码文件或者原仓库提供的链接

GithubPages线上Demo: [Demo](https://github.com/Samary1999/24EnCoder)

主要代码来源于[wheatup/hexie-encode: 自定义字典的对称加密](https://github.com/wheatup/hexie-encode)

**下面内容来源于源仓库**

# 和谐加解密

使用自定义字典对字符串进行加解密

## 安装

> `npm i hexie-encode`

## 在线使用

> [和谐加密器 (wheatup.github.io)](https://wheatup.github.io/labs/hexie)

### 用社会主义核心价值观对字符串进行对称加解密

```javascript
import { encode, decode } from 'hexie-encode';

// 公正公正友善敬业文明友善敬业敬业友善敬业敬业友善诚信民主友善自由富强友善文明诚信友善诚信敬业友善诚信民主友善诚信自由友善敬业敬业友善敬业民主友善和谐富强友善文明诚信友善民主自由文明诚信和谐友善民主公正文明和谐法治友善民主自由富强文明和谐友善文明富强公正民主敬业友善自由平等富强平等法治
encode('Hello, world! 你好世界！');

// Hello, world! 你好世界！
decode('公正公正友善敬业文明友善敬业敬业友善敬业敬业友善诚信民主友善自由富强友善文明诚信友善诚信敬业友善诚信民主友善诚信自由友善敬业敬业友善敬业民主友善和谐富强友善文明诚信友善民主自由文明诚信和谐友善民主公正文明和谐法治友善民主自由富强文明和谐友善文明富强公正民主敬业友善自由平等富强平等法治');
```

### 并且可以使用自定义的字典进行加解密

> 字典的复杂度越高，密文就越短

```javascript
import { encode, decode } from 'hexie-encode';

const dict = ['😀', '😃', '😄', '😁', '😆', '😅', '😂', '🤣', '😊', '😇', '🙂', '🙃', '😉', '😌', '😍', '🥰', '😘', '😗', '😙', '😚', '😋', '😛', '😝', '😜', '🤪', '🤨', '🧐', '🤓', '😎', '🤩', '🥳', '😏', '😒', '😞', '😔'];

// 😄😄😔😄🥳😔😁😁😔😁😁😔😁😂😔😃😊😔😏😔😁😌😔😁😂😔😁😊😔😁😁😔😄🤩😔😒😔😏😔🥰😚😚😔😗😜😙😔🥰🙂😅😔😜😘😒😔😃😗😇😂
encode('Hello, world! 你好世界！', dict);

// Hello, world! 你好世界！
decode('😄😄😔😄🥳😔😁😁😔😁😁😔😁😂😔😃😊😔😏😔😁😌😔😁😂😔😁😊😔😁😁😔😄🤩😔😒😔😏😔🥰😚😚😔😗😜😙😔🥰🙂😅😔😜😘😒😔😃😗😇😂', dict);
```

# 最后这里提供一个两千四百多汉字的字典
```javascript
['局', '耳', '耽', '届', '屋', '屈', '耻', '漆', '展', '漂', '屑', '漏', '属', '鄙', '耗', '耕', '屠', '屡', '耐', '屯', '战', '光', '贸', '猪', '戚', '克', '费', '猫', '兄', '贷', '充', '或', '贴', '兆', '贵', '成', '允', '我', '戒', '贱', '秤', '集', '宇', '雅', '秧', '雄', '宁', '雁', '它', '棒', '雀', '完', '宏', '积', '秩', '安', '守', '宋', '棚', '株', '涛', '廊', '粪', '廉', '芽', '粮', '涝', '花', '芳', '俱', '粥', '消', '俩', '涉', '芬', '俯', '涌', '俭', '盆', '袭', '香', '被', '哗', '构', '首', '馒', '皱', '哑', '极', '皮', '枝', '响', '果', '馋', '哈', '馅', '林', '枕', '宾', '森', '宿', '租', '雾', '宽', '雹', '秘', '容', '秆', '棵', '室', '秃', '宣', '客', '私', '审', '秀', '种', '宫', '矿', '解', '石', '触', '替', '曾', '曲', '角', '更', '览', '觉', '矛', '见', '观', '规', '喷', '视', '颈', '领', '瞧', '港', '逼', '脏', '缝', '脉', '温', '脊', '缘', '逢', '缎', '逮', '脚', '游', '鼻', '踏', '割', '晴', '唤', '智', '售', '唯', '唱', '页', '顷', '顶', '项', '睛', '须', '晨', '顺', '顽', '景', '普', '顿', '顾', '啄', '阻', '阿', '校', '阳', '防', '蜂', '阵', '阴', '阶', '蜘', '核', '孩', '根', '蜜', '格', '栽', '季', '蜒', '学', '样', '馆', '哄', '品', '哀', '析', '袍', '枯', '袋', '枪', '袄', '哲', '枣', '哭', '袜', '哨', '哪', '哥', '袖', '的', '皇', '挖', '假', '谷', '谱', '振', '谋', '挨', '谊', '挪', '谈', '挥', '挤', '偷', '谅', '偶', '调', '挡', '兴', '关', '共', '兰', '托', '扛', '扑', '走', '扒', '打', '扔', '赶', '起', '赴', '赵', '手', '才', '扎', '扁', '所', '结', '胁', '胆', '绕', '纯', '肿', '肾', '醉', '纪', '醋', '肺', '级', '约', '纤', '红', '育', '纠', '线', '纽', '肯', '整', '数', '敲', '魔', '故', '敏', '敌', '效', '魄', '魂', '救', '敞', '教', '嘉', '言', '支', '鬼', '球', '理', '纺', '肩', '纸', '纹', '肤', '肥', '纷', '纵', '肠', '纲', '股', '纳', '醒', '肢', '纱', '肝', '肚', '峡', '肌', '肉', '恐', '匀', '恒', '轰', '软', '轮', '转', '匙', '恋', '轨', '轧', '车', '北', '化', '口', '悲', '输', '叠', '另', '句', '马', '畏', '界', '在', '摸', '摧', '驴', '驶', '驱', '驰', '驳', '地', '驼', '圾', '驾', '畜', '场', '留', '摩', '驻', '诊', '擦', '评', '识', '痕', '痒', '证', '课', '读', '型', '诸', '请', '垄', '诵', '诱', '垃', '垂', '操', '误', '杨', '吸', '饿', '吼', '杯', '饼', '行', '杰', '街', '衔', '否', '饥', '吧', '吨', '吩', '含', '听', '饮', '松', '板', '竞', '竟', '毯', '落', '塌', '锈', '锋', '锄', '锅', '销', '锁', '稠', '稿', '塞', '稼', '错', '稻', '塘', '营', '塔', '干', '津', '年', '舅', '并', '但', '幸', '幻', '洪', '位', '幼', '广', '舍', '住', '舌', '低', '洒', '舰', '佳', '舱', '底', '库', '粉', '俘', '保', '芝', '芒', '液', '粘', '涨', '俊', '建', '节', '粒', '促', '润', '延', '粗', '芹', '获', '必', '价', '忆', '件', '万', '鉴', '汤', '七', '弱', '丁', '污', '一', '池', '与', '不', '下', '草', '上', '强', '算', '钱', '钳', '姿', '姻', '钻', '钥', '姥', '简', '钢', '钩', '姨', '妖', '妙', '铜', '铃', '铁', '如', '妄', '妇', '烤', '懒', '热', '烫', '劈', '总', '卫', '鸭', '鸡', '占', '卡', '鸣', '卧', '鸦', '怪', '怨', '卸', '鸽', '即', '危', '映', '是', '昨', '矩', '喉', '喊', '短', '风', '矮', '喂', '知', '善', '喇', '喘', '飘', '飞', '喜', '喝', '食', '僵', '控', '掠', '探', '貌', '推', '掩', '僻', '犁', '狱', '狸', '揉', '描', '狼', '插', '狡', '提', '狠', '傅', '狮', '窜', '窝', '境', '毒', '章', '毕', '童', '比', '毛', '毙', '端', '竭', '墓', '毁', '毅', '墙', '竹', '蓬', '增', '每', '别', '判', '删', '慰', '灿', '慎', '灾', '初', '慌', '创', '刚', '则', '刘', '慈', '列', '灶', '蹦', '划', '齐', '折', '抛', '抚', '抄', '现', '技', '趣', '凑', '凝', '鲜', '把', '玻', '率', '抵', '凤', '抱', '凡', '几', '凯', '抽', '索', '乳', '茶', '气', '紧', '紫', '累', '胸', '绪', '绩', '释', '重', '能', '里', '续', '量', '野', '绣', '绢', '岂', '画', '坛', '坚', '坝', '搏', '坟', '话', '垮', '诞', '垫', '诚', '症', '试', '垦', '病', '诗', '译', '词', '诉', '痛', '糊', '苗', '混', '座', '度', '深', '苏', '侍', '糟', '苍', '例', '侄', '糕', '糖', '康', '淡', '序', '便', '苹', '开', '丰', '串', '异', '弃', '丽', '絮', '举', '江', '式', '丸', '丹', '弊', '为', '主', '乃', '范', '影', '茂', '氧', '洗', '幅', '船', '洞', '使', '佣', '洁', '你', '幕', '洋', '佩', '航', '般', '菌', '于', '亏', '二', '泪', '事', '菊', '吐', '杀', '补', '吗', '杆', '君', '登', '表', '衫', '杏', '衬', '吞', '百', '李', '白', '衰', '吃', '材', '村', '各', '禽', '禾', '障', '察', '寄', '寇', '密', '螺', '随', '富', '家', '宴', '零', '雷', '宵', '秒', '害', '宰', '科', '拐', '珠', '拒', '内', '拔', '践', '拖', '拘', '冈', '招', '班', '再', '拜', '册', '冒', '担', '拆', '跪', '写', '拉', '稳', '锐', '塑', '键', '稍', '锯', '税', '款', '萝', '欺', '填', '程', '锦', '锤', '稀', '锣', '欲', '锡', '萍', '萌', '仇', '仅', '念', '治', '快', '仙', '油', '付', '沸', '沿', '沾', '河', '仓', '忠', '忧', '仗', '他', '器', '改', '攻', '放', '政', '攀', '琴', '嚼', '旬', '瓜', '旨', '早', '日', '旦', '嚷', '旧', '无', '既', '旺', '旷', '膝', '美', '差', '膜', '邮', '羊', '巩', '膛', '巨', '邪', '巧', '左', '工', '巡', '那', '道', '遗', '腥', '崖', '罢', '时', '旱', '族', '旋', '瓶', '旅', '旁', '旗', '瓦', '瓣', '斩', '固', '誉', '断', '国', '图', '斯', '困', '斤', '围', '挎', '爽', '停', '谨', '做', '爹', '按', '爸', '指', '爷', '父', '谦', '挂', '爱', '谣', '谢', '偏', '爬', '爪', '历', '惑', '厂', '述', '黎', '厌', '惜', '追', '厉', '压', '迹', '情', '厕', '黑', '原', '厘', '迫', '默', '惊', '厚', '予', '注', '争', '了', '德', '泥', '波', '泡', '菜', '微', '泽', '泼', '泻', '些', '循', '亚', '井', '五', '泳', '互', '挠', '谁', '挣', '挽', '谜', '挺', '健', '爆', '倚', '牺', '特', '捉', '候', '豪', '倘', '捏', '借', '捎', '象', '牲', '捧', '版', '牌', '倡', '倦', '片', '捷', '状', '掏', '掌', '僚', '授', '掉', '犹', '像', '犯', '犬', '掘', '接', '房', '公', '贞', '六', '负', '八', '全', '户', '戴', '入', '兽', '猜', '兼', '养', '猛', '截', '典', '具', '其', '兵', '麦', '熄', '叫', '熊', '只', '辛', '叨', '可', '叮', '辜', '辟', '辞', '悼', '召', '史', '患', '右', '台', '悠', '霉', '需', '椒', '婆', '震', '婚', '霜', '植', '霞', '椅', '破', '楼', '虚', '革', '础', '面', '靠', '虑', '虏', '虎', '锻', '锹', '欣', '欢', '堂', '葱', '堆', '葵', '镇', '空', '歉', '穿', '镜', '葬', '歌', '葡', '愤', '愧', '剩', '剪', '副', '愿', '鼠', '剥', '剧', '踩', '愉', '踪', '愈', '意', '愁', '剑', '鼓', '踢', '剖', '愚', '孤', '孙', '存', '栋', '示', '孝', '队', '礼', '栏', '孟', '社', '子', '蜡', '孕', '孔', '标', '字', '阔', '蜻', '树', '暗', '预', '暖', '暑', '颂', '颜', '额', '题', '颗', '暂', '嗓', '瞎', '颤', '暴', '颠', '暮', '嗽', '覆', '瞒', '要', '命', '本', '呼', '术', '木', '末', '未', '朴', '朵', '朱', '呢', '朽', '周', '机', '相', '盾', '柏', '盼', '盲', '语', '高', '详', '该', '询', '痰', '垒', '骨', '疏', '骡', '骤', '疆', '基', '培', '播', '疑', '疗', '撤', '论', '埋', '赢', '赠', '扇', '赤', '赚', '批', '赛', '找', '承', '赞', '扰', '赔', '扶', '赖', '扫', '扩', '扯', '儿', '鱼', '扮', '董', '穷', '歇', '究', '穴', '葛', '堪', '死', '歼', '堡', '堤', '著', '歪', '镰', '步', '堵', '此', '疫', '许', '访', '设', '疯', '讽', '撞', '验', '疮', '城', '撑', '骂', '讲', '撒', '记', '撕', '疤', '骆', '骄', '讨', '艳', '币', '似', '希', '艺', '伸', '师', '浙', '浇', '浆', '帖', '浅', '伤', '米', '流', '传', '帐', '伯', '济', '帝', '橡', '失', '筑', '筐', '策', '头', '答', '太', '筋', '夫', '天', '等', '央', '大', '依', '庭', '淹', '供', '添', '联', '聚', '酬', '就', '酱', '酷', '聋', '尸', '酸', '酿', '尼', '尿', '潮', '职', '尾', '演', '居', '层', '腔', '遥', '湾', '湿', '遭', '遮', '崭', '清', '逗', '缴', '途', '递', '逐', '速', '逝', '通', '缸', '缺', '渔', '逆', '茅', '茄', '久', '彻', '之', '义', '役', '么', '乏', '乎', '彼', '茎', '乌', '形', '乒', '乓', '乐', '乖', '水', '乔', '淘', '庆', '侵', '庄', '英', '糠', '侮', '废', '府', '系', '淋', '侨', '庙', '侦', '若', '店', '侧', '苦', '应', '川', '州', '溉', '源', '邀', '巾', '羞', '膏', '溪', '膊', '邻', '巷', '巴', '膀', '已', '己', '元', '贯', '购', '戏', '猾', '贫', '贪', '贩', '质', '党', '货', '兔', '猴', '败', '贤', '责', '财', '贡', '猎', '贝', '肆', '峰', '肃', '澡', '封', '将', '射', '尊', '配', '小', '潜', '少', '酒', '尖', '尚', '尘', '聪', '尝', '繁', '尤', '碍', '碌', '鞭', '碎', '蚂', '碑', '蚀', '蚁', '碗', '榨', '蚊', '嫂', '嫁', '碧', '鞋', '榜', '嫌', '概', '碰', '榆', '腰', '崇', '罩', '罪', '腹', '腾', '腿', '置', '遍', '网', '罐', '罗', '遵', '罚', '腊', '避', '腐', '遣', '傍', '狭', '独', '狐', '握', '傲', '狗', '揪', '傻', '揭', '狂', '援', '储', '催', '贿', '免', '献', '贼', '先', '贺', '壁', '蒸', '殃', '殊', '残', '段', '壤', '窄', '突', '窃', '殿', '蒜', '壮', '蒙', '士', '壶', '窗', '声', '窑', '壳', '铅', '妈', '篮', '铲', '银', '铸', '妻', '铺', '妹', '链', '藏', '篇', '妥', '妨', '笼', '第', '裂', '监', '咱', '盒', '咳', '裁', '查', '盖', '装', '盗', '盈', '裙', '益', '咬', '盏', '柿', '柱', '柳', '柴', '裕', '博', '鸟', '卜', '怎', '态', '怀', '焰', '单', '南', '然', '卖', '煎', '煌', '恼', '匪', '恶', '恳', '匠', '恰', '息', '桌', '祸', '案', '陕', '框', '桃', '桂', '限', '降', '票', '陈', '蝶', '陆', '祥', '蝴', '附', '际', '桐', '桑', '殖', '跨', '军', '农', '拌', '拍', '路', '拳', '跑', '冠', '拴', '冤', '距', '拿', '珍', '拼', '冬', '拢', '冲', '削', '感', '前', '剂', '剃', '齿', '慨', '券', '刻', '刺', '蹈', '慧', '刷', '制', '蹄', '到', '慢', '灌', '刮', '利', '秋', '雨', '宪', '雪', '雕', '宗', '称', '检', '宜', '宝', '棍', '实', '官', '棉', '宙', '定', '移', '棋', '棕', '宅', '艇', '企', '帽', '伍', '伏', '浮', '浩', '常', '浪', '帆', '伶', '伴', '帅', '艰', '市', '浓', '布', '估', '色', '浑', '胞', '经', '胜', '练', '胖', '组', '织', '绘', '岸', '给', '络', '绝', '背', '绞', '统', '绑', '胃', '绒', '胀', '怠', '印', '性', '卷', '急', '卵', '却', '午', '半', '怜', '思', '华', '协', '十', '怒', '千', '怕', '怖', '焦', '升', '胳', '继', '采', '胶', '岛', '绸', '绿', '金', '绳', '胡', '激', '岗', '岔', '维', '绵', '岩', '终', '绍', '岭', '娱', '确', '虽', '虾', '硬', '楚', '虹', '娇', '娃', '威', '非', '静', '虫', '娘', '青', '梢', '梦', '隶', '寺', '寻', '蔑', '樱', '筹', '夜', '够', '签', '夕', '外', '橘', '复', '夏', '处', '备', '蕉', '筛', '夺', '夹', '夸', '筝', '启', '餐', '蠢', '最', '服', '呜', '朋', '有', '月', '员', '呆', '瘦', '朗', '呀', '期', '朝', '告', '望', '呈', '乘', '乙', '彩', '乞', '也', '九', '乡', '习', '当', '归', '茧', '录', '书', '茫', '氏', '素', '买', '民', '乱', '考', '山', '漠', '老', '耀', '屿', '耍', '而', '漫', '自', '滋', '翻', '翼', '臭', '臣', '郑', '郊', '滚', '渗', '渐', '缠', '适', '逃', '退', '送', '脱', '脾', '透', '缩', '脸', '选', '编', '脆', '缓', '渣', '渡', '脂', '渠', '拣', '决', '冰', '跃', '拦', '冶', '冷', '拥', '况', '冻', '拨', '择', '跌', '括', '嘴', '嘱', '散', '敢', '敬', '瑞', '凭', '趟', '押', '王', '玉', '抹', '凶', '超', '护', '报', '抢', '趁', '凳', '抬', '出', '击', '披', '越', '趋', '跳', '叉', '又', '边', '友', '及', '反', '双', '达', '悟', '辽', '发', '辣', '悄', '叔', '变', '辪', '辫', '叙', '磁', '槽', '蛛', '蛙', '蛇', '韵', '音', '蛋', '槐', '蛾', '磨', '蛮', '砌', '砍', '码', '霸', '露', '研', '砖', '婶', '云', '御', '泰', '京', '亭', '亮', '泉', '亩', '泊', '享', '交', '泄', '亦', '产', '得', '徐', '亡', '菠', '徒', '亿', '穗', '武', '委', '姐', '姑', '箱', '钓', '姓', '钞', '姜', '薯', '钟', '薪', '管', '箭', '箩', '钉', '始', '针', '薄', '沉', '莫', '忙', '仪', '们', '代', '沃', '令', '志', '沙', '任', '忍', '份', '忌', '沟', '仿', '莲', '仰', '心', '刑', '灰', '灯', '灭', '刊', '火', '分', '切', '慕', '刃', '刀', '蹲', '炒', '躁', '炕', '勺', '勾', '勿', '勤', '炉', '炊', '炎', '勒', '龙', '炸', '点', '身', '躬', '炼', '龟', '躲', '勇', '龄', '勉', '躺', '炮', '炭', '励', '劲', '劳', '商', '眠', '易', '眯', '星', '眨', '啊', '昆', '昂', '昌', '眼', '昏', '明', '啦', '省', '显', '昼', '看', '眉', '春', '良', '帜', '类', '伪', '帘', '舒', '洲', '体', '何', '余', '活', '佛', '舞', '作', '舟', '洽', '派', '平', '悉', '辨', '辩', '叛', '辬', '厦', '返', '燃', '想', '近', '运', '惰', '违', '远', '迟', '连', '这', '还', '惹', '进', '咐', '裤', '柄', '直', '裹', '盯', '咏', '目', '柜', '和', '染', '裳', '某', '柔', '盘', '咸', '盛', '咽', '盟', '盐', '阀', '阁', '栗', '阅', '神', '祝', '桨', '陵', '祖', '陷', '蝇', '桥', '陶', '档', '险', '陪', '除', '恭', '鹿', '医', '区', '匹', '恩', '恨', '恢', '鹰', '轿', '煮', '载', '鹊', '轻', '煤', '包', '匆', '照', '鹅', '鹂', '梨', '寸', '对', '梯', '融', '寿', '难', '导', '梳', '禁', '械', '寨', '福', '梁', '寒', '隐', '梅', '隔', '离', '隙', '严', '引', '两', '丧', '汇', '汁', '荣', '弓', '荡', '丢', '求', '中', '药', '弟', '汉', '个', '弄', '临', '荷', '汗', '吊', '合', '吉', '后', '束', '杜', '同', '名', '条', '饲', '杠', '饱', '血', '饰', '饶', '吴', '吹', '饺', '较', '悦', '叶', '号', '辅', '熔', '辆', '辈', '辉', '您', '司', '麻', '叹', '熟', '叼', '悬', '辱', '辰', '参', '悔', '架', '皆', '皂', '睡', '晒', '晓', '督', '晕', '唇', '唉', '晚', '睬', '西', '唐', '晃', '晋', '晌', '着', '睁', '晶', '滑', '至', '翠', '郁', '臶', '滔', '臵', '致', '滨', '滩', '都', '臂', '满', '滤', '滥', '部', '翁', '翅', '滴', '羽', '涂', '信', '粱', '芦', '浴', '带', '众', '海', '伞', '伟', '浸', '优', '伙', '艘', '会', '址', '均', '用', '甩', '坊', '搜', '搞', '坏', '坑', '由', '搁', '田', '坐', '申', '搂', '甲', '搅', '电', '块', '男', '让', '疼', '议', '讯', '疾', '域', '训', '订', '疲', '计', '骑', '骗', '认', '撇', '吓', '权', '衡', '杂', '衣', '向', '厨', '迅', '惧', '燕', '过', '迁', '惠', '惯', '县', '迎', '惭', '迈', '去', '惨', '惩', '迷', '惕', '厅', '燥', '黄', '斥', '斧', '方', '园', '施', '因', '璃', '团', '四', '回', '文', '囊', '料', '斜', '斑', '斗', '畅', '圣', '倒', '捆', '牵', '物', '捞', '损', '倍', '牢', '捐', '牧', '捕', '牙', '牛', '债', '值', '倾', '据', '捡', '换', '豆', '很', '泛', '律', '人', '法', '待', '径', '征', '往', '亲', '今', '介', '沫', '从', '仍', '忽', '什', '没', '仁', '仆', '摔', '略', '圆', '圈', '摘', '番', '摄', '警', '摇', '摆', '土', '摊', '坡', '携', '甚', '甘', '生', '搭', '搬', '烟', '势', '烘', '烛', '务', '加', '劣', '烂', '助', '动', '烈', '劫', '努', '懂', '办', '功', '劝', '力', '烧', '烦', '竿', '母', '墨', '闪', '立', '门', '闯', '问', '蓝', '闭', '闲', '闷', '间', '竖', '蓄', '闻', '站', '闸', '毫', '闹', '赌', '扭', '赏', '扬', '扣', '执', '资', '投', '抗', '趴', '抖', '准', '足', '净', '鲁', '抓', '环', '减', '玩', '凉', '奏', '蔽', '笨', '奉', '奋', '符', '奇', '好', '笛', '横', '她', '奸', '奶', '奴', '笔', '女', '笑', '模', '笋', '奥', '汪', '三', '弹', '丈', '弦', '世', '且', '荐', '专', '荒', '张', '丑', '弯', '东', '丝', '汽', '业', '丛', '丘', '丙', '鞠', '榴', '蚕', '嫩']
```
