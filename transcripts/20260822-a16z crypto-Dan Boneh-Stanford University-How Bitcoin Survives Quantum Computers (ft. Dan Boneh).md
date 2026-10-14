---
访谈时间: 2026-08-22
访谈时间说明: "无法确认实际访谈时间，使用 YouTube 发布时间。"
嘉宾名字: "Dan Boneh"
嘉宾公司名称: "Stanford University"
参与嘉宾:
  - 姓名: "Dan Boneh"
    公司或机构: "Stanford University"
    职务: "计算机科学与电气工程教授，Stanford Computer Security Lab 联合主任"
  - 姓名: "Tim Roughgarden"
    公司或机构: "a16z crypto、Columbia University"
    职务: "a16z crypto 研究负责人，Columbia University 计算机科学教授，主持人"
播客名称: "a16z crypto"
播客url地址: "https://www.youtube.com/watch?v=E61gUCKcx2s"
youtube_video_id: "E61gUCKcx2s"
YouTube发布时间: "2026-08-22T14:30:31Z"
字幕来源: "YouTube 原始字幕 en-orig，经上下文转写为简体中文"
全文提及的关键名词:
  - Dan Boneh
  - Tim Roughgarden
  - post-quantum signatures
  - Bitcoin
  - Ethereum
  - ECDSA
  - Schnorr
  - hash-based signatures
  - lattice-based signatures
  - one-time signatures
  - few-time signatures
  - stateful signatures
  - SLH-DSA
  - Sphinx
  - XMSS
  - Merkle tree
  - Winternitz signatures
  - threshold signatures
  - context-aware threshold PRF
  - MPC
  - FHE
  - quantum computers
  - Satoshi
---

# How Bitcoin Survives Quantum Computers (ft. Dan Boneh)

## Transcript

这次讲座的边界是：研究结果提供了新的构造和风险拆解，但并没有宣称 Bitcoin 已经完成迁移，也没有给出量子计算机出现时间的预测。真正的完成标准应当是算法、钱包、节点、区块空间、治理和恢复流程都能在公开条件下被测试和复核。今天的实际行动重点不是预测量子计算机哪一天出现，而是尽早让活跃钱包拥有迁移能力，让新签名在真实硬件和真实网络中完成测试，并让社区提前讨论废弃资产和恢复资格。只要这些问题仍未解决，所谓完全量子安全就只能是一句不完整的宣传，而不是可以交付给持有人的安全承诺。

因此，算法论文、钱包实现和主网升级必须同步推进，任何一个环节拖延，都会缩短实际迁移窗口并放大持有人风险。

Tim：Dan Boneh 来到 a16z crypto 实验室，总是能带来非常及时的话题。Dan 是著名 cryptographer、Stanford University 长期任教的教授，也是很多 crypto 从业者的导师。今天讨论 post-quantum signatures，以及 Bitcoin 和其他 blockchain 如何应对量子计算机。

Dan：很高兴再次来到实验室。现在谈 post-quantum signatures，主要是为了回答一个现实问题：当量子计算机足够强大时，Bitcoin、Ethereum 等网络如何继续保护交易授权。最近每周都能看到“Bitcoin 会因为量子计算机结束”“量子计算机将摧毁 proof of work”之类的消息。这里面有很多夸张说法，但 blockchain 社区确实需要给出答案。网络不能等到 Q-day 到来之后才开始升级，必须提前完成 post-quantum 准备。

目前正在考虑的 post-quantum signature 主要有几类：lattice-based signatures、hash-based signatures、isogeny-based signatures、multivariate signatures，以及基于 zero-knowledge proof of pre-image 的方案。问题是，blockchain 应该使用哪一类。

我过去多年一直支持 lattice-based signatures，因为 blockchain 传统上需要 ECDSA 和 Schnorr 提供的 algebraic structure，而 lattice 体系在某种程度上也能提供这种结构。但现实可能不会沿这条路线发展。市场对新 cryptographic assumptions 的担忧，加上某些 lattice 方案的事件，让 lattice-based signatures 在 blockchain 中的推进变得更难。

Bitcoin 和 Ethereum 现在更可能采用 hash-based signatures。原因是 hash-based 方案不需要引入新的复杂安全假设。Bitcoin 当前依赖 ECDSA 和 Schnorr 的 discrete-log assumption；如果改用 hash-based signatures，系统可以主要依赖 SHA-256。Bitcoin core developers 对 lattice-based cryptography 的接受度并不高，所以 hash-based 路线可能是最终方向。

今天先讲 hash-based signatures 的基本结构，后半部分介绍我们关于 threshold signing 的新研究。

### 一次签名、少次签名和有状态签名

Dan：第一类术语是 one-time signature。它的安全前提是同一个 public key 最多只签一条消息。签完一条消息，就必须更换 public key；如果同一个 public key 签两条消息，系统可能失去安全性。优点是 signature 可以比较短，某些实例只有约 292 bytes，但验证速度可能较慢。也可以用更长的 signature 换取更快的验证。

