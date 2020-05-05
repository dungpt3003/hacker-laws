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
    - [Dao cạo Hanlon](#dao-c%e1%ba%a1o-hanlon)
    - [Luật Hofstadter](#lu%e1%ba%adt-hofstadter)
    - [Luật Hutber](#lu%e1%ba%adt-hutber)
    - [Chu kỳ Kỳ vọng và Luật Amara](#chu-k%e1%bb%b3-k%e1%bb%b3-v%e1%bb%8dng-v%c3%a0-lu%e1%ba%adt-amara)
    - [Luật Hyrum (Luật Giao diện ngầm)](#lu%e1%ba%adt-hyrum-lu%e1%ba%adt-giao-di%e1%bb%87n-ng%e1%ba%a7m)
    - [Luật Kernighan](#lu%e1%ba%adt-kernighan)
    - [Luật Metcalfe](#lu%e1%ba%adt-metcalfe)
    - [Luật Moore](#lu%e1%ba%adt-moore)
    - [Luật Murphy / Luật Sod](#lu%e1%ba%adt-murphy--lu%e1%ba%adt-sod)
    - [Dao cạo Occam](#dao-c%e1%ba%a1o-occam)
    - [Luật Parkinson](#lu%e1%ba%adt-parkinson)
    - [Hiệu ứng Tối ưu hoá sớm](#hi%e1%bb%87u-%e1%bb%a9ng-t%e1%bb%91i-%c6%b0u-ho%c3%a1-s%e1%bb%9bm)
    - [Luật Putt](#lu%e1%ba%adt-putt)
    - [Luật Reed](#lu%e1%ba%adt-reed)
    - [Định luật Bảo toàn Độ phức tạp (Luật Tesler)](#%c4%90%e1%bb%8bnh-lu%e1%ba%adt-b%e1%ba%a3o-to%c3%a0n-%c4%90%e1%bb%99-ph%e1%bb%a9c-t%e1%ba%a1p-lu%e1%ba%adt-tesler)
    - [The Law of Leaky Abstractions](#the-law-of-leaky-abstractions)
    - [Luật của Sự tầm thường](#lu%e1%ba%adt-c%e1%bb%a7a-s%e1%bb%b1-t%e1%ba%a7m-th%c6%b0%e1%bb%9dng)
    - [Triết lý Unix](#tri%e1%ba%bft-l%c3%bd-unix)
    - [Mô hình Spotify](#m%c3%b4-h%c3%acnh-spotify)
    - [Luật Wadler](#lu%e1%ba%adt-wadler)
    - [Luật Wheaton](#lu%e1%ba%adt-wheaton)
  - [Nguyên tắc](#nguy%c3%aan-t%e1%ba%afc)
    - [Nguyên tắc Dilbert](#nguy%c3%aan-t%e1%ba%afc-dilbert)
    - [Nguyên tắc Pareto (Quy tắc 80/20)](#nguy%c3%aan-t%e1%ba%afc-pareto-quy-t%e1%ba%afc-8020)
    - [Nguyên tắc Peter](#nguy%c3%aan-t%e1%ba%afc-peter)
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
    - [Sự ảo tưởng của Điện toán Phân tán](#s%e1%bb%b1-%e1%ba%a3o-t%c6%b0%e1%bb%9fng-c%e1%bb%a7a-%c4%90i%e1%bb%87n-to%c3%a1n-ph%c3%a2n-t%c3%a1n)
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

### Dao cạo Hanlon

[Dao cạo Hanlon xem tại Wikipedia](https://en.wikipedia.org/wiki/Hanlon%27s_razor)

> Đừng vội vã gán ý đồ xấu cho một hiện tượng trong khi có thể giải thích một cách hợp lí rằng đó là do sự thiếu hiểu biết.
>
> Robert J. Hanlon

Nguyên tắc này gợi ý rằng các hành động dẫn đến kết quả tiêu cực chưa chắc đã là kết quả của ý đồ xấu. Thay vào đó, kết quả tiêu cực nhiều khả năng được quy kết từ chính những hành động đó và/hoặc ảnh hưởng của sự thiếu hiểu biết.

### Luật Hofstadter

[Luật Hofstadter xem tại Wikipedia](https://en.wikipedia.org/wiki/Hofstadter%27s_law)

> Mọi việc sẽ luôn mất thời gian hơn dự kiến, kể cả khi bạn đã tính đến Luật Hofstadter
>
> (Douglas Hofstadter)

Bạn có thể đã từng nghe đến luật này khi xem xét việc ước tính thời gian hoàn thành của một việc gì đó. Sự thật là trong phát triển phần mềm, chúng ta thường không giỏi trong việc ước tính một cách chính xác thời gian hoàn thành của bất kì việc gì.

Luật này được trích từ cuốn sách '[Gödel, Escher, Bach: An Eternal Golden Braid](#reading-list)'.

Xem thêm:

- [Reading List: Gödel, Escher, Bach: An Eternal Golden Braid](#reading-list)

### Luật Hutber

[Luật Hutber xem tại Wikipedia](https://en.wikipedia.org/wiki/Hutber%27s_law)

> Cải tiến đồng nghĩa với "cải lùi"
>
> ([Patrick Hutber](https://en.wikipedia.org/wiki/Patrick_Hutber))

Luật này gợi ý rằng các cải tiến của một hệ thống sẽ dẫn đến sự hỏng hóc ở một số phần, hoặc che giấu sự bất ổn, dẫn tới sự suy giảm chung so với trạng thái hiện tại của hệ thống.

Ví dụ, việc gỉảm độ trễ phản hồi cho một end-point nhất định có thể dẫn tới các vấn đề về tăng thông lượng và dung lượng xa hơn trong luồng request, làm ảnh hưởng tới một hệ thống con hoàn toàn khác.

### Chu kỳ Kỳ vọng và Luật Amara

[Chu kỳ Kỳ vọng xem tại Wikipedia](https://en.wikipedia.org/wiki/Hype_cycle)

> Chúng ta thường có xu hướng đánh giá quá cao ảnh hưởng của một công nghệ trong ngắn hạn và coi nhẹ ảnh hưởng của nó trong dài hạn.
> (Roy Amara)

Chu kỳ Kỳ vọng là một minh họa trực quan về sự phát triển của một công nghệ cũng như những sự phấn khích bao quanh nó theo thời gian, được tạo ra bởi Gartner (một hãng nghiên cứu ở Mỹ - ND). 

![The Hype Cycle](./images/gartner_hype_cycle.png)

*(Nguồn ảnh: Bởi Jeremykemp tại Wikipedia tiếng Anh, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=10547051)*

Nói một cách ngắn gọn, chu kỳ này gợi ý rằng thường sẽ có một sự phấn khích lớn xung quanh một công nghệ mới và tiềm năng tác động của nó. Các nhóm thường tiếp cận những công nghệ này một cách nhanh chóng và đôi khi kết quả khiến họ thất vọng. Điều này có thể là do công nghệ chưa đủ "chín", hoặc khả năng ứng dụng vào các vấn đề thực tế của nó chưa được nhìn nhận đầy đủ. Sau một khoảng thời gian nhất định, khi khả năng và cơ hội ứng dụng thực tế của công nghệ đó tăng lên, các nhóm cuối cùng cũng có thể làm việc hiệu quả với nó. Roy Amara tóm tắt điều này một cách ngắn gọn trong trích dẫn - "Chúng ta thường có xu hướng đánh giá quá cao ảnh hưởng của một công nghệ trong ngắn hạn và coi nhẹ ảnh hưởng của nó trong dài hạn."

### Luật Hyrum (Luật Giao diện ngầm)

[Hyrum's Law Online](http://www.hyrumslaw.com/)

> Khi số lượng người dùng một API đạt đến một mức nhất định,
> những điều bạn định nghĩa trong tài liệu sẽ không còn quan trọng nữa:
> tất cả các hành vi có thể quan sát được của hệ thống
> sẽ bị phụ thuộc bởi ai đó.
>
> (Hyrum Wright)

Luật Hyrum chỉ ra rằng khi API của bạn có một số lượng người dùng đủ lớn, tất cả các hành vi của API đó (kể cả những hành vi không được định nghĩa trong tài liệu công khai) cuối cùng sẽ trở nên bị phụ thuộc bởi người nào đó. Một ví dụ đơn giản có thể kể đến là các yếu tố phi chức năng như là thời gian phản hồi của một API. Một ví dụ tinh tế hơn là người dùng dựa vào việc áp dụng một biểu thức chính quy cho thông báo lỗi để xác định *loại* lỗi của một API. Thậm chí nếu tài liệu công khai của API không nói gì về nội dung của thông báo và nói rõ rằng người dùng nên sử dụng mã lỗi, _một vài_ người dùng có thể dùng thông báo và việc thay đổi cái này sẽ phá vỡ API đối với những người dùng đó.

Xem thêm:

- [The Law of Leaky Abstractions](#the-law-of-leaky-abstractions)
- [XKCD 1172](https://xkcd.com/1172/)

### Luật Kernighan

> Việc debug khó gấp đôi việc viết mã từ đầu. Vậy nên, nếu bạn viết mã một cách thông minh nhất có thể, thì theo định nghĩa, bạn không đủ thông minh để debug nó. 
>
> (Brian Kernighan)

Luật Kernighan được đặt tên theo [Brian Kernighan](https://en.wikipedia.org/wiki/Brian_Kernighan), bắt nguồn từ một trích dẫn trong cuốn sách [The Elements of Programming Style](https://en.wikipedia.org/wiki/The_Elements_of_Programming_Style) của Kernighan và Plauger: 

> Ai cũng biết từ đầu rằng việc debug khó gấp đôi việc viết một chương trình. Vậy nếu bạn "chỉ" đủ thông minh để viết mã, bạn sẽ debug như thế nào? 

Dù hơi cường điệu, luật Kerighan lập luận rằng mã nguồn đơn giản nên được ưu tiên hơn mã nguồn quá phức tạp, bởi vì việc debug bất kì vấn đề gì phát sinh từ những đoạn mã phức tạp có thể sẽ rất tốn kém hoặc thậm chí là không khả thi.

See also:

- [Nguyên tắc KISS](#nguy%c3%aan-t%e1%ba%afc-kiss)
- [Triết lý Unix](#tri%e1%ba%bft-l%c3%bd-unix)
- [Dao cạo Occam](#dao-c%e1%ba%a1o-occam)

### Luật Metcalfe

[Luật Metcalfe xem tại Wikipedia](https://en.wikipedia.org/wiki/Metcalfe's_law)

> Trong lý thuyết mạng, giá trị của một hệ thống tăng trưởng xấp xỉ bằng bình phương số người dùng của hệ thống đó.

Luật này dựa trên số lượng kết nối chập đôi trong một hệ thống và liên hệ mật thiết với [Luật Reed](#reeds-law). Odlyzko và những người khác đã lập luận rằng cả Luật Reed và Luật Metcalfe đều đánh giá quá mức giá trị của một hệ thống bằng việc bỏ qua giới hạn nhận thức của con người trong việc kết nối; xem [Số Dunbar](#s%e1%bb%91-dunbar)

See also:
- [Luật Reed](#lu%e1%ba%adt-reed)
- [Số Dunbar](#s%e1%bb%91-dunbar)

### Luật Moore

[Luật Moore xem tại Wikipedia](https://en.wikipedia.org/wiki/Moore%27s_law)

> Số lượng bán dẫn trong một mạch tích hợp sẽ tăng lên gấp đôi sau mỗi hai năm.

Thường được sử dụng để minh hoạ tốc độ phát triển tuyệt đối của công nghệ chip và bán dẫn, dự đoán của Moore đã được chứng minh là có độ chính xác cao từ những năm 70 của thế kỉ 20 cho tới những năm 2000. Trong những năm gần đây, xu hướng có thay đổi một chút, một phần là do [giới hạn vật lý về mức độ thu nhỏ của các thành phần](https://en.wikipedia.org/wiki/Quantum_tunnelling). Tuy nhiên, những tiến bộ trong tính toán song song và những thay đổi tiềm năng mang tính cách mạng trong công nghệ bán dẫn và điện toán lượng tử có thể giữ nguyên tính đúng đắn của luật Moore trong nhiều thập kỉ nữa.

### Luật Murphy / Luật Sod

[Luật Murphy xem tại Wikipedia](https://en.wikipedia.org/wiki/Murphy%27s_law)

> Bất cứ thứ gì có thể sai thì sẽ sai.

Liên quan tới [Edward A. Murphy, Jr](https://en.wikipedia.org/wiki/Edward_A._Murphy_Jr.) _Luật Murphy_ khẳng định rằng nếu điều gì đó có khả năng sai, nó sẽ sai.

Đây là một ngạn ngữ phổ biến trong cộng đồng các nhà phát triển. Đôi khi một vài điều bất ngờ xảy ra trong quá trình phát triển, kiểm thử hoặc thậm chí là trên môi trường sản phẩm. Luật này còn liên quan tới một luật phổ biến hơn trong tiếng Anh-Anh là _Luật Sod_:

> Nếu điều gì đó có thể sai, nó sẽ sai, vào thời điểm tệ nhất có thể.

Những 'luật' này thường được sử dụng theo nghĩa châm biếm. Tuy nhiên, các hiện tượng như [Thiên kiến xác nhận](#TODO) hay [_Thiên kiến lựa chọn_](#TODO) có thể khiến mọi người quá nhấn mạnh tầm quan trọng của chúng (khi mọi thứ hoạt động bình thường, chúng thường không được chú ý, còn các lỗi thì được chú ý và đem ra thảo luận nhiều hơn).

Xem thêm:

- [Thiên kiến xác nhận](#TODO)
- [Thiên kiến lựa chọn](#TODO)

### Dao cạo Occam

[Dao cạo Occam xem tại Wikipedia](https://vi.wikipedia.org/wiki/Dao_c%E1%BA%A1o_Ockham)

> Các thực thể không nên bị phức tạp hóa một cách không cần thiết.
>
> William xứ Occam

Dao cạo Occam cho rằng trong số những giải pháp khả thi, giải pháp hữu ích nhất thường là giải pháp cần tới ít khái niệm và giả định nhất. Giải pháp này là giải pháp đơn giản nhất và giải quyết đúng bài toán được đặt ra mà không dẫn tới những sự phức tạp ngẫu nhiên hay những hậu quả tiêu cực có thể có.

Xem thêm:

- [YAGNI](#yagni)
- [Không có viên đạn bạc: Sự phức tạp ngẫu nhiên và tất nhiên](https://en.wikipedia.org/wiki/No_Silver_Bullet)

Ví dụ:

- [Phát triển phần mềm tinh gọn: Loại bỏ dư thừa](https://en.wikipedia.org/wiki/Lean_software_development#Eliminate_waste)

### Luật Parkinson

[Luật Parkinson xem tại Wikipedia](https://en.wikipedia.org/wiki/Parkinson%27s_law)

> Công việc luôn tự mở rộng ra để chiếm đủ thời gian được ấn định cho nó.

Trong bối cảnh ban đầu, luật này được dựa trên nghiên cứu trên các cơ quan hành chính. Nó có thể được áp dụng một cách bi quan vào quá trình phát triển phần mềm, rằng một nhóm sẽ làm việc thiếu hiệu quả cho đến khi thời hạn đến gần, sau đó vội vã hoàn thành công việc trước thời hạn, làm cho thời hạn thực tế trở nên tuỳ tiện.

Nếu kết hợp luật này với [Luật Hofstadter](#lu%e1%ba%adt-hofstadter), thậm chí chúng ta còn có một góc nhìn bi quan hơn - Công việc luôn tự mở rộng ra để chiếm đủ thời gian được ấn định cho nó và vẫn *mất nhiều thời gian hơn dự kiến*.

Xem thêm:

- [Luật Hofstadter](#lu%e1%ba%adt-hofstadter)

### Hiệu ứng Tối ưu hoá sớm

[Hiệu ứng Tối ưu hoá sớm xem tại Wikipedia](http://wiki.c2.com/?PrematureOptimization)

> Tối ưu hoá sớm là nguồn gốc của mọi vấn đề.
>
> [(Donald Knuth)](https://twitter.com/realdonaldknuth?lang=en)

Trong bài viết [Lập trình có cấu trúc với câu lệnh Go To](http://wiki.c2.com/?StructuredProgrammingWithGoToStatements) của Donald Knuth, ông viết: "Lập trình viên thường lãng phí lượng thời gian khổng lồ suy nghĩ hoặc lo lắng về tốc độ của những phần không quan trọng trong chương trình của họ, và thực tế những nỗ lực cải thiện hiệu năng thường tạo ảnh hưởng tiêu cực không nhỏ khi tính tới việc debug và bảo trì. Chúng ta nên quên đi những cải tiến hiệu năng vụn vặt, hay có thể nói, trong 97% số trường hợp, **tối ưu hoá sớm là nguồn gốc của mọi vấn đề**". Tuy nhiên, chúng ta không nên bỏ qua cơ hội của mình trong 3% quan trọng còn lại.

Tuy nhiên, _Tối ưu hoá sớm_ (_Premature Optimization_) có thể được định nghĩa (một cách nhẹ nhàng hơn) là tối ưu hoá trước cả khi chúng ta biết rằng mình cần nó.

### Luật Putt

[Luật Putt xem tại Wikipedia](https://en.wikipedia.org/wiki/Putt%27s_Law_and_the_Successful_Technocrat)

> Công nghệ bị chi phối bởi hai loại người, những người hiểu những gì họ không quản lí và những người quản lí những gì họ không hiểu.

Luật Putt thường được theo sau bởi Hệ quả Putt:

> Mọi hệ thống phân cấp kỹ thuật, theo thời gian, phát triển một sự đảo ngược năng lực.

Những mệnh đề này gợi ý rằng do các tiêu chí lựa chọn và xu hướng tổ chức nhóm khác nhau, sẽ có một số người có kĩ năng làm việc ở cấp độ thấp của một tổ chức kĩ thuật, trong khi một số người nắm các vai trò quản lí nhưng không hiểu rõ về mức độ phức tạp và thử thách của công việc mà họ quản trị. Điều này có thể là do các hiện tượng như là [Nguyên tắc Peter](#nguy%c3%aan-t%e1%ba%afc-peter) hay [Nguyên tắc Dilbert](#nguy%c3%aan-t%e1%ba%afc-dilbert).

Xem thêm:

- [Nguyên tắc Peter](#nguy%c3%aan-t%e1%ba%afc-peter)
- [Nguyên tắc Dilbert](#nguy%c3%aan-t%e1%ba%afc-dilbert)


### Luật Reed

[Luật Reed xem tại Wikipedia](https://en.wikipedia.org/wiki/Reed's_law)

> Tiện ích của một mạng lớn, cụ thể là mạng xã hội, tăng trưởng theo cấp số mũ so với kích thước của mạng.

Luật này được dựa trên lý thuyết đồ thị, trong đó tiện ích tăng trưởng theo số lượng nhóm con, nhanh hơn số lượng thành viên hay số lượng các kết nối cặp tối đa. Odlyzko và một số người khác lập luận rằng luật Reed đã đánh giá quá mức tiện ích của một hệ thống bằng việc bỏ qua những giới hạn nhận thức của con người đối với các hiệu ứng mạng; tham khảo [Số Dunbar](#s%e1%bb%91-dunbar)

Xem thêm:
- [Luật Metcalfe](#lu%e1%ba%adt-metcalfe)
- [Số Dunbar](#s%e1%bb%91-dunbar)

### Định luật Bảo toàn Độ phức tạp (Luật Tesler)

[Định luật Bảo toàn Độ phức tạp xem tại Wikipedia](https://en.wikipedia.org/wiki/Law_of_conservation_of_complexity)

Luật này chỉ ra rằng mỗi hệ thống có một mức độ phức tạp nhất định trong không thể bị loại bỏ.

Một vài sự phức tạp trong một hệ thống là do 'vô tình'. Nó là kết quả của một cấu trúc tồi, lỗi, hoặc việc mô hình hoá vấn đề không tốt. Sự phức tạp vô tình có thể bị giảm thiểu hoặc loại bỏ hoàn toàn. Tuy nhiên, một vài sự phức tạp thuộc về 'bản chất', là hệ quả của sự phức tạp vốn có trong vấn đề đang được giải quyết. Sự phức tạp này có thể được chuyển từ phần này qua phần khác, nhưng không thể bị loại bỏ hoàn toàn.

Một yếu tố thú vị của luật này là ngay cả khi đơn giản hoá toàn bộ hệ thống, sự phức tạp bản chất không bị mất đi, mà được _chuyển sang phía người dùng_, khiến họ phải thao tác phức tạp hơn cần thiết.

### The Law of Leaky Abstractions

[The Law of Leaky Abstractions on Joel on Software](https://www.joelonsoftware.com/2002/11/11/the-law-of-leaky-abstractions/)

> Tất cả các khái niệm trừu tượng phức tạp, mở một mức nào đó, đều dễ rò rỉ.
>
> ([Joel Spolsky](https://twitter.com/spolsky))

Luật này chỉ ra rằng các khái niệm trừu tượng thường được sử dụng trong tính toán để đơn giản hoá việc làm việc với các hệ thống phức tạp sẽ làm 'rò rỉ' các yếu tố cấu thành nên hệ thống. Điều này làm cho các khái niệm trừu tượng này trở nên khó đoán.

Một ví dụ là việc tải một tập tin và đọc nội dung của nó. APIs của hệ thống tệp là một __trừu tượng__ của hệ thống cấp thấp hơn, và hệ thống này cũng chính là một trừu tượng của các tiến trình vật lý liên quan đến việc chuyển đổi dữ liệu trên một đĩa từ (hoặc bộ nhớ flash trong trường hợp ổ SSD). Trong đa số các trường hợp, cách trừu tượng hoá việc xử lí tệp như là một dòng chảy dữ liệu nhị phân sẽ hiệu quả. Tuy nhiên, với một ổ đĩa từ, việc đọc dữ liệu tuần tự sẽ nhanh hơn *một cách đáng kể* so với truy cập ngẫu nhiên (do chi phí lỗi trang tăng). Ngược lại, với ổ SSD, chi phí ngày không tồn tại. Các chi tiết cơ bản sẽ cần được hiểu rõ để xử lí những trường hợp như vậy (ví dụ, các tệp chỉ mục của cơ sở dữ liệu được cấu trúc để giảm chi phí của truy cập ngẫy nhiên). Trừu tượng đã 'làm rò rỉ' chi tiết triển khai mà nhà phát triển có thể cần phải để ý tới.

Ví dụ kể trên có thể trở nên phức tạp hơn khi có _nhiều_ trừu tượng hơn. Hệ điều hành Linux cho phép các tệp có được truy xuất được qua mạng nhưng lại được biểu diễn cục bộ như các tệp 'bình thường'. Trừu tượng này sẽ bị 'rò rỉ' nếu như có lỗi mạng. Nếu một nhà phát triển xử lí các tệp này như các tệp 'bình thường' mà không quan tâm đến việc chúng có thể bị phụ thuộc vào độ trễ hay lỗi mạng, các giải pháp sẽ có lỗi.

Bài báo mô tả luật này gợi ý rằng sự phụ thuộc quá mức vào các trừu tượng kết hợp với sự thiếu hiểu biết về các tiến trình bên trong làm cho việc xử lí vấn đề trở nên phức tạp _hơn_ trong một vài trường hợp.

Xem thêm:

- [Luật Hyrum](#lu%e1%ba%adt-hyrum-lu%e1%ba%adt-giao-di%e1%bb%87n-ng%e1%ba%a7m)

Ví dụ thực tế:

- [Vấn đề khởi động chậm của Photoshop](https://forums.adobe.com/thread/376152) - một vấn đề mà tôi đã gặp trong quá khứ. Photoshop khởi động chậm, đôi khi mất đến vài phút. Có vẻ như vấn đề nằm ở việc trong quá trình khởi độn, Photoshop đọc một số thông tin về máy in mặc định hiện tại. Tuy nhiên, nếu máy in đó là một máy in qua mạng, điều này sẽ rất tốn thời gian. Trong trường hợp này, _trừu tượng_ của một máy in qua mạng được biểu diễn trong hệ thống tương tự như máy in cục bộ gây ra vấn đề cho những người dùng với kết nối kém.

### Luật của Sự tầm thường

[Luật của Sự tầm thường xem tại Wikipedia](https://en.wikipedia.org/wiki/Law_of_triviality)

Luật này gợi ý rằng người ta thường dành quá nhiều thời gian và sự chú ý vào những vấn đề tầm thường hơn là những vấn đề thực sự nghiêm trọng và thiết yếu.

Một ví dụ giả tưởng thường được sử dụng là về một hội đồng phê duyệt các kế hoạch cho nhà máy năng lượng hạt nhân, những người dành phần lớn thời gian của họ để thảo luận về kiến trúc của nhà để xe đạp, thay vì vấn đề quan trọng hơn nhiều là thiết kế của nhà máy hạt nhân. Rất khó để đóng góp những ý kiến có giá trị về một vấn đề cực kì phức tạp và rộng lớn mà không có trình độ chuyên môn cao hoặc sự chuẩn bị kĩ càng. Tuy nhiên, người ta thường muốn được nhìn nhận như là có đóng gó. Điều này dẫn tới xu hướng tập trung quá nhiều vào các tiểu tiết, những điều có thể lí giải dễ dàng nhưng không thực sự cần thiết hay quan trọng.

Ví dụ giả tưởng nói trên dẫn tới khái niệm "Bike Shedding" như là một cách diễn đạt cho việc tốn thời gian vào các tiểu tiết. Một khái niệm tương đương là "Yak-Shaving"

### Triết lý Unix

[Xem Triết lý Unix tại Wikipedia](https://en.wikipedia.org/wiki/Unix_philosophy)

Triết lý Unix nói rằng các thành phần phần mềm nên nhỏ gọn, và tập trung làm tốt một việc cụ thể. Điều này giúp việc xây dựng các hệ thống dễ dàng bằng cách kết hợp các đơn vị nhỏ, đơn giản, được định nghĩa rõ ràng, thay vì sử dụng các chương trình lớn, phức tạp và đa mục đích.

Các mô hình hiện đại như 'Kiến trúc Microservice' có thể coi là một ứng dụng của luật này, trong đó các dịch vụ được thiết kế nhỏ gọn, tập trung làm một việc cụ thể, cho phép hành vi phức tạp được tạo thành từ các khối xây dựng đơn giản.

### Mô hình Spotify

[Mô hình Spotify xem tại Spotify Labs](https://labs.spotify.com/2014/03/27/spotify-engineering-culture-part-1/)

Mô hình Spotify là một cách tiếp cận trong việc xây dựng cấu trúc cho đội nhóm và tổ chức, được phổ biến bởi 'Spotify'. Trong mô hình này, các đội nhóm được tập trung xây dựng xung quanh tính năng thay vì công nghệ. 

Mô hình Spotify cũng phổ biến các khái niệm về **Tribes**, **Guilds** hay **Chapters**, là những thành phần khác trong cấu trúc tổ chức của họ.

### Luật Wadler

[Luật Wadler xem tại wiki.haskell.org](https://wiki.haskell.org/Wadler's_Law)

> Trong bất kỳ thiết kế ngôn ngữ nào, tổng thời gian dành để thảo luận một tính năng trong danh sách này tỉ lệ thuận theo lũy thừa 2 của vị trí.
>
> 0. Ngữ nghĩa
> 1. Cú pháp
> 2. Cú pháp từ vựng
> 3. Cú pháp từ vựng của bình luận
>
> Nói cách khác, với mỗi giờ dành cho ngữ nghĩa, cần 8 giờ dành cho cú pháp từ vựng của bình luận.

Tương tự như [Luật của sự tầm thường](#lu%e1%ba%adt-c%e1%bb%a7a-s%e1%bb%b1-t%e1%ba%a7m-th%c6%b0%e1%bb%9dng), luật Wadler chỉ ra rằng khi thiết kế một ngôn ngữ, lượng thời gian dành cho các cấu trúc của ngôn ngữ không tương xứng với tầm quan trọng của chúng.

Xem thêm:

- [Luật của sự tầm thường](#lu%e1%ba%adt-c%e1%bb%a7a-s%e1%bb%b1-t%e1%ba%a7m-th%c6%b0%e1%bb%9dng)

### Luật Wheaton

[Liên kết](http://www.wheatonslaw.com/)

[Ngày lễ chính thức](https://dontbeadickday.com/)

> Đừng là đồ khốn.
>
> _Wil Wheaton_

Được tạo ra bởi Wil Wheaton (Star Trek: The Next Generation, The Big Bang Theory), điều luật đơn giản, ngắn gọn và mạnh mẽ này nhắm tới việc tăng cường sự hài hoà và sự tôn trọng trong một tổ chức chuyên nghiệp. Nó có thể được áp dụng khi nói chuyện với đồng nghiệp, thực hiện việc đánh giá mã nguồn, tranh cãi về quan điểm, phê bình và nói chung là hầu hết các tương tác giữa người với người trong môi trường chuyên nghiệp.

## Nguyên tắc

Các nguyên tắc thường là các hướng dẫn liên quan tới thiết kế.

### Nguyên tắc Dilbert

[Xem nguyên tắc Dilbert tại Wikipedia](https://en.wikipedia.org/wiki/Dilbert_principle)

> Các công ty có xu hướng thăng cấp một cách có hệ thống các nhân viên không đủ năng lực vào vị trí quản lý để đưa họ ra khỏi quy trình làm việc
>
> _Scott Adams_

Một khái niệm quản lý được phát triển bởi Scott Adams (tác giả của truyện tranh Dilbert), Nguyên tắc Dilbert được lấy cảm hứng từ [Nguyên tắc Peter](#the-peter-principle). Theo Nguyên tắc Dilbert, những nhân viên không có đủ năng lực thường được thăng chức lên làm quản lý nhằm hạn chế thiệt hại mà họ có thể gây ra. Adams đã giải thích nguyên lý lần đầu tiên tại một bài báo Phố Wall (Wall Street Journal) vào năm 1995, và đã mở rộng nó trong cuốn sách kinh doanh năm 1996 của ông, [The Dilbert Principle](#reading-list)

Xem thêm:

- [The Peter Principle](#the-peter-principle)
- [Putt's Law](#putts-law)

### Nguyên tắc Pareto (Quy tắc 80/20)

[Nguyên tắc Pareto xem tại Wikipedia](https://en.wikipedia.org/wiki/Pareto_principle)

> Hầu hết mọi thứ trong cuộc sống không được phân phối đều.

Nguyên tắc Pareto gợi ý rằng trong vài trường hợp, một phần lớn kết quả được tạo ra từ một phần nhỏ đầu vào:

- 80% thành phần của một phần mềm có thể chỉ được viết trong khoảng 20% lượng thời gian được phân bổ (ngược lại, 20% khó nhất của mã nguồn tiêu tống mất 80% thời gian).
- 20% công sức tạo ra 80% kết quả.
- 20% lượng công việc tạo ra 80% doanh thu.
- 20% số lỗi tạo ra 80% số lần sập chương trình.
- 20% số tính năng năng chiếm 80% lượng sử dụng.

Vào những năm 40 của thế kỉ 20, tiến sĩ, kĩ sư người Mỹ-Rumani Joseph Juran, người được cho là cha đẻ của kiểm soát chất lượng, [bắt đầu áp dụng nguyên tắc Pareto cho các vấn đề chất lượng](https://en.wikipedia.org/wiki/Joseph_M._Juran).

Nguyên tắc này còn được biết tới như là: Quy tắc 80/20, Luật Thiểu số Quan trọng hay Nguyên tắc Nhân tố thưa.

Ví dụ thực tế:

- Vào năm 2002, Microsoft thông báo rằng bằng việc sửa 20% số lỗi được báo nhiều nhất, 80% số lỗi và lần sập chương trình trên Windows cũng được loại bỏ.([Xem thêm](https://www.crn.com/news/security/18821726/microsofts-ceo-80-20-rule-applies-to-bugs-not-just-features.htm)).

### Nguyên tắc Peter

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

- [Luật Hyrum](#lu%e1%ba%adt-hyrum-lu%e1%ba%adt-giao-di%e1%bb%87n-ng%e1%ba%a7m)


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
