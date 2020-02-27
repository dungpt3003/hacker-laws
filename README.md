# 💻📖 hacker-laws

[![gitlocalized](https://gitlocalize.com/repo/2513/whole_project/badge.svg)](https://gitlocalize.com/repo/2513/whole_project?utm_source=badge)

Các Định luật, Lý thuyết, Nguyên tắc và Khuôn mẫu hữu ích cho các nhà phát triển.

Tài liệu được dịch từ bản gốc của [Dave Kerr](https://github.com/dwmkerr/hacker-laws) tại [đây](https://github.com/dwmkerr/hacker-laws)

---

<!-- vim-markdown-toc GFM -->

- [💻📖 hacker-laws](#%f0%9f%92%bb%f0%9f%93%96-hacker-laws)
  - [Giới thiệu](#gi%e1%bb%9bi-thi%e1%bb%87u)
  - [Các định luật](#c%c3%a1c-%c4%91%e1%bb%8bnh-lu%e1%ba%adt)
    - [Luật Amdahl](#lu%e1%ba%adt-amdahl)
    - [Lý thuyết Cửa sổ vỡ](#l%c3%bd-thuy%e1%ba%bft-c%e1%bb%ada-s%e1%bb%95-v%e1%bb%a1)
    - [Luật Brooks](#lu%e1%ba%adt-brooks)
    - [Luật Conway](#lu%e1%ba%adt-conway)
    - [Luật Cunningham](#lu%e1%ba%adt-cunningham)
    - [Số Dunbar](#s%e1%bb%91-dunbar)
    - [Luật Gall](#lu%e1%ba%adt-gall)
    - [Luật Goodhart](#lu%e1%ba%adt-goodhart)
    - [Hanlon's Razor](#hanlons-razor)
    - [Hofstadter's Law](#hofstadters-law)
    - [Hutber's Law](#hutbers-law)
    - [The Hype Cycle & Amara's Law](#the-hype-cycle--amaras-law)
    - [Hyrum's Law (The Law of Implicit Interfaces)](#hyrums-law-the-law-of-implicit-interfaces)
    - [Kernighan's Law](#kernighans-law)
    - [Metcalfe's Law](#metcalfes-law)
    - [Moore's Law](#moores-law)
    - [Murphy's Law / Sod's Law](#murphys-law--sods-law)
    - [Occam's Razor](#occams-razor)
    - [Parkinson's Law](#parkinsons-law)
    - [Premature Optimization Effect](#premature-optimization-effect)
    - [Putt's Law](#putts-law)
    - [Reed's Law](#reeds-law)
    - [The Law of Conservation of Complexity (Tesler's Law)](#the-law-of-conservation-of-complexity-teslers-law)
    - [The Law of Leaky Abstractions](#the-law-of-leaky-abstractions)
    - [The Law of Triviality](#the-law-of-triviality)
    - [The Unix Philosophy](#the-unix-philosophy)
    - [Mô hình Spotify](#m%c3%b4-h%c3%acnh-spotify)
    - [Wadler's Law](#wadlers-law)
    - [Wheaton's Law](#wheatons-law)
  - [Principles](#principles)
    - [The Dilbert Principle](#the-dilbert-principle)
    - [The Pareto Principle (The 80/20 Rule)](#the-pareto-principle-the-8020-rule)
    - [The Peter Principle](#the-peter-principle)
    - [The Robustness Principle (Postel's Law)](#the-robustness-principle-postels-law)
    - [SOLID](#solid)
    - [The Single Responsibility Principle](#the-single-responsibility-principle)
    - [The Open/Closed Principle](#the-openclosed-principle)
    - [The Liskov Substitution Principle](#the-liskov-substitution-principle)
    - [The Interface Segregation Principle](#the-interface-segregation-principle)
    - [The Dependency Inversion Principle](#the-dependency-inversion-principle)
    - [Nguyên tắc DRY](#nguy%c3%aan-t%e1%ba%afc-dry)
    - [Nguyên tắc KISS](#nguy%c3%aan-t%e1%ba%afc-kiss)
    - [YAGNI](#yagni)
    - [The Fallacies of Distributed Computing](#the-fallacies-of-distributed-computing)
  - [Reading List](#reading-list)
  - [Contributing](#contributing)
  - [TODO](#todo)

<!-- vim-markdown-toc -->

## Giới thiệu

Khi nói đến phát triển hay khoa học máy tính, có rất nhiều định luật, lý thuyết, nguyên tắc hay là khuôn mẫu được đem ra thảo luận và áp dụng. Tài liệu này đưa ra một góc nhìn tổng quan về một số luật phổ biến nhất.

❗: Tài liệu này bao gồm phần giải thích của một số định luật, nguyên tắc và khuôn mẫu, nhưng không khẳng định sự ủng hộ cho bất kì cái nào. Việc chúng có nên được áp dụng hay không sẽ luôn là một vấn đề cần tranh luận, và điều đó phụ thuộc rất lớn vào những gì bạn đang làm.

## Các định luật

### Luật Amdahl

[Luật Amdahl xem tại Wikipedia](https://vi.wikipedia.org/wiki/Lu%E1%BA%ADt_Amdahl)

> Luật Amdahl là một công thức thể hiện khả năng tăng tốc mà một tác vụ tính toán có thể đạt được bằng cách tăng lượng tài nguyên của một hệ thống. Nó thường được sử dụng trong tính toán song song và có khả năng dự đoán lợi ích thực tế của việc tăng số lượng bộ xử lý, điều bị giới hạn bởi tính song song của chương trình.

Lấy ví dụ, nếu một chương trình được tạo nên bởi hai phần, trong đó phần A chỉ có thể được thực thi bởi một bộ xử lý đơn lẻ còn phần B có thể được song song hoá thì chúng ta sẽ thấy việc thêm nhiều bộ xử lý cho hệ thống thực thi chương trình đó chỉ mang lại những lợi ích hạn chế. Nó có khả năng cải thiện đáng kể tốc độ của phần B, nhưng tốc độ của phần A sẽ không thay đổi.

Biểu đồ dưới đây minh hoạ cho khả năng cải thiện tốc độ của việc thêm bộ xử lý cho hệ thống thực thi chương trình song song.

<img width="480px" alt="Diagram: Amdahl's Law" src="./images/amdahls_law.png" />

*(Nguồn ảnh: Bởi Daniels220 từ Wikipedia Tiếng Anh, Creative Commons Attribution-Share Alike 3.0 Unported, https://en.wikipedia.org/wiki/File:AmdahlsLaw.svg)*

Như chúng ta có thể thấy, một chương trình được song song hoá 50% sẽ tăng tốc rất hạn chế khi thêm quá 10 đơn vị xử lý, trong khi đó một chương trình có thành phần song song hoá chiếm 95% vẫn cho thấy sự cải thiện về tốc độ khi số lượng đơn vị xử lý vượt quá hàng nghìn.

Khi khoảng thời gian được nhắc tới trong [Luật Moore](#moores-law) chậm lại, hay sự tăng trưởng trong tốc độ của một bộ xử lý đơn lẻ giảm đi, tính song song là chìa khoá của việc cải thiện hiệu năng. Lập trình đồ hoạ (Graphics programming) là một ví dụ tuyệt vời cho điều này. Trong mô hình tính toán dựa trên Shader (Shader based computing) ngày nay, mỗi điểm ảnh hay thành phần đều có thể được kết xuất song song. Vì vậy, việc sử dụng nhiều bộ xử lý có thể cải thiện tốc độ tính toán một cách đáng kể. Đó là lí do vì sao các card đồ họa hiện nay thường có hàng nghìn lõi xử lý (GPUs hay đơn vị Shader).

Xem thêm:

- [Luật Brooks](#brooks-law)
- [Luật Moore](#moores-law)

### Lý thuyết Cửa sổ vỡ

[Lý thuyết Cửa sổ vỡ xem tại Wikipedia](https://en.wikipedia.org/wiki/Broken_windows_theory)

Lý thuyết Cửa sổ vỡ gợi ý rằng những dấu hiệu phạm tội trực quan (hay sự thiếu quan tâm đến một môi trường nào đó) có thể dẫn tới những hành động phạm tội nghiêm trọng hơn (hay sự phá huỷ môi trường nặng nề hơn).

Lý thuyết này đã được áp dụng vào phát triển phần mềm. Nó cho rằng những đoạn mã nguồn kém chất lượng nếu không được sửa chữa kịp thời, sẽ dẫn đến việc bỏ qua (hoặc đánh giá thấp) các nỗ lực cải thiện chất lượng, từ đó dẫn đến nhiều đoạn mã kém chất lượng hơn. Theo thời gian, chất lượng của mã nguồn (và sản phẩm) sẽ bị suy giảm nghiêm trọng.

Xem thêm (Tiếng Anh):

- [The Pragmatic Programming: Software Entropy](https://pragprog.com/the-pragmatic-programmer/extracts/software-entropy)
- [Coding Horror: The Broken Window Theory](https://blog.codinghorror.com/the-broken-window-theory/)
- [OpenSource: Joy of Programming - The Broken Window Theory](https://opensourceforu.com/2011/05/joy-of-programming-broken-window-theory/)

### Luật Brooks

[Luật Brooks xem tại Wikipedia](https://en.wikipedia.org/wiki/Brooks%27s_law)

> Việc thêm người vào một dự án phát triển phần mềm đã chậm tiến độ thường sẽ khiến nó chậm hơn.

Luật này gợi ý rằng trong nhiều trường hợp, việc cố gắng đẩy nhanh một dự án đã bị chậm tiến độ bằng việc thêm nhiều người sẽ khiến việc hoàn thành thậm chí chậm hơn. Dù chính Brooks đã khẳng định rằng luật này đã bị đơn giản hoá quá mức, nhưng luận điểm chung của nó là với thời gian phải bỏ ra cho các nguồn tài nguyên mới và gánh nặng giao tiếp, tốc độ trong ngắn hạn sẽ giảm đi. Hơn nữa, rất nhiều tác vụ có thể không chia nhỏ được (hay dễ dàng phân chia cho các nguồn lực tăng cường), nghĩa là khả năng tăng tốc nói chung cũng thấp hơn.

Có một câu nói phổ biến liên quan tới luật Brooks: "Chín người phụ nữ cũng không thể sinh ra một đứa trẻ trong một tháng", hay một số loại công việc đơn giản là không thể chia nhỏ hay song song hoá được.

Luật này là chủ đề chính của cuốn sách '[The Mythical Man Month](#reading-list)'

Xem thêm:

- [Reading List: The Mythical Man Month](#reading-list)

### Luật Conway

[Luật Conway xem tại Wikipedia](https://en.wikipedia.org/wiki/Conway%27s_law)

Luật Conway gợi ý rằng những giới hạn kỹ thuật của một hệ thống sẽ phản ánh cấu trúc của tổ chức làm ra nó. Luật này thường được đề cập khi xem xét các cải tiến của tổ chức, rằng nếu một tổ chức được cấu thành từ những đơn vị nhỏ lẻ, rời rạc, phần mềm mà nó tạo ra cũng sẽ như vậy. Nếu một tổ chức được xây dựng "theo chiều dọc" và được định hướng xung quanh các tính năng và dịch vụ, hệ thống phần mềm của họ cũng sẽ phản ánh điều này. 

Xem thêm:

- [Mô hình Spotify](#m%c3%b4-h%c3%acnh-spotify)

### Luật Cunningham

[Luật Cunningham xem tại Wikipedia](https://en.wikipedia.org/wiki/Ward_Cunningham#Cunningham's_Law)

> Cách tốt nhất để tìm được câu trả lời đúng trên Internet không phải là đặt câu hỏi, mà là đăng lên một câu trả lời sai.

Theo [Steven McGeady](https://en.wikipedia.org/wiki/Steven_McGeady), [Ward Cunningham](https://en.wikipedia.org/wiki/Ward_Cunningham) đã đưa ra lời khuyên này cho ông vào đầu những năm 80: "Cách tốt nhất để tìm được câu trả lời đúng trên Internet không phải là đặt câu hỏi, mà là đăng lên một câu trả lời sai.". McGeady đặt tên cho luật này là ***Luật Cunningham***, tuy nhiên Cunningham phủ nhận điều này và gọi đây là một "trích dẫn sai". Mặc dù ban đầu nó được dùng để nói về tương tác trên Usenet, luật này cũng được sử dụng để mô tả cách mà các cộng đồng trực tuyến khác hoạt động (ví dụ: Wikipedia, Reddit, Twitter, Facebook).

Xem thêm:

- [XKCD 386: "Duty Calls"](https://xkcd.com/386/)

### Số Dunbar

[Số Dunbar xem tại Wikipedia](https://en.wikipedia.org/wiki/Dunbar%27s_number)

Số Dunbar được đề xuất như là một giới hạn nhận thức để chỉ số lượng người tối đa mà một cá nhân có thể duy trì mối quan hệ xã hội ổn định (những mối quan hệ mà trong đó một người biết những người còn lại và mối liên hệ của họ với những người khác). Dù có một vài bất đồng trong con số chính xác, nhưng Dunbar cho rằng mỗi người chỉ có thể thoải mái duy trì 150 quan hệ ổn định. Ông ấy đặt con số này trong một hoàn cảnh xã hội cụ thể: "Đó là số người mà bạn có thể thoải mái làm với họ một ly khi vô tình gặp nhau trong quán bar". Ước tính về con số cụ thể thường rơi vào giữa 100 và 250.

Cũng giống như những mối quan hệ ổn định giữa người với người, mối quan hệ của một nhà phát triển với mã nguồn của họ cũng đòi hỏi nỗ lực để duy trì. Khi phải đối mặt với những dự án lớn và phức tạp, hay khi phải làm chủ quá nhiều dự án, chúng ta thường dựa vào các quy ước, luật lệ và các quy trình đã được mô hình hóa để mở rộng. Số Dunbar không chỉ quan trọng và cần được ghi nhớ khi phát triển tổ chức, mà còn áp dụng khi đặt ra giới hạn cho nỗ lực của đội nhóm hay khi đưa ra quyết định rằng một hệ thống có nên đầu tư vào các công cụ để hỗ trợ việc mô hình hóa và tự động hóa các công việc hậu cần hay không. Đặt con số này vào môi trường kĩ thuật, đó là số lượng dự án (hoặc các mức độ phức tạp của một dự án) mà bạn có thể tự tin tham gia vào khi được yêu cầu hỗ trợ.

Xem thêm:

- [Luật Conway](#lu%e1%ba%adt-conway)

### Luật Gall

[Luật Gall xem tại Wikipedia](https://en.wikipedia.org/wiki/John_Gall_(author)#Gall's_law)

> Một hệ thống phức tạp hoạt động được luôn luôn phát triển từ một hệ thống đơn giản hoạt động được. Một hệ thống được thiết kế phức tạp từ đầu sẽ không bao giờ hoạt động dù có cố vá víu như thế nào. Bạn phải bắt đầu với một hệ thống đơn giản, hoạt động được trước.
> ([John Gall](https://en.wikipedia.org/wiki/John_Gall_(author)))

Luật Gall chỉ ra rằng việc cố gắng _thiết kế_ những hệ thống cực kì phức tạp thường dễ dẫn tới thất bại. Những hệ thống như vậy thường ít khi được xây dựng phức tạp từ đầu, thay vào đó là được phát triển từ nhiều hệ thống đơn giản hơn.

Ví dụ kinh điển cho luật này chính là mạng world-wide-web (WWW). Ở trạng thái hiện tại, nó là một hệ thống cực kì phức tạp. Tuy nhiên, ban đầu nó chỉ được định nghĩa như là một cách thức đơn giản để chia sẻ nội dung giữa các tổ chức học thuật. Nó đã hoàn thành mục tiêu đó rất thành công và phát triển để trở nên phức tạp hơn theo thời gian.
Xem thêm:

- [Nguyên tắc KISS](#nguy%c3%aan-t%e1%ba%afc-kiss)

### Luật Goodhart

[Luật Goodhart xem tại Wikipedia](https://en.wikipedia.org/wiki/Goodhart's_law)
> Bất kỳ chỉ số thống kê nào cũng có xu hướng sụp đổ một khi áp lực được đặt vào nó cho mục đích kiểm soát.
> 
> _Charles Goodhart_

Nói cách khác:

> Khi một chỉ số trở thành mục tiêu, nó không còn là một chỉ số tốt nữa.
>
> _Marilyn Strathern_

Luật này chỉ ra rằng việc tối ưu hóa theo chỉ số có thể dẫn tới sự giảm giá trị của chính chỉ số đó. 
Tập hợp các chỉ tiêu bị lựa chọn quá mức ([KPIs](https://en.wikipedia.org/wiki/Performance_indicator)) một cách mù quáng khi áp dụng vào một quá trình thường dẫn tới những hiệu ứng méo mó. Người ta có xu hướng tối ưu cục bộ bằng cách "thưởng nóng" hệ thống để thỏa mãn một tập chỉ số nhất định thay vì tập trung vào kết quả toàn diện của hành động của họ.

Ví dụ thực tế:
- Các kiểm thử không xác minh (assert-free tests) chỉ thoả mãn yêu cầu về độ bao phủ mã, mặc dù mục đích của nó là tạo ra một phần mềm được kiểm thử tốt.
- Hiệu suất của nhà phát triển nếu được đo bằng số lượng dòng mã sẽ dẫn tới hệ thống mã nguồn cồng kềnh không cần thiết.

Xem thêm:
- [Goodhart’s Law: How Measuring The Wrong Things Drive Immoral Behaviour](https://coffeeandjunk.com/goodharts-campbells-law/)
- [Dilbert on bug-free software](https://dilbert.com/strip/1995-11-13)

### Hanlon's Razor

[Hanlon's Razor on Wikipedia](https://en.wikipedia.org/wiki/Hanlon%27s_razor)

> Never attribute to malice that which is adequately explained by stupidity.
>
> Robert J. Hanlon

This principle suggests that actions resulting in a negative outcome were not a result of ill will. Instead the negative outcome is more likely attributed to those actions and/or the impact being not fully understood.

### Hofstadter's Law

[Hofstadter's Law on Wikipedia](https://en.wikipedia.org/wiki/Hofstadter%27s_law)

> It always takes longer than you expect, even when you take into account Hofstadter's Law.
>
> (Douglas Hofstadter)

You might hear this law referred to when looking at estimates for how long something will take. It seems a truism in software development that we tend to not be very good at accurately estimating how long something will take to deliver.

This is from the book '[Gödel, Escher, Bach: An Eternal Golden Braid](#reading-list)'.

See also:

- [Reading List: Gödel, Escher, Bach: An Eternal Golden Braid](#reading-list)

### Hutber's Law

[Hutber's Law on Wikipedia](https://en.wikipedia.org/wiki/Hutber%27s_law)

> Improvement means deterioration.
>
> ([Patrick Hutber](https://en.wikipedia.org/wiki/Patrick_Hutber))

This law suggests that improvements to a system will lead to deterioration in other parts, or it will hide other deterioration, leading overall to a degradation from the current state of the system.

For example, a decrease in response latency for a particular end-point could cause increased throughput and capacity issues further along in a request flow, affecting an entirely different sub-system.

### The Hype Cycle & Amara's Law

[The Hype Cycle on Wikipedia](https://en.wikipedia.org/wiki/Hype_cycle)

> We tend to overestimate the effect of a technology in the short run and underestimate the effect in the long run.
>
> (Roy Amara)

The Hype Cycle is a visual representation of the excitement and development of technology over time, originally produced by Gartner. It is best shown with a visual:

![The Hype Cycle](./images/gartner_hype_cycle.png)

*(Image Reference: By Jeremykemp at English Wikipedia, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=10547051)*

In short, this cycle suggests that there is typically a burst of excitement around new technology and its potential impact. Teams often jump into these technologies quickly, and sometimes find themselves disappointed with the results. This might be because the technology is not yet mature enough, or real-world applications are not yet fully realised. After a certain amount of time, the capabilities of the technology increase and practical opportunities to use it increase, and teams can finally become productive. Roy Amara's quote sums this up most succinctly - "We tend to overestimate the effect of a technology in the short run and underestimate in the long run".

### Hyrum's Law (The Law of Implicit Interfaces)

[Hyrum's Law Online](http://www.hyrumslaw.com/)

> With a sufficient number of users of an API,
> it does not matter what you promise in the contract:
> all observable behaviours of your system
> will be depended on by somebody.
>
> (Hyrum Wright)

Hyrum's Law states that when you have a _large enough number of consumers_ of an API, all behaviours of the API (even those not defined as part of a public contract) will eventually come to be depended on by someone. A trivial example may be non-functional elements such as the response time of an API. A more subtle example might be consumers who are relying on applying a regex to an error message to determine the *type* of error of an API. Even if the public contract of the API states nothing about the contents of the message, indicating users should use an associated error code, _some_ users may use the message, and changing the message essentially breaks the API for those users.

See also:

- [The Law of Leaky Abstractions](#the-law-of-leaky-abstractions)
- [XKCD 1172](https://xkcd.com/1172/)

### Kernighan's Law

> Debugging is twice as hard as writing the code in the first place. Therefore, if you write the code as cleverly as possible, you are, by definition, not smart enough to debug it.
>
> (Brian Kernighan)

Kernighan's Law is named for [Brian Kernighan](https://en.wikipedia.org/wiki/Brian_Kernighan) and derived from a quote from Kernighan and Plauger's book [The Elements of Programming Style](https://en.wikipedia.org/wiki/The_Elements_of_Programming_Style):

> Everyone knows that debugging is twice as hard as writing a program in the first place. So if you're as clever as you can be when you write it, how will you ever debug it?

While hyperbolic, Kernighan's Law makes the argument that simple code is to be preferred over complex code, because debugging any issues that arise in complex code may be costly or even infeasible.

See also:

- [The KISS Principle](#the-kiss-principle)
- [The Unix Philosophy](#the-unix-philosophy)
- [Occam's Razor](#occams-razor)

### Metcalfe's Law

[Metcalfe's Law on Wikipedia](https://en.wikipedia.org/wiki/Metcalfe's_law)

> In network theory, the value of a system grows as approximately the square of the number of users of the system.

This law is based on the number of possible pairwise connections within a system and is closely related to [Reed's Law](#reeds-law). Odlyzko and others have argued that both Reed's Law and Metcalfe's Law overstate the value of the system by not accounting for the limits of human cognition on network effects; see [Dunbar's Number](#dunbars-number).

See also:
- [Reed's Law](#reeds-law)
- [Dunbar's Number](#dunbars-number)

### Moore's Law

[Moore's Law on Wikipedia](https://en.wikipedia.org/wiki/Moore%27s_law)

> The number of transistors in an integrated circuit doubles approximately every two years.

Often used to illustrate the sheer speed at which semiconductor and chip technology has improved, Moore's prediction has proven to be highly accurate over from the 1970s to the late 2000s. In more recent years, the trend has changed slightly, partly due to [physical limitations on the degree to which components can be miniaturised](https://en.wikipedia.org/wiki/Quantum_tunnelling). However, advancements in parallelisation, and potentially revolutionary changes in semiconductor technology and quantum computing may mean that Moore's Law could continue to hold true for decades to come.

### Murphy's Law / Sod's Law

[Murphy's Law on Wikipedia](https://en.wikipedia.org/wiki/Murphy%27s_law)

> Anything that can go wrong will go wrong.

Related to [Edward A. Murphy, Jr](https://en.wikipedia.org/wiki/Edward_A._Murphy_Jr.) _Murphy's Law_ states that if a thing can go wrong, it will go wrong.

This is a common adage among developers. Sometimes the unexpected happens when developing, testing or even in production. This can also be related to the (more common in British English) _Sod's Law_:

> If something can go wrong, it will, at the worst possible time.

These 'laws' are generally used in a comic sense. However, phenomena such as [_Confirmation Bias_](#TODO) and [_Selection Bias_](#TODO) can lead people to perhaps over-emphasise these laws (the majority of times when things work, they go unnoticed, failures however are more noticeable and draw more discussion).

See Also:

- [Confirmation Bias](#TODO)
- [Selection Bias](#TODO)

### Occam's Razor

[Occam's Razor on Wikipedia](https://en.wikipedia.org/wiki/Occam's_razor)

> Entities should not be multiplied without necessity.
>
> William of Ockham

Occam's razor says that among several possible solutions, the most likely solution is the one with the least number of concepts and assumptions. This solution is the simplest and solves only the given problem, without introducing accidental complexity and possible negative consequences.

See also:

- [YAGNI](#yagni)
- [No Silver Bullet: Accidental Complexity and Essential Complexity](https://en.wikipedia.org/wiki/No_Silver_Bullet)

Example:

- [Lean Software Development: Eliminate Waste](https://en.wikipedia.org/wiki/Lean_software_development#Eliminate_waste)

### Parkinson's Law

[Parkinson's Law on Wikipedia](https://en.wikipedia.org/wiki/Parkinson%27s_law)

> Work expands so as to fill the time available for its completion.

In its original context, this Law was based on studies of bureaucracies. It may be pessimistically applied to software development initiatives, the theory being that teams will be inefficient until deadlines near, then rush to complete work by the deadline, thus making the actual deadline somewhat arbitrary.

If this law were combined with [Hofstadter's Law](#hofstadters-law), an even more pessimistic viewpoint is reached - work will expand to fill the time available for its completion and *still take longer than expected*.

See also:

- [Hofstadter's Law](#hofstadters-law)

### Premature Optimization Effect

[Premature Optimization on WikiWikiWeb](http://wiki.c2.com/?PrematureOptimization)

> Premature optimization is the root of all evil.
>
> [(Donald Knuth)](https://twitter.com/realdonaldknuth?lang=en)

In Donald Knuth's paper [Structured Programming With Go To Statements](http://wiki.c2.com/?StructuredProgrammingWithGoToStatements), he wrote: "Programmers waste enormous amounts of time thinking about, or worrying about, the speed of noncritical parts of their programs, and these attempts at efficiency actually have a strong negative impact when debugging and maintenance are considered. We should forget about small efficiencies, say about 97% of the time: **premature optimization is the root of all evil**. Yet we should not pass up our opportunities in that critical 3%."

However, _Premature Optimization_ can be defined (in less loaded terms) as optimizing before we know that we need to.

### Putt's Law

[Putt's Law on Wikipedia](https://en.wikipedia.org/wiki/Putt%27s_Law_and_the_Successful_Technocrat)

> Technology is dominated by two types of people, those who understand what they do not manage and those who manage what they do not understand.

Putt's Law is often followed by Putt's Corollary:

> Every technical hierarchy, in time, develops a competence inversion.

These statements suggest that due to various selection criteria and trends in how groups organise, there will be a number of skilled people at working levels of a technical organisations, and a number of people in managerial roles who are not aware of the complexities and challenges of the work they are managing. This can be due to phenomena such as [The Peter Principle](#the-peter-principle) or [The Dilbert Principle](#the-dilbert-principle).

However, it should be stressed that Laws such as this are vast generalisations and may apply to _some_ types of organisations, and not apply to others.

See also:

- [The Peter Principle](#the-peter-principle)
- [The Dilbert Principle](#the-dilbert-principle)


### Reed's Law

[Reed's Law on Wikipedia](https://en.wikipedia.org/wiki/Reed's_law)

> The utility of large networks, particularly social networks, scales exponentially with the size of the network.

This law is based on graph theory, where the utility scales as the number of possible sub-groups, which is faster than the number of participants or the number of possible pairwise connections. Odlyzko and others have argued that Reed's Law overstates the utility of the system by not accounting for the limits of human cognition on network effects; see [Dunbar's Number](#dunbars-number).

See also:
- [Metcalfe's Law](#metcalfes-law)
- [Dunbar's Number](#dunbars-number)

### The Law of Conservation of Complexity (Tesler's Law)

[The Law of Conservation of Complexity on Wikipedia](https://en.wikipedia.org/wiki/Law_of_conservation_of_complexity)

This law states that there is a certain amount of complexity in a system which cannot be reduced.

Some complexity in a system is 'inadvertent'. It is a consequence of poor structure, mistakes, or just bad modeling of a problem to solve. Inadvertent complexity can be reduced (or eliminated). However, some complexity is 'intrinsic' as a consequence of the complexity inherent in the problem being solved. This complexity can be moved, but not eliminated.

One interesting element to this law is the suggestion that even by simplifying the entire system, the intrinsic complexity is not reduced, it is _moved to the user_, who must behave in a more complex way.

### The Law of Leaky Abstractions

[The Law of Leaky Abstractions on Joel on Software](https://www.joelonsoftware.com/2002/11/11/the-law-of-leaky-abstractions/)

> All non-trivial abstractions, to some degree, are leaky.
>
> ([Joel Spolsky](https://twitter.com/spolsky))

This law states that abstractions, which are generally used in computing to simplify working with complicated systems, will in certain situations 'leak' elements of the underlying system, this making the abstraction behave in an unexpected way.

An example might be loading a file and reading its contents. The file system APIs are an _abstraction_ of the lower level kernel systems, which are themselves an abstraction over the physical processes relating to changing data on a magnetic platter (or flash memory for an SSD). In most cases, the abstraction of treating a file like a stream of binary data will work. However, for a magnetic drive, reading data sequentially will be *significantly* faster than random access (due to increased overhead of page faults), but for an SSD drive, this overhead will not be present. Underlying details will need to be understood to deal with this case (for example, database index files are structured to reduce the overhead of random access), the abstraction 'leaks' implementation details the developer may need to be aware of.

The example above can become more complex when _more_ abstractions are introduced. The Linux operating system allows files to be accessed over a network but represented locally as 'normal' files. This abstraction will 'leak' if there are network failures. If a developer treats these files as 'normal' files, without considering the fact that they may be subject to network latency and failures, the solutions will be buggy.

The article describing the law suggests that an over-reliance on abstractions, combined with a poor understanding of the underlying processes, actually makes dealing with the problem at hand _more_ complex in some cases.

See also:

- [Hyrum's Law](#hyrums-law-the-law-of-implicit-interfaces)

Real-world examples:

- [Photoshop Slow Startup](https://forums.adobe.com/thread/376152) - an issue I encountered in the past. Photoshop would be slow to startup, sometimes taking minutes. It seems the issue was that on startup it reads some information about the current default printer. However, if that printer is actually a network printer, this could take an extremely long time. The _abstraction_ of a network printer being presented to the system similar to a local printer caused an issue for users in poor connectivity situations.

### The Law of Triviality

[The Law of Triviality on Wikipedia](https://en.wikipedia.org/wiki/Law_of_triviality)

This law suggests that groups will give far more time and attention to trivial or cosmetic issues rather than serious and substantial ones.

The common fictional example used is that of a committee approving plans for nuclear power plant, who spend the majority of their time discussing the structure of the bike shed, rather than the far more important design for the power plant itself. It can be difficult to give valuable input on discussions about very large, complex topics without a high degree of subject matter expertise or preparation. However, people want to be seen to be contributing valuable input. Hence a tendency to focus too much time on small details, which can be reasoned about easily, but are not necessarily of particular importance.

The fictional example above led to the usage of the term 'Bike Shedding' as an expression for wasting time on trivial details. An alternative term is 'Yak Shaving'.

### The Unix Philosophy

[The Unix Philosophy on Wikipedia](https://en.wikipedia.org/wiki/Unix_philosophy)

The Unix Philosophy is that software components should be small, and focused on doing one specific thing well. This can make it easier to build systems by composing together small, simple, well-defined units, rather than using large, complex, multi-purpose programs.

Modern practices like 'Microservice Architecture' can be thought of as an application of this law, where services are small, focused and do one specific thing, allowing complex behaviour to be composed of simple building blocks.

### Mô hình Spotify

[Mô hình Spotify xem tại Spotify Labs](https://labs.spotify.com/2014/03/27/spotify-engineering-culture-part-1/)

Mô hình Spotify là một cách tiếp cận trong việc xây dựng cấu trúc cho đội nhóm và tổ chức, được phổ biến bởi 'Spotify'. Trong mô hình này, các đội nhóm được tập trung xây dựng xung quanh tính năng thay vì công nghệ. 

Mô hình Spotify cũng phổ biến các khái niệm về **Tribes**, **Guilds** hay **Chapters**, là những thành phần khác trong cấu trúc tổ chức của họ.

### Wadler's Law

[Wadler's Law on wiki.haskell.org](https://wiki.haskell.org/Wadler's_Law)

> In any language design, the total time spent discussing a feature in this list is proportional to two raised to the power of its position.
>
> 0. Semantics
> 1. Syntax
> 2. Lexical syntax
> 3. Lexical syntax of comments
>
> (In short, for every hour spent on semantics, 8 hours will be spent on the syntax of comments).

Similar to [The Law of Triviality](#the-law-of-triviality), Wadler's Law states what when designing a language, the amount of time spent on language structures is disproportionately high in comparison to the importance of those features.

See also:

- [The Law of Triviality](#the-law-of-triviality)

### Wheaton's Law

[The Link](http://www.wheatonslaw.com/)

[The Official Day](https://dontbeadickday.com/)

> Don't be a dick.
>
> _Wil Wheaton_

Coined by Wil Wheaton (Star Trek: The Next Generation, The Big Bang Theory), this simple, concise, and powerful law aims for an increase in harmony and respect within a professional organization. It can be applied when speaking with coworkers, performing code reviews, countering other points of view, critiquing, and in general, most professional interactions humans have with each other.

## Principles

Principles are generally more likely to be guidelines relating to design.

### The Dilbert Principle

[The Dilbert Principle on Wikipedia](https://en.wikipedia.org/wiki/Dilbert_principle)

> Companies tend to systematically promote incompetent employees to management to get them out of the workflow.
>
> _Scott Adams_

A management concept developed by Scott Adams (creator of the Dilbert comic strip), the Dilbert Principle is inspired by [The Peter Principle](#the-peter-principle). Under the Dilbert Principle, employees who were never competent are promoted to management in order to limit the damage they can do. Adams first explained the principle in a 1995 Wall Street Journal article, and expanded upon it in his 1996 business book, [The Dilbert Principle](#reading-list).

See Also:

- [The Peter Principle](#the-peter-principle)
- [Putt's Law](#putts-law)

### The Pareto Principle (The 80/20 Rule)

[The Pareto Principle on Wikipedia](https://en.wikipedia.org/wiki/Pareto_principle)

> Most things in life are not distributed evenly.

The Pareto Principle suggests that in some cases, the majority of results come from a minority of inputs:

- 80% of a certain piece of software can be written in 20% of the total allocated time (conversely, the hardest 20% of the code takes 80% of the time)
- 20% of the effort produces 80% of the result
- 20% of the work creates 80% of the revenue
- 20% of the bugs cause 80% of the crashes
- 20% of the features cause 80% of the usage

In the 1940s American-Romanian engineer Dr. Joseph Juran, who is widely credited with being the father of quality control, [began to apply the Pareto principle to quality issues](https://en.wikipedia.org/wiki/Joseph_M._Juran).

This principle is also known as: The 80/20 Rule, The Law of the Vital Few and The Principle of Factor Sparsity.

Real-world examples:

- In 2002 Microsoft reported that by fixing the top 20% of the most-reported bugs, 80% of the related errors and crashes in windows and office would become eliminated ([Reference](https://www.crn.com/news/security/18821726/microsofts-ceo-80-20-rule-applies-to-bugs-not-just-features.htm)).

### The Peter Principle

[The Peter Principle on Wikipedia](https://en.wikipedia.org/wiki/Peter_principle)

> People in a hierarchy tend to rise to their "level of incompetence".
>
> _Laurence J. Peter_

A management concept developed by Laurence J. Peter, the Peter Principle observes that people who are good at their jobs are promoted, until they reach a level where they are no longer successful (their "level of incompetence". At this point, as they are more senior, they are less likely to be removed from the organisation (unless they perform spectacularly badly) and will continue to reside in a role which they have few intrinsic skills at, as their original skills which made them successful are not necessarily the skills required for their new jobs.

This is of particular interest to engineers - who initial start out in deeply technical roles, but often have a career path which leads to _managing_ other engineers - which requires a fundamentally different skills-set.

See Also:

- [The Dilbert Principle](#the-dilbert-principle)
- [Putt's Law](#putts-law)

### The Robustness Principle (Postel's Law)

[The Robustness Principle on Wikipedia](https://en.wikipedia.org/wiki/Robustness_principle)

> Be conservative in what you do, be liberal in what you accept from others.

Often applied in server application development, this principle states that what you send to others should be as minimal and conformant as possible, but you should be aim to allow non-conformant input if it can be processed.

The goal of this principle is to build systems which are robust, as they can handle poorly formed input if the intent can still be understood. However, there are potentially security implications of accepting malformed input, particularly if the processing of such input is not well tested.

Allowing non-conformant input, in time, may undermine the ability of protocols to evolve as implementors will eventually rely on this liberality to build their features.

See Also:

- [Hyrum's Law](#hyrums-law-the-law-of-implicit-interfaces)


### SOLID

This is an acronym, which refers to:

* S: [The Single Responsibility Principle](#the-single-responsibility-principle)
* O: [The Open/Closed Principle](#the-openclosed-principle)
* L: [The Liskov Substitution Principle](#the-liskov-substitution-principle)
* I: [The Interface Segregation Principle](#the-interface-segregation-principle)
* D: [The Dependency Inversion Principle](#the-dependency-inversion-principle)

These are key principles in [Object-Oriented Programming](#todo). Design principles such as these should be able to aid developers build more maintainable systems.

### The Single Responsibility Principle

[The Single Responsibility Principle on Wikipedia](https://en.wikipedia.org/wiki/Single_responsibility_principle)

> Every module or class should have a single responsibility only.

The first of the '[SOLID](#solid)' principles. This principle suggests that modules or classes should do one thing and one thing only. In more practical terms, this means that a single, small change to a feature of a program should require a change in one component only. For example, changing how a password is validated for complexity should require a change in only one part of the program.

Theoretically, this should make the code more robust, and easier to change. Knowing that a component which is being changed has a single responsibility only means that _testing_ that change should be easier. Using the earlier example, changing the password complexity component should only be able to affect the features which relate to password complexity. It can be much more difficult to reason about the impact of a change to a component which has many responsibilities.

See also:

- [Object-Oriented Programming](#todo)
- [SOLID](#solid)

### The Open/Closed Principle

[The Open/Closed Principle on Wikipedia](https://en.wikipedia.org/wiki/Open%E2%80%93closed_principle)

> Entities should be open for extension and closed for modification.

The second of the '[SOLID](#solid)' principles. This principle states that entities (which could be classes, modules, functions and so on) should be able to have their behaviour _extended_, but that their _existing_ behaviour should not be able to be modified.

As a hypothetical example, imagine a module which is able to turn a Markdown document into HTML. If the module could be extended to handle a newly proposed markdown feature, without modifying the module internals, then it would be open for extension. If the module could _not_ be modified by a consumer so that how existing Markdown features are handled, then it would be _closed_ for modification.

This principle has particular relevance for object-oriented programming, where we may design objects to be easily extended, but would avoid designing objects which can have their existing behaviour changed in unexpected ways.

See also:

- [Object-Oriented Programming](#todo)
- [SOLID](#solid)

### The Liskov Substitution Principle

[The Liskov Substitution Principle on Wikipedia](https://en.wikipedia.org/wiki/Liskov_substitution_principle)

> It should be possible to replace a type with a subtype, without breaking the system.

The third of the '[SOLID](#solid)' principles. This principle states that if a component relies on a type, then it should be able to use subtypes of that type, without the system failing or having to know the details of what that subtype is.

As an example, imagine we have a method which reads an XML document from a structure which represents a file. If the method uses a base type 'file', then anything which derives from 'file' should be able to be used in the function. If 'file' supports seeking in reverse, and the XML parser uses that function, but the derived type 'network file' fails when reverse seeking is attempted, then the 'network file' would be violating the principle.

This principle has particular relevance for object-oriented programming, where type hierarchies must be modeled carefully to avoid confusing users of a system.

See also:

- [Object-Oriented Programming](#todo)
- [SOLID](#solid)

### The Interface Segregation Principle

[The Interface Segregation Principle on Wikipedia](https://en.wikipedia.org/wiki/Interface_segregation_principle)

> No client should be forced to depend on methods it does not use.

The fourth of the '[SOLID](#solid)' principles. This principle states that consumers of a component should not depend on functions of that component which it doesn't actually use.

As an example, imagine we have a method which reads an XML document from a structure which represents a file. It only needs to read bytes, move forwards or move backwards in the file. If this method needs to be updated because an unrelated feature of the file structure changes (such as an update to the permissions model used to represent file security), then the principle has been invalidated. It would be better for the file to implement a 'seekable-stream' interface, and for the XML reader to use that.

This principle has particular relevance for object-oriented programming, where interfaces, hierarchies and abstract types are used to [minimise the coupling](#todo) between different components. [Duck typing](#todo) is a methodology which enforces this principle by eliminating explicit interfaces.

See also:

- [Object-Oriented Programming](#todo)
- [SOLID](#solid)
- [Duck Typing](#todo)
- [Decoupling](#todo)

### The Dependency Inversion Principle

[The Dependency Inversion Principle on Wikipedia](https://en.wikipedia.org/wiki/Dependency_inversion_principle)

> High-level modules should not be dependent on low-level implementations.

The fifth of the '[SOLID](#solid)' principles. This principle states that higher level orchestrating components should not have to know the details of their dependencies.

As an example, imagine we have a program which read metadata from a website. We would assume that the main component would have to know about a component to download the webpage content, then a component which can read the metadata. If we were to take dependency inversion into account, the main component would depend only on an abstract component which can fetch byte data, and then an abstract component which would be able to read metadata from a byte stream. The main component would not know about TCP/IP, HTTP, HTML, etc.

This principle is complex, as it can seem to 'invert' the expected dependencies of a system (hence the name). In practice, it also means that a separate orchestrating component must ensure the correct implementations of abstract types are used (e.g. in the previous example, _something_ must still provide the metadata reader component a HTTP file downloader and HTML meta tag reader). This then touches on patterns such as [Inversion of Control](#todo) and [Dependency Injection](#todo).

See also:

- [Object-Oriented Programming](#todo)
- [SOLID](#solid)
- [Inversion of Control](#todo)
- [Dependency Injection](#todo)

### Nguyên tắc DRY

[Nguyên tắc DRY xem tại Wikipedia](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)

> Trong một hệ thống, mỗi thành phần phải có một mô tả duy nhất, không mơ hồ và chắc chắn.

DRY là viết tắt của _Don't Repeat Yourself_, _Đừng Lặp Lại Chính Bạn_. Mục tiêu của nguyên tắc này là để giúp nhà phát triển giảm việc lặp lại mã nguồn và giữ thông tin ở một nơi duy nhất, nguyên tắc này đã được trích dẫn vào năm 1999 bởi Andrew Hunt và Dave Thomas trong cuốn [The Pragmatic Developer](https://en.wikipedia.org/wiki/The_Pragmatic_Programmer)

> Trái ngược với DRY là _WET_ (Write Everything Twice, Viết Mọi Thứ Hai Lần hay We Enjoy Typing, Chúng Tôi Thích Gõ).

Trong thực hành, nếu bạn có phần thông tin giống nhau trong hai (hoặc nhiều) nơi khác nhau, bạn có thể sử dụng DRY để hợp nhất chúng thành một và sử dụng nó bất kỳ nơi nào bạn muốn/cần.

Xem thêm:

- [The Pragmatic Developer](https://en.wikipedia.org/wiki/The_Pragmatic_Programmer)

### Nguyên tắc KISS

[KISS xem tại Wikipedia](https://en.wikipedia.org/wiki/KISS_principle)

> Keep it simple, stupid

Nguyên tắc KISS chỉ ra rằng hầu hết các hệ thống hoạt động tốt nhất nếu nó được giữ đơn giản thay vì bị phức tạp hoá; vì vậy, tính đơn giản nên là một mục tiêu chính trong thiết kế, và sự phức tạp không cần thiết nên được tránh. Bắt nguồn từ Hải quân Mỹ (U.S Navy) năm 1960, nguyên tắc này đã được gắn liền với tên tuổi của kỹ sư hàng không Kelly Johnson.

Nguyên tắc này được minh họa rõ nhất qua câu chuyện Johnson trao cho một nhóm kỹ sư thiết kế một số ít các công cụ, với thách thức là máy bay phản lực mà họ đang thiết kế phải có khả năng sửa chữa được bởi một thợ máy trung bình trong điều kiện chiến đấu mà chỉ bằng những công cụ này. Do đó, "stupid" chỉ mối quan hệ giữa cách mọi thứ bị phá vỡ và sự phức tạp của các công cụ có sẵn để sửa chữa chúng, chứ không phải với khả năng của các kỹ sư.

Xem thêm::

- [Gall's Law](#galls-law)

### YAGNI

[YAGNI on Wikipedia](https://en.wikipedia.org/wiki/You_ain%27t_gonna_need_it)

Đây là từ viết tắt của _**Y**ou **A**ren't **G**onna **N**eed **I**t_. (Bạn sẽ không cần nó)

> Hãy luôn thực hiện mọi thứ khi bạn thực sự cần chúng, chứ không phải khi bạn mới chỉ thấy trước rằng bạn cần chúng.
> (Always implement things when you actually need them, never when you just foresee that you need them.)
> ([Ron Jeffries](https://twitter.com/RonJeffries)) (Đồng sáng lập XP và tác giả của cuốn sách "Extreme Programming Installed")

Nguyên tắc _Extreme Programming_ (XP) này gợi ý rằng các nhà phát triển chỉ nên thực hiện chức năng cần thiết cho các yêu cầu ngay trước mắt và tránh các nỗ lực dự đoán tương lai bằng việc triển khai chức năng có thể cần thiết sau này.

Tuân thủ nguyên tắc này sẽ làm giảm số lượng đoạn mã không được sử dụng trong toàn bộ mã nguồn cũng như tránh lãng phí thời gian và công sức cho các chức năng không mang lại giá trị.

Xem thêm:

- [Reading List: Extreme Programming Installed](#reading-list)

### Sự ảo tưởng của Điện toán Phân tán

[Từ gốc `The Fallacies of Distributed Computing` xem tại Wikipedia](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing)

Còn được gọi là _Sự ảo tưởng của Mạng Điện toán_, Fallacies là một danh sách các ảo tưởng (hay niềm tin) về điện toán phân tán, có thể dẫn đến các thất bại trong việc phát triển phần mêmf. Các ảo tưởng này là:

- Mạng luôn tin cậy
- Độ trễ bằng 0
- Băng thông vô hạn
- Mạng luôn an toàn
- Cấu trúc mạng (topology) không thay đổi
- Có một quản trị viên
- Chi phí vận truyền bằng 0
- Mạng là đồng nhất

Bốn ý đầu tiên được liệt kê bởi [Bill Joy](https://en.wikipedia.org/wiki/Bill_Joy) and [Tom Lyon](https://twitter.com/aka_pugs) khoảng năm 1991 và được phân loại thành "Fallacies of Networked Computing" lần đầu bởi [James Gosling](https://en.wikipedia.org/wiki/James_Gosling). [L. Peter Deutsch](https://en.wikipedia.org/wiki/L._Peter_Deutsch) đã thêm vào danh sách các ý số 5, 6 và 7. Cuối thập niên 90 Gosling đã thêm vào ý số 8.

Nhóm được truyền cảm hứng bởi những gì đã xảy ra trong khoảng thời gian làm việc tại [Sun Microsystems](https://en.wikipedia.org/wiki/Sun_Microsystems).

Những ảo tưởng nên được xem xét một cách cẩn thận khi thiết kế chương trình; việc tin vào bất kỳ các ảo tưởng nào ở đây đều có thể dẫn tới sự thiếu sót logic, mà không giải quyết được vấn đề thực tế và sự phức tạp của các hệ thống phân tán.

Xem thêm:

- [Foraging for the Fallacies of Distributed Computing (Part 1) - Vaidehi Joshi
 trên Medium](https://medium.com/baseds/foraging-for-the-fallacies-of-distributed-computing-part-1-1b35c3b85b53)
- [Deutsch's Fallacies, 10 Years After](http://java.sys-con.com/node/38665)

## Reading List

If you have found these concepts interesting, you may enjoy the following books.

- [Extreme Programming Installed - Ron Jeffries, Ann Anderson, Chet Hendrikson](https://www.goodreads.com/en/book/show/67834) - Covers the core principles of Extreme Programming.
- [The Mythical Man Month - Frederick P. Brooks Jr.](https://www.goodreads.com/book/show/13629.The_Mythical_Man_Month) - A classic volume on software engineering. [Brooks' Law](#brooks-law) is a central theme of the book.
- [Gödel, Escher, Bach: An Eternal Golden Braid - Douglas R. Hofstadter.](https://www.goodreads.com/book/show/24113.G_del_Escher_Bach) - This book is difficult to classify. [Hofstadter's Law](#hofstadters-law) is from the book.
- [The Dilbert Principle - Scott Adams](https://www.goodreads.com/book/show/85574.The_Dilbert_Principle) - A comic look at corporate America, from the author who created the [Dilbert Principle](#the-dilbert-principle).
- [The Peter Principle - Lawrence J. Peter](https://www.goodreads.com/book/show/890728.The_Peter_Principle) - Another comic look at the challenges of larger organisations and people management, the source of [The Peter Principle](#the-peter-principle).

## Contributing

Please do contribute! [Raise an issue](https://github.com/dwmkerr/hacker-laws/issues/new) if you'd like to suggest an addition or change, or [Open a pull request](https://github.com/dwmkerr/hacker-laws/compare) to propose your own changes.

Please be sure to read the [Contributing Guidelines](./.github/contributing.md) for requirements on text, style and so on. Please be aware of the [Code of Conduct](./.github/CODE_OF_CONDUCT.md) when engaging in discussions on the project.

## TODO

Hi! If you land here, you've clicked on a link to a topic I've not written up yet, sorry about this - this is work in progress!

Feel free to [Raise an Issue](https://github.com/dwmkerr/hacker-laws/issues) requesting more details, or [Open a Pull Request](https://github.com/dwmkerr/hacker-laws/pulls) to submit your proposed definition of the topic.