第二类是 few-time signatures。它允许同一个 secret key 签少数几条消息，但签名次数越多，安全性逐步下降。可以通过重新设置参数，让系统支持 10 次或 100 次签名，同时保持一定的 security level。超过上限后，安全性不是突然从 100% 变成 0%，而是随着复用次数增加而逐渐恶化。

第三类是 stateful few-time signatures。基本做法是把许多 one-time public keys 放进一棵 Merkle tree，每个叶子只签一次。这样可以用一个总的 public key 代表很多一次性 public keys，signature 仍然相对短，验证也很快。

但是，签名者必须记录已经使用过哪一个叶子，也就是维护一个 counter。下一个签名必须使用下一片叶子。这就是 stateful 的含义。最大的危险在于 counter 状态没有正确更新，或者多个设备之间不同步，导致同一个叶子被使用两次。一旦出现这种情况，signature scheme 可能被攻破。

如果要在 Q-day 之前部署 stateful signatures，我强烈建议使用 hybrid signature scheme，把 stateful signature 和 ECDSA 组合起来。即使在维护状态时犯错，ECDSA 部分仍然能在量子计算机出现之前保护系统。只有到 Q-day 时，ECDSA 才会失去保护作用，所以在那以前可以获得一个过渡安全层。

主持人：private key 很长，会不会成为问题？

Dan：不会。private key 通常只是一个 seed，通过 PRF 生成各个叶子的 secret key，不需要保存二的十次方个 secret keys。如果需要使用第七个叶子，可以即时生成第七个 secret key。这里没有 forward security，但即时生成叶子是这类系统的重要特性。

### SLH-DSA、Sphinx 和签名尺寸

Dan：NIST 已经标准化了 SLH-DSA，它基于 Sphinx framework。SLH-DSA 设计为在同一个 public key 下支持大约 2 的 64 次方个 stateless signatures，签名不需要维护 counter。但代价是 signature 很大，常规参数大约是 8 kilobytes；更快的签名器还会让 signature 变得更大。

它适合 software update system，因为软件更新本来就要传输 megabytes 的数据，signature 大小不是核心问题。但 blockchain 不能为每一笔交易都放入 8KB signature。Bitcoin 和 Ethereum 也没有必要支持 2 的 64 次方笔交易，因此 NIST 在今年 4 月提出了缩小版 Sphinx。它把支持范围降到约 2 的 24 次方，signature 可以缩短到约 3.8 kilobytes。

这个缩小版的签名速度很慢，大约需要十亿次 hash computation。通常可能只需要几百万次，但这个设计在签名时要承担很高的计算量。好处是 verification 只需要约 300 次 hashes，因此非常适合把 verifier 放入 ZK SNARK 中。签名尺寸、签名时间和验证时间之间有多个可以调节的参数。允许 verifier 做更多工作，可以进一步压缩 signature；也可以扩大 signature 换取更快的 signer。实际参数选择需要脚本计算对应的 security level。

SLH-DSA 的关键结构是一棵巨大的虚拟树。首先生成一棵由 many one-time signature public keys 构成的 XMSS tree。每个叶子只能签一条消息。每个叶子的 public key 又可以签一个 few-time signature 的 public key，这样层层嵌套，直到得到足够多的可用叶子。

整个 2 的 64 次方叶子的 tree 不可能真的在内存中建立。它是 virtual tree：只有在要签名时，系统才根据 seed 生成需要的路径，其余部分永远不被 materialize。secret key 和 public key 都可以保持很短。public key 可以理解为顶层的 Merkle root，签名时提供使用叶子对应的 authentication path。

签名时，系统随机选择一片叶子，用 seed 推导该叶子的 secret key 和 public key，再用 few-time signature 对消息签名，同时用 one-time signature 对这片叶子的 public key 签名。最后把连接叶子到 Merkle root 的 authentication path 放入 signature。验证者使用路径重建 root，并检查它是否与记录的 public key 一致。

为什么随机选择叶子？因为这是 stateless scheme。如果从左到右顺序使用叶子，就必须保存 counter，重新引入状态问题。随机分配会变成一个 bins-and-balls experiment：每次签名相当于把一个球放进随机叶子对应的 bin。系统需要确保任何一个 few-time signature 没有被使用过多次，使整体 forgery probability 低于二的负 128 次方。参数脚本正是用来计算这种最坏负载和安全概率。

如果能够以 stateless 的方式改进 hash table，让球更均匀地分布，SLH-DSA 还可以得到改善。double hashing、cuckoo hashing 等 data structure 技巧可以降低最拥挤 bin 的负载，但如何在不保存状态的条件下做到这一点，仍然是一个有趣的研究问题。

### Bitcoin 和 Ethereum 的迁移计划

Dan：Ethereum 有一套名为 leanig 的方向，Bitcoin 这边叫 shrinks。Ethereum 的方案仍在变化，而 shrinks 已经逐渐写进 Bitcoin 的 BIP。整体思路是使用两类 keys。

第一类是 long-term stateless public key，从 seed phrase 导出，支持较多的签名次数。第二类是 short-term key，理想情况下每次只用于一笔 transaction，每笔交易之后都更换。short-term key 的生成会用 wallet ID 和 stateful counter。虽然它的实际复用限制可能放宽到 5 或 10 次，但本质上仍要小心维护状态，因此 hybrid signature 仍然重要。

正常情况下，交易的 calldata 会带上下一笔交易使用的 public key。当前 public key 签这一笔交易，然后替换为下一次使用的 one-time public key，形成连续滚动的短签名链。long-term key 只在 recovery 场景使用。如果钱包坏了、丢失 wallet ID，尤其是丢失 counter，用户必须停止使用不确定的 short-term state，用 long-term key 重新初始化新的 short-term key chain。

这里存在一个工程细节：wallet 需要判断本地保存的 state 是否是最新的。即使把 counter 和 next public key 放到 call data，恶意节点也可能向钱包提供较旧的 block，让钱包重复使用旧 counter。因此，钱包仍要保留本地 state，并验证它的新鲜度。

如果硬件钱包同时管理很多 chain 和很多 wallet，nonvolatile memory 可能不够，设备需要把部分 state 卸载到 laptop。但 laptop 也可能提供错误的旧 state，所以设备必须保存某种 counter 来确认外部 state 的新鲜程度。这会给 Ledger、Trezor 等钱包厂商带来工程负担。

当前硬件钱包的另一个问题是，hash-based signature 在现有处理器上可能需要几十秒生成 key 和 signature。未来的处理器如果内置 SHA-256 hardware acceleration，运行时间可以改善。恢复钱包并不是只能做几次，因为 long-term stateless key 可以支持约一百万次 recovery，甚至可以根据实际需要把参数缩小到二的十四次方。若接近上限，可以用旧 key 的最后一笔交易刷新新的 key chain，必要时也可以更换 seed phrase。

把 state 写入 blockchain 可能帮助钱包确认状态，但不能完全依赖链上信息，因为钱包还需要防止外部节点提供 stale state。总体来看，hash-based signatures 会在未来几年成为 Bitcoin 和 Ethereum 的重要基础设施，但钱包厂商需要为状态同步、恢复和硬件加速做大量工程工作。

### hash-based threshold signing 的问题

Dan：如果使用 hash-based signatures，还需要考虑 threshold signing。传统 multi-signature 是生成 n 个 public keys，让其中 t 个参与者签名，最终交易带有 t 个 signatures。它的问题是最终 signature 很大，而且公开暴露 t，外部观察者知道需要攻破多少个 key 才可能影响系统。更重要的是，thresholdized key 和普通 key 的 signature 不一样。理想情况下，是否把 key 分成多个参与者，应该是 key holder 自己的隐私，最终链上 signature 应该和普通 signature 完全相同。

可以把多份签名 SNARK 化成一个证明，但 Bitcoin 社区目前不愿意在链上内置 SNARK verification，这基本上还不是现实选项。FHE 可以做 universal thresholdizer，把任意 signature 变成普通格式的 threshold signature，但目前在 FHE 内部运行完整签名过程太慢。通用 MPC 也有类似问题，尤其是 hash-based signatures 本身需要大量 hash computation。

还有一些专门方案，例如对 Winternitz signatures 做 thresholdization，但往往要求 n choose t 足够小、为每一种 coalition 准备不同 public key，而且 t 会被公开，最终 signature 也有特殊格式。这些方案都没有完全满足“区块链只看见普通 hash-based signature”的目标。

### 用 lattice 做阈值机制，用 hash 做链上签名

Dan：我们的方向有一点特别。区块链最终只验证纯 hash-based signature，所以链本身完全不需要知道 lattice。只有 key holder 在内部决定把自己的 key thresholdize 时，才使用 lattice-based mechanism。也就是说，签名本身是标准 hash-based signature，threshold mechanism 则使用 lattice。key holder 可以自己承担 lattice assumptions，区块链不需要承认或验证 lattice 的存在。

如果 lattice assumption 失效，使用这个 threshold mechanism 的人可能失去 private key，这属于 key holder 自己选择承担的风险。但它的好处是支持较大的 N 和 T，最终仍然生成和普通 key 一样的 signature。Fireblocks 等托管机构可以采用这种方式，而没有人能够阻止它们把自己的 key 做成 lattice-based threshold key。

### threshold one-time signature 为什么困难

Dan：先看一个三选八的 threshold one-time signature。攻击者可以向三台服务器请求对 M1 签名，再向三台服务器请求对 M2 签名。普通 threshold signer 之间通常不会互相通信，只会检查各自收到的消息是否合法，于是相同的 one-time public key 可能被用在两条不同消息上，secret key 就被破坏了。

一种办法是要求签名者协调，第一组三个签名者签 M1 后告诉其他人不要再为这个 public key 签名。但这会引入很重的 coordination，甚至像是为了管理一次性签名而额外建立一条 blockchain。我们希望做到不协调。

这里会出现 quorum intersection。假设诚实参与者永远不会在同一 public key 下签超过一次，而恶意参与者数量不超过 f，那么 threshold 必须满足大于 n 加 f 再除以 2 的关系。这样，如果两个 quorum 都足够大，它们必然有一个共同的诚实签名者。这个人不会同时签 M1 和 M2，因此攻击者不能为两条消息各自收集足够的 shares。

如果底层是 d-time signature，诚实参与者最多签 d 条消息。攻击者可以拿到 n-f 个诚实参与者的 d 份 shares，再加上 f 个恶意参与者自己控制的 key。若生成一条 signature 需要 t-f 份 shares，攻击者能生成的签名数量上限大约是 d 乘以 n-f，再除以 t-f。以 t 为 n 的三分之二、恶意参与者不超过 n 的三分之一为例，攻击者最多能得到 2d 条 signatures。因此，要构造 d-time threshold signature，底层 few-time scheme 最好至少能安全承受 2d 次使用。对于两次或三次签名，可以通过提高 threshold 缩小 d 和 2d 之间的间隔；一般参数下则需要保留这个安全余量。

### context-aware threshold PRF

Dan：实现上述目标的关键工具是 context-aware threshold PRF。普通 threshold PRF 的 key generation 会生成 master secret key 和 n 个参与者各自的 secret key share。每个参与者用自己的 share 对输入 X 做一次 evaluation，combiner 收到足够的 evaluation shares 后，重建 PRF(X)。少于 t 份 shares 的攻击者无法得到 PRF 在 X 点的值。

但 threshold hash-based signatures 需要更强的性质。每份 evaluation share 还必须绑定 context。只有 t 个参与者在同一个 context 下对 X 生成 shares，combiner 才能得到 PRF(X)。如果攻击者从一个 context 得到两份、从另一个 context 得到两份、再从第三个 context 得到两份，即使总共拿到六份 shares，也不能把它们拼起来得到任何一个 context 下的 PRF 值。

在我们的场景中，context 就是被签名的 message。这样，如果不同签名者分别为不同消息提供 shares，攻击者不能把不同消息的 shares 混合起来。这个性质和我们过去讨论 encrypted mempool 时需要的 context-aware threshold decryption 有相似之处，但这里使用的是 threshold PRF。

我们给出了两种 construction。一种基于 lattice 的 BLMR threshold PRF，能够支持较大的 N 和 T。另一种是基于普通 PRF 的组合式 construction，但它在 n choose t 很小时才实用，因为参与者的 secret keys 会变大。无论使用哪一种，最终签名都还是普通的非 threshold signature，是否做 thresholdization 只有 key holder 自己知道。

### Winternitz one-time signature

Dan：为了说明 construction，先回顾 Winternitz one-time signature，也叫 WOTS。它的思想来自 Robert Winternitz，他当年是 Stanford 的 PhD student，却没有把这个经典构造单独写成 paper。Ralph Merkle 在 thesis 中提到他的贡献，于是这个名字流传下来。这个故事给研究者的教训是，有好想法一定要写下来，否则同一个想法可能被别人反复重新发现。

WOTS 先生成一组 secret values，例如 x1 到 x8。对每个值做 hash chain，得到一排顶端值，再把顶端值压缩成一个短 public key。实际系统中，hash chain 可能长度为 16；缩小参数的版本可能只有约 4。

签名时，把 message 通过一个函数 P 映射成长度为 8 的向量。向量中的每个数决定对应 hash chain 上暴露到哪一个位置。可以把整个签名看成穿过这张 hash-chain 表格的一条 cut，签名就是 cut 下方的绿色元素。验证者把这些元素继续 hash 到顶端，再压缩顶端一行，检查是否得到正确 public key。

安全性来自 P 的 cover-free property。假设消息 M1 的向量完全覆盖消息 M0，那么拿到 M1 的签名后，攻击者可能沿 hash chain 方向推导出 M0 的签名，这就是不允许的情况。因此对任意两个消息，都不能让一个向量在所有坐标上支配另一个向量。P 还需要满足 collision resistance 或更精确的 target collision resistance。

### threshold Winternitz 的构造

Dan：我们先生成一个 threshold PRF，让它提供 master key 和每个 signer 的 key share。然后用 PRF 生成 Winternitz 表格的底行。表格顶行的元素本身是秘密，不能直接交给不受信任的 combiner，否则 combiner 可以伪造签名。所以我们用 PRF 产生的值对每个顶行元素做 one-time-pad encryption，把加密后的 Winternitz table 放进 combiner public key。

签名时，每个 signer 对表格中的每个位置释放一份 PRF evaluation share，并且使用 message 作为 context。combiner 收到足够多的签名者 shares 后，可以重建这些 PRF 值，解除顶行元素的遮蔽，恢复对应的 Winternitz signature。链上最终看到的仍然是标准的 hash-based signature。

context 是不可省略的。如果一条 message M 被两条不同消息 M1 和 M2 的向量共同支配，那么拿到 M1 和 M2 的签名后可以伪造 M。攻击者可以让一半参与者对 M1 提供 shares，再让另一半参与者对 M2 提供 shares。单独看，每条消息都不足以达到 threshold；但如果没有 context，攻击者可以把对应位置的 shares 拼起来，刚好凑出 M 所需的 shares。把 message 绑定为 context 后，不同消息的 shares 无法组合，攻击路径就被切断了。

在 collision-resistant 的 P 下，可以得到自适应安全性证明。如果改用 target collision resistance，签名过程需要两轮，因为签名者要先生成随机性，再完成 TCR 相关操作。这个两轮特征是实际部署时需要考虑的工程成本。

这个方法也可以推广到 XMSS 和 few-time signatures。对于 d-time stateful signature，key generator 的工作量大约会增加 d 倍，因为要生成 d 组 Winternitz public keys。它不适合直接 thresholdize SLH-DSA 的完整 2 的 64 次方 tree，因为 combiner public key 会变得太大。若确实需要 thresholdize SLH-DSA，可以用 MPC；我们的方法不能完全取消 MPC，但能显著减少在 MPC 中需要运行 SHA-256 的次数。

### 研究边界、区块大小和废弃资产

Dan：当前还需要解决 distributed key generator，也就是如何为这些 hash-based threshold signatures 建立 DKG。另一个方向是 silent setup，让 N 和 T 能在运行中改变。这些都是正在推进的研究，而不是已经可以直接部署的产品。

有人问，lattice 里的 algebraic structure 能否用来实现 blind signatures、ring signatures 或其他协议。直觉上可能可以：signature 仍然是 hash-based，协议层用 lattice 做辅助。但这仍是开放问题，需要进一步研究。threshold PRF 的 robustness 也可以按通常方式加入 proof of knowledge，防止参与者发送假的 PRF share。

更大的 signature size 是 Bitcoin 迁移时最现实的系统问题之一。Ethereum 的方案可能是把一个 block 内的大量 signatures SNARK 化，每 12 秒生成一个证明，说明 block 中的签名都正确。Bitcoin 目前还没有最终答案。shrinks 的实际 signature 会比今天的 64 bytes 大很多，可能是数百 bytes，成本大约增加一个数量级。社区有人认为可能需要重新讨论 block size，也有人担心重新打开 block size wars。至少交易数量本身不一定增加，只是每笔交易的 signature 更大，但 Bitcoin 如何处理仍然未知。

这甚至还没触及 abandoned assets。更换 ECDSA 后，长期不动的 coins 要怎么处理，是技术和政治问题的结合。一种想法是在 Bitcoin 上预先设置一个特殊 address，例如由 Pi 的数字组成。只要这个 address 没有被攻破，网络继续使用旧的 ECDSA；一旦第一个可信的 quantum computer 破解它，就触发取消 ECDSA，废弃资产进入单独的 recovery procedure。这依赖于第一个拥有量子计算机的人是善意参与者，当然不是理想的安全假设。

Satoshi 的情况尤其有趣。假设一百年后 ECDSA 已被取消，Satoshi 想证明自己拥有早期 coins，但量子计算机存在后，任何人都可以生成对应 secret key，单纯签一笔交易不再能证明“我在 2026 年就知道这个 key”。一种解决思路是现在先生成一笔花费 Satoshi coins 的 transaction，但不把 transaction 直接广播，因为那会暴露 Satoshi 已经苏醒。可以把 transaction 放进 hiding commitment，再用 OP_RETURN 把 commitment 写入链上。未来 Satoshi 可以拿出原始 transaction 和 2026 年的 commitment，证明自己在量子计算机出现之前就掌握 secret key，从而申请恢复资产。

这个 recovery path 还有大量细节需要解决，所以社区可能会尽量把它推迟。目前更重要的问题是保护今天仍然活跃、能够在迁移机制出现后移动资产的 Bitcoin holders。post-quantum migration 不是一个单纯换算法的问题，而是钱包状态、区块大小、签名成本、历史资产、治理协调和恢复证明共同组成的系统工程。

Tim：总结一下，hash-based signatures 可能成为 Bitcoin 和 Ethereum 的主要 post-quantum 路线，但它们带来更大的 signature、更复杂的钱包状态和更高的迁移成本。Dan 的 threshold 方案让链上只看到普通 hash-based signature，同时把 lattice 机制留在 key holder 的内部选择中。现在仍需完成 DKG、参数、钱包、区块空间和 abandoned assets 的设计。谢谢 Dan 来到实验室。

Dan：谢谢邀请。

### 从旧 signature 到 post-quantum signature 的取舍

Dan：从工程角度看，迁移不是简单把 ECDSA 的名字换成另一个名字。ECDSA 和 Schnorr 有成熟的 algebraic structure，很多 wallet derivation、batch verification、threshold protocol 都依赖这些结构。换成 hash-based signatures 后，很多熟悉的能力会消失。例如 HD wallet 中的 hardened key derivation 使用 public-key algebra 把一个 public key 推导成另一个 public key，这在 hash-based scheme 中基本不可行。lattice-based signatures 也许可以保留部分类似能力，所以 lattice 仍有长期吸引力，但当前社区对新假设的谨慎让它更难成为 Bitcoin 的第一选择。

另一个取舍是 signature 变大。今天 Bitcoin 的 signature 约 64 bytes，shrinks 这样的 stateful hash-based signature 可能达到数百 bytes，成本大约放大一个数量级。它不会必然增加每秒交易数量，但会增加每个 block 所需空间。Ethereum 可以在 block 级别用 SNARK 把签名聚合，Bitcoin 是否愿意引入类似验证逻辑还不确定。有人可能提出增加 block size，也有人担心这会重新打开历史上的 block size wars。

状态管理也和“能否复用”不同。short-term key 不是绝对只能签一条消息，而是设计成一条非常短的 few-time chain。允许同一状态偶尔重复一两次，是为了防止极小的设备失步立即造成安全事故。但如果超过预设次数，安全性会下降。因此，wallet 不能把 state 当作普通缓存，它必须把 counter 当作安全关键材料来管理。

在正常使用中，钱包可以从 seed phrase 生成 long-term key，从随机 wallet ID 和 counter 生成 short-term chain。每一笔交易把下一次的 public key 放入 calldata，链上合约或验证逻辑据此更新。这样，钱包每次只使用一个短 signature，交易保持相对紧凑。若设备丢失或本地数据库损坏，long-term key 可以重新初始化一条新 chain。long-term key 平时不签支付交易，只有在 recovery 时才出现，这样可以降低它的暴露频率。

不过，所谓把状态写入链上，也不能解决所有问题。链上可能存在多个候选状态，钱包必须判断哪个状态是最新的。恶意节点可以返回一个较旧的 block，诱导钱包使用旧 counter。设备需要维护 monotonic counter、验证 chain ID 和 wallet ID，并拒绝无法证明新鲜度的状态。硬件钱包如果内存不足，将状态交给 laptop，也必须要求 laptop 提供可验证的版本信息。

### 为什么 thresholdization 必须对外不可见

Dan：threshold signature 的核心动机不是让链知道“有几个人共同控制 key”，而是把一个 private key 的风险分散到多台机器或多个运营者，同时让链看到的仍然像普通账户。若最终 signature 直接包含 t 个参与者的 signature，观察者就知道这个账户采用了 threshold，而且知道需要攻破多少节点。这会泄露治理结构和攻击成本。

把 t 份普通 signature 先 SNARK 化是一个可行的理论方向，但 Bitcoin 还没有准备好把 SNARK verifier 作为基础操作放入协议。FHE thresholdizer 的优势是可以从任意 signature 产生一个规则格式的结果，但当前在 FHE 中运行完整 hash-based signing 太慢。MPC 可以模拟同样过程，却要承担大量轮次和 hash 计算。我们的做法把复杂的 lattice thresholding 放在链下，链上只需要验证已经熟悉的 hash-based signature。

这是一种明确的风险隔离。若 lattice 机制的数学假设未来被攻破，使用者的 threshold private key 可能被影响，但没有使用 lattice thresholding 的普通账户不受影响，区块链的验证规则也不需要因此更改。相反，如果把 lattice 直接放进链上，所有用户都会被迫接受同一套额外假设。把选择留在 key holder 手里，更符合 thresholding 是账户控制方式而不是链上资产格式的原则。

### 不协调的 threshold one-time signing

Dan：one-time signature 的特殊难点在于，诚实 signer 不应该对同一个 public key 签第二个 message，但他们之间又不能每次签名都协调。如果一个攻击者拿到三个 out of eight 的 shares，并分别向两组服务器请求 M1 和 M2，服务器单独工作就可能暴露同一 key 的两份签名。

quorum intersection 的解法是让 threshold 足够大。假设最多有 f 个恶意 signer，任何两个满足 threshold 的 quorum 必须有一个诚实交集。交集中的诚实 signer 不会对两个不同消息都签名，于是攻击者不能在两条消息上都获得足够的 shares。这里的数学和共识系统的 quorum intersection 很像，但它用于防止一次性签名的 key reuse。

扩展到 d-time signature 后，攻击者可以重复利用恶意 signer 的 key，而诚实 signer 每个最多签 d 次。若每条完整签名需要 t-f 份诚实 shares，攻击者可构造的消息数量由 d、n、f、t 共同决定。对常用的两又三分之二 threshold，底层 few-time scheme 需要至少抵抗两倍 d 的签名请求，才能给 threshold scheme 留出安全余量。这个结论告诉我们，底层 signature 的参数不能只按普通 single-user 使用来配置，必须把分布式攻击者可能组合 shares 的能力算进去。

### context 不是装饰，而是安全边界

Dan：context-aware threshold PRF 的作用可以用一个攻击场景说明。假设 P(M) 映射出了若干需要暴露的 hash-chain positions。攻击者对 M1 拿到一部分 signer shares，对 M2 拿到另一部分 shares。M1 和 M2 各自都没有达到 threshold，但它们在某些位置上合起来可能刚好覆盖 P(M)，让攻击者伪造 M。

如果每一份 PRF share 都绑定 message context，那么 M1 的 share 只能在 M1 下组合，M2 的 share 只能在 M2 下组合。不同 context 的 shares 即使数量加总，也不能产生任何有效 PRF output。于是 attacker 不能通过跨消息拼接来满足第三条消息的 hash chain。

这也是为什么 context 必须进入 evaluation，而不是只作为签名者之间的口头约定。攻击者可以故意让不同参与者看到不同消息，系统必须在 cryptographic level 阻止 shares 被交换。threshold PRF 的普通版本不提供这个边界，context-aware 版本才适合 hash-based one-time signatures。

在具体构造中，combiner 保存的是加密后的 Winternitz table，而不是秘密顶端值。签名者只释放与当前 message 绑定的 PRF evaluations。combiner 只有在收到足够数量的同 context shares 后，才能解开对应的 table elements。它本身不需要知道每个 signer 的 private key，也无法在没有 shares 的情况下伪造。对外发布的 signature 仍然可以按普通 WOTS 的方式验证。

Winternitz 的 hash chains 也说明了 signature 的尺寸和速度为何难以同时优化。链越长、参数越保守，安全性和可支持的消息空间越好，但 signing 和 verification 的成本会变大。把 chain 截短可以减少 signature，但会降低可承受的使用次数。把更多工作放到 verification 端，可以让签名者更快，却可能给每个节点增加验证负担。每个部署都要根据区块空间、钱包 CPU、网络带宽和安全等级共同决定参数。

### 研究路线和可部署性边界

Dan：我们现在有 threshold hash-based signature 的 construction 和 security theorem，但距离可部署的 production system 还有工作。首先要有可靠的 DKG，让参与者在不暴露 master secret 的情况下共同初始化 key。其次要考虑 silent setup，让参与者数量 N 和 threshold T 可以动态变化，而不用每次重建整个系统。还要处理参与者掉线、错误 share、恶意 share 和恢复流程。

robustness 可以用标准的 proof of knowledge 机制处理。参与者发送 PRF share 时，必须证明它确实来自自己的合法 secret share。如果有人发送随机数据，combiner 应该能够识别并排除，而不是在最终签名阶段才发现失败。由于 PRF 是 lattice-based，这类 proof 可以沿用 lattice proof 的常规设计，但会增加通信和计算成本。

Blind signature、ring signature 和其他 privacy protocol 是否也能采用“hash-based final signature、lattice-based internal protocol”的混合方式，目前仍是开放研究问题。这个架构有吸引力，因为链上不需要支持新的 algebraic assumption，但并不意味着所有高级协议都能自然移植。每种协议都要单独分析可组合性、匿名性和抗重放性质。

### Bitcoin 的 abandoned assets 和 Satoshi 问题

Dan：量子迁移最容易被忽略的部分是 abandoned assets。对仍在使用的钱包，可以设计迁移交易，把资产移动到新的 post-quantum address。对长期不动的 coins，尤其是丢失 seed phrase 的钱包，社区必须决定是永久冻结、允许某种恢复，还是采用自动迁移规则。这不是单纯的技术决策，因为它涉及财产权、治理权和谁有资格证明控制权。

一种自动规则是预先设定特殊触发地址。它可能由 Pi 的数字或其他公开值导出，只要量子计算机还没有破解这个地址，网络就认为旧 ECDSA 继续有效。第一个能破解它的人可能是诚实的研究机构，也可能不是。若默认第一个破解者是 good guy，就可以让他触发 ECDSA 的撤销，并把 abandoned assets 放入 recovery procedure。但这依赖一个很强的社会假设，因此只能算是讨论中的方案。

Satoshi 的 recovery path 更能说明问题。假设 Satoshi 在 2026 年知道自己拥有 coins，却不想让市场知道自己还活跃。现在直接花费这些 coins 会暴露这个事实。Satoshi 可以先制作一笔交易，把它做成 hiding commitment，只把 commitment 通过 OP_RETURN 写到链上。因为当时没有 quantum computer，只有真正知道 private key 的人才能构造正确 transaction。很多年后，在 ECDSA 已经被撤销的情况下，Satoshi 可以揭示原始 transaction 和当年的 commitment，证明自己在旧算法仍安全时就拥有这个 key。

这种方案还需要解决 commitment 格式、时间证明、链上验证、恢复资产的签名方式，以及恶意抢先揭示等问题。它说明“废弃资产如何处置”不仅是区块大小或签名格式问题，还需要建立一套可验证的历史证明。正因为复杂，社区可能先把注意力放在 active holders：让今天还能移动资产的人尽快进入 quantum recoverable 的迁移路径。

### 结尾总结

Tim：今天的结论可以分成几层。第一，Bitcoin 和 Ethereum 必须为 quantum computing 提前准备，社区并没有忽略这个风险。第二，hash-based signatures 由于不引入新的离散对数以外的复杂假设，可能成为主要迁移方向，但 signature 会更大，钱包需要管理状态，区块空间会承受压力。第三，stateful few-time signatures 很短却容易因为设备失步而出错，部署时应该加入 hybrid ECDSA 保护。第四，threshold signing 不应让链上暴露账户内部结构，context-aware threshold PRF 可以让 lattice 只存在于 key holder 的内部机制中，而链上仍验证标准 hash-based signature。

第五，Bitcoin 还没有解决 block size、abandoned assets、Satoshi recovery 和完整治理协调问题。Ethereum 可能使用 SNARK 聚合大 signature，Bitcoin 的 shrinks BIP 仍在制定。未来的迁移不能等到 Q-day 才开始，而要先完成钱包、硬件、节点、矿工和交易所的共同准备。

Dan：这项工作仍在快速发展。研究论文正在完善，DKG、silent setup、参数选择和钱包集成都还需要推进。今天能确定的是，post-quantum migration 是一个完整的系统工程，不只是把 ECDSA 替换成某个新的 signature scheme。真正安全的方案必须让 active holders 能够迁移，让 long-term holders 有 recovery path，并且让区块链在不增加不必要假设的情况下验证新的签名。

Tim：感谢 Dan 来到 a16z crypto 实验室。

Dan：谢谢。

Dan：再强调一次，量子风险有三个不同层面，不能只用“量子安全”四个字概括。第一层是签名算法本身会不会被量子算法伪造。第二层是网络有没有一个可以执行的迁移计划，以及用户能否在旧算法失效前完成迁移。第三层是迁移之后，隐私、钱包状态和历史资产是否仍然安全。某个网络即使在论文层面有一个新的签名，也不代表它解决了后三层问题。

对 Bitcoin 来说，量子计算机会带来两个方向的压力。一方面，攻击者可能从公开的 public key 中恢复 secret key，伪造授权交易；另一方面，迁移到 hash-based signatures 后，交易会携带更大的证明，节点和区块需要处理更多数据。对 Ethereum 来说，SNARK 聚合可能帮助控制链上验证成本，但生成证明的计算和工程复杂度会增加。对 Bitcoin 来说，社区还要考虑 Taproot 迁移、新旧账户共存以及不愿升级的钱包如何处理。

签名状态的风险也容易被低估。一个用户如果只有一部设备，counter 看起来很容易维护；但现实中可能有手机、硬件钱包、备份设备和交易所托管系统同时访问同一账户。设备之间只要有一次恢复顺序错误，就可能重新使用一个已被签过的叶子。hybrid signature 不是为了让系统更漂亮，而是为了在这些现实错误发生时，给用户留一个量子计算机到来之前的安全缓冲期。

如果使用 stateless 方案，用户不必保存 counter，但签名会明显变大，而且签名器或验证器需要承担更多 hash 工作。SLH-DSA 之所以可以支持极大的使用次数，是因为它把巨大的树做成虚拟结构，使用时才沿一条路径计算。但这也意味着参数、随机叶子分配和概率分析必须准确。签名数量一旦接近上限，不能只看平均负载，而要看最拥挤叶子可能承担多少次使用。

量子安全的成本最终会由不同参与者共同承担。钱包需要保存和验证状态，硬件厂商需要加入 SHA-256 加速和足够的非易失存储，节点需要接受更大的交易，矿工需要处理更大的区块，交易所需要支持新的地址和恢复流程。任何一个环节没有准备好，用户就可能在迁移窗口中失去流动性或无法移动资金。因此，算法选择必须和基础设施的时间表一起评估。

在 threshold system 中，参与者也不能只把“人数够了”当作安全证明。恶意参与者可能跨多个 message 复用自己的 shares，诚实参与者则必须有明确的规则，不能在一次性 key 下重复签名。quorum intersection 保证的是两个足够大的集合存在诚实交集，但它要求 threshold、恶意上限和底层可复用次数同时匹配。任何一个参数改变，都可能需要重新计算攻击者最多能构造多少条签名。

context-aware PRF 的价值在于把消息本身变成不可替换的标签。攻击者不能把“给 M1 的 share”换成“给 M2 的 share”，也不能把不同协议阶段的 share 直接拼接。这个想法和很多分布式密码学中绑定会话、区块高度或交易内容的做法一致，但在 hash-based threshold signature 中，它直接关系到一次性 hash chain 是否会被跨消息伪造。

研究结果的意义不是立即宣布某个 Bitcoin BIP 已经完成，而是展示了一条可能的工程路线：链上保持简单，只验证标准 hash-based signature；复杂的多方控制、分布式密钥生成和 lattice 运算在链下完成。这样可以减少对现有共识规则的改动，但也把责任转移给钱包、托管方和 key holder。它们必须自行验证 threshold setup、保护本地状态，并为参与者掉线和恶意行为设计恢复流程。

最后，量子迁移的时间窗口是一个关键变量。量子计算机可能还需要很长时间，但签名算法、钱包固件、交易所和主网升级都需要多年协调。等到“Q-day”已经明确时，用户可能已经没有足够时间迁移所有历史资产。提前采用可恢复的 long-term key、测试短期状态链、设计 abandoned assets 的 commitment，虽然会带来成本，却能把一次可能致命的系统性事件拆成多个可以验证的工程任务。

因此，今天的实际行动重点不是预测量子计算机哪一天出现，而是尽早让活跃钱包拥有迁移能力，让新签名在真实硬件和真实网络中完成测试，并让社区提前讨论废弃资产和恢复资格。只要这些问题仍未解决，所谓完全量子安全就只能是一句不完整的宣传，而不是可以交付给持有人的安全承诺。
