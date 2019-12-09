<!-- =================== Bắt đầu dịch Phần 1 ==================== -->

<!--
# Introduction
-->

# *dịch tiêu đề phía trên*
:label:`chap_introduction`

Giới thiệu

<!--
Until recently, nearly every computer program that interact with daily
were coded by software developers from first principles.
Say that we wanted to write an application to manage an e-commerce platform.  After huddling around a whiteboard for a few hours to ponder the problem,
we would come up with the broad strokes of a working solution that might probably look something like this:
(i) users interact with the application through an interface
running in a web browser or mobile application;
(ii) our application interacts with a commercial-grade database engine
to keep track of each user's state and maintain records
of historical transactions; and (iii) at the heart of our application,
the *business logic* (you might say, the *brains*) of our application
spells out in methodical detail the appropriate action
that our program should take in every conceivable circumstance.
-->


*dịch đoạn phía trên*

Mãi tới gần đây, hầu như tất cả các chương trình máy tính mà chúng ta tương tác hàng ngày đều được tạo ra bởi những nhà phát triển phần mềm theo các nguyên lý lập trình cơ bản nhất. Nếu chúng ta muốn viết một ứng dụng chung cho việc quản lý thương mại điện tử. Chúng ta sẽ trao đổi và phác họa sơ bộ vấn đề như sau:
(i) người dùng tương tác với ứng dụng qua giao diện trình duyệt web trên máy tính hoặc trên điện thoại;
(ii) ứng dụng tương tác với một hệ thống cơ sở dữ liệu thương mại, theo dõi trạng thái và lưu giữ lại các giao dịch của người dùng; và 
(iii) ở lõi (hay còn gọi là bộ não) của ứng dụng, được thiết kế chi tiết để thực thi từng trường hợp cụ thể.


<!--
To build the *brains* of our application,
we'd have to step through every possible corner case
that we anticipate encountering, devising appropriate rules.
Each time a customer clicks to add an item to their shopping cart,
we add an entry to the shopping cart database table,
associating that user's ID with the requested product’s ID.
While few developers ever get it completely right the first time
(it might take some test runs to work out the kinks),
for the most part, we could write such a program from first principles
and confidently launch it *before ever seeing a real customer*.
Our ability to design automated systems from first principles
that drive functioning products and systems, often in novel situations,
is a remarkable cognitive feat.
And when you are able to devise solutions that work $100\%$ of the time,
*you should not be using machine learning*.
-->

*dịch đoạn phía trên*

Để xây dựng *bộ não* của ứng dụng này, ta phải đưa ra tất cả các trường hợp có thể, qua đó đặt ra những quy tắc thích hợp.
Mỗi lần người dùng nhấn để thêm một món đồ vào giỏ hàng, ta thêm một trường vào bảng giỏ hàng trong cơ sở dữ liệu, liên kết định danh ID của người dùng với định danh ID của món hàng được yêu cầu.
Gần như rất ít lập trình viên có thể làm đúng hết trong lần đầu tiên, (sẽ cần vài lần chạy kiểm tra để xử lý hết được những trường hợp phức tạp), phần lớn chúng ta đều xây dựng từ những nguyên tắc cơ bản nhất, trước khi chính thức giới thiệu sản phẩm cho khách hàng.
Khả năng phát triển những sản phầm và hệ thống tự động từ những nguyên tắc suy luận cơ bản nhất, thường là trong những điều kiện mới, là một kì công trong suy luận và nhận thức của con người.
Và khi mà bạn có thể tạo ra một giải pháp mà có thể hoạt động được trong mọi tình huống, *bạn không nên sử dụng học máy*.


<!--
Fortunately for the growing community of ML scientists,
many tasks that we would like to automate
do not bend so easily to human ingenuity.
Imagine huddling around the whiteboard with the smartest minds you know,
but this time you are tackling one of the following problems:
-->

*dịch đoạn phía trên*

May mắn thay cho sự tang trưởng của các nhà khoa học về học máy, nhiều tác vụ mà chúng ta muốn tự động hoá không dễ dàng bị khuất phục bởi sự tài tình của con người.
Thử tưởng tượng bạn đang quây quần bên tấm bảng trắng với những bộ não thông minh nhất mà bạn biết, nhưng lần này bạn đang đương đầu với một trong những vấn đề dưới đây:


<!--
* Write a program that predicts tomorrow's weather given geographic
information, satellite images, and a trailing window of past weather.
* Write a program that takes in a question, expressed in free-form text, and
 answers it correctly.
* Write a program that given an image can identify all the people it contains,
 drawing outlines around each.
* Write a program that presents users with products that they are likely to
  enjoy but unlikely, in the natural course of browsing, to encounter.
-->

*dịch đoạn phía trên*

* Viết một chương trình dự báo thời tiết cho một địa điểm xác định, có dữ liệu hình ảnh vệ tinh, và một chuỗi dữ liệu thời tiết trong quá khứ.
* Viết một chương trình lấy đầu vào là một câu hỏi, mô tả không theo khuôn mẫu, và trả lời nó một cách chính xác.
* Viết một chương trình cung cấp hình ảnh có thể xác định tất cả những người trong ảnh, và các nét vẽ bao quanh mỗi người.
* Viết một chương trình hiển thị ra cho người dùng những sản phẩm mà họ có khả năng cao sẽ thích, nhưng lại ít có khả năng gặp được khi duyệt qua môt cách tự nhiên.


<!--
In each of these cases, even elite programmers
are incapable of coding up solutions from scratch.
The reasons for this can vary. Sometimes the program
that we are looking for follows a pattern that changes over time,
and we need our programs to adapt.
In other cases, the relationship (say between pixels,
and abstract categories) may be too complicated,
requiring thousands or millions of computations
that are beyond our conscious understanding
(even if our eyes manage the task effortlessly).
Machine learning (ML) is the study of powerful
techniques that can *learn* from *experience*.
As ML algorithm accumulates more experience,
typically in the form of observational data or
interactions with an environment, their performance improves.
Contrast this with our deterministic e-commerce platform,
which performs according to the same business logic,
no matter how much experience accrues,
until the developers themselves *learn* and decide
that it is time to update the software.
In this book, we will teach you the fundamentals of machine learning,
and focus in particular on deep learning, a powerful set of techniques
driving innovations in areas as diverse as computer vision,
natural language processing, healthcare, and genomics.
-->

*dịch đoạn phía trên*

Trong mỗi trường hợp trên, cho dù có là lập trình viên thượng thừa cũng không thể lập trình lên được từ con số không. Có nhiều lý do khác nhau. Đôi khi chương trình mà chúng ta tìm lại có khuôn mẫu thay đổi theo thời gian, và chương trình của chúng ta cần phải thích ứng.
Trong nhiều trường hợp khác, mối quan hệ (giả dụ như giữa các điểm ảnh và các hạng mục trừu tượng) có thể là quá phức tạp, yêu cầu hàng ngàn hay hàng triệu các phép tính vượt ra khỏi khả năng của chúng ta (mặc dù chúng ta có thể xử lý tác vụ này một cách dễ dàng bằng mắt).
Học máy (Machine Learning - ML) là lĩnh vực nghiên cứu những kĩ thuật tiên tiến mà có thể *học* từ *kinh nghiệm*.
Khi thuật toán học máy tích luỹ thêm nhiều kinh nghiệm, thường là dưới dạng dữ liệu quan sát hoặc tương tác với môi trường, hiệu năng của nó sẽ tăng lên.
Tương phản với hệ thống thương mại điện tử hiện nay của chúng ta, khi mà nó luôn tuân theo nghiệp vụ phân tích đã có, mặc cho đã chạy trong thời gian dài, nhưng nó vẫn cần các lập trình viên thực hiện việc nâng cấp phần mềm này.
Trong cuốn sách này, chúng tôi sẽ dạy cho bạn về những điều căn bản nhất về học máy, đặc biệt là học sâu, đó là một bộ các kĩ thuật tiên tiến, giúp thúc đẩy sự đổi mới ở nhiều lĩnh vực như xử lý ảnh, xử lý ngôn ngữ, chăm sóc y tế và nghiên cứu cấu trúc gen.



<!-- =================== Kết thúc dịch Phần 1 ==================== -->

<!-- =================== Bắt đầu dịch Phần 2 ==================== -->

<!--
## A Motivating Example
-->

## *dịch tiêu đề phía trên*

## Một ví dụ điển hình


<!--
Before we could begin writing, the authors of this book,
like much of the work force, had to become caffeinated.
We hopped in the car and started driving.
Using an iPhone, Alex called out "Hey Siri",
awakening the phone's voice recognition system.
Then Mu commanded "directions to Blue Bottle coffee shop".
The phone quickly displayed the transcription of his command.
It also recognized that we were asking for directions
and launched the Maps application to fulfill our request.
Once launched, the Maps app identified a number of routes.
Next to each route, the phone displayed a predicted transit time.
While we fabricated this story for pedagogical convenience,
it demonstrates that in the span of just a few seconds,
our everyday interactions with a smart phone
can engage several machine learning models.
-->

*dịch đoạn phía trên*

Trước khi bắt đầu, chúng tôi cũng giống như phần lớn các lực lượng lao động phổ thông hiện nay. Chúng tôi nhảy lên và bắt đầu lái xe. Sử dụng iPhone, Alex gọi "Hey Siri",  để đánh thức hệ thống nhận dạng giọng nói của điện thoại. Sau đó, Mu ra lệnh "chỉ đường đến quán cà phê Blue Bottle ".
Điện thoại nhanh chóng phân tích âm thanh của anh ấy. Nó cũng nhận ra rằng chúng tôi đã yêu cầu chỉ đường và khởi động ứng dụng Bản đồ để thực hiện yêu cầu của chúng tôi.
Sau khi hoạt động, ứng dụng Bản đồ đã xác định một số tuyến đường. Bên cạnh mỗi tuyến đường, điện thoại hiển thị thêm thời gian di chuyển dự kiến.
Mặc dù đây là câu chuyện không có thật nhưng chúng tôi đã tạo ra để nhấn mạnh về ứng dụng của học máy cho điện thoại di động


<!--
Imagine just writing a program to respond to a *wake word*
like "Alexa", "Okay, Google" or "Siri".
Try coding it up in a room by yourself
with nothing but a computer and a code editor,
as illustrated in :numref:`fig_wake_word`.
How would you write such a program from first principles?
Think about it... the problem is hard.
Every second, the microphone will collect roughly 44,000 samples.
Each sample is a measurement of the amplitude of the sound wave.
What rule could map reliably from a snippet of raw audio to confident predictions ``{yes, no}`` on whether the snippet contains the wake word?
If you are stuck, do not worry.
We do not know how to write such a program from scratch either.
That is why we use ML.
-->

*dịch đoạn phía trên*

Hãy tưởng tượng chỉ cần viết một chương trình để trả lời từ * đánh thức * như "Alexa", "Được rồi, Google" hoặc "Siri".
Hãy thử tự mình viết code mà không có gì ngoài máy tính và trình chỉnh sửa mã, như được minh họa trong: numref: `fig_wake_word`.
Làm thế nào bạn sẽ viết một chương trình như vậy từ các nguyên tắc đầu tiên? Hãy suy nghĩ về nó ... đây là vấn đề khó.
Mỗi giây, điện thoại có thể thu thập khoảng 44.000 mẫu. Mỗi mẫu là một phép đo biên độ của sóng âm.
Quy tắc nào có thể ánh xạ âm thanh ban đầu thành các dự đoán tin cậy để xác định `` {có hay không có} `` từ đánh thức trong lời nói gốc? Nếu bạn bị mắc kẹt, đừng lo lắng.
Chúng tôi cũng không biết cách viết một chương trình như vậy từ đầu. 
Đó là lý do tại sao chúng tôi sử dụng học máy.


<!--
![Identify an awake word.](../img/wake-word.svg)
-->

![*dịch chú thích ảnh phía trên*](../img/wake-word.svg)
:label:`fig_wake_word`

[Xác định từ * đánh thức * ở trên.] (../ img / Wake-word.svg)


<!--
Here's the trick.
Often, even when we do not know how to tell a computer
explicitly how to map from inputs to outputs,
we are nonetheless capable of performing the cognitive feat ourselves.
In other words, even if you do not know
*how to program a computer* to recognize the word "Alexa",
you yourself *are able* to recognize the word "Alexa".
Armed with this ability, we can collect a huge *dataset*
containing examples of audio and label those that *do*
and that *do not* contain the wake word.
In the ML approach, we do not attempt to design a system
*explicitly* to recognize wake words.
Instead, we define a flexible program
whose behavior is determined by a number of *parameters*.
Then we use the dataset to determine the best possible set of parameters, those that improve the performance of our program
with respect to some measure of performance on the task of interest.
-->

*dịch đoạn phía trên*

Đây là mẹo. Thường, ngay cả khi chúng ta không biết rõ về cách máy tính ánh xạ từ đầu vào đến đầu ra, nhưng chúng ta vẫn có khả năng nhận thức về việc này.
Nói cách khác, ngay cả khi bạn không biết * cách lập trình máy tính * để nhận ra từ "Alexa", nhưng bản than bạn * có thể * nhận ra từ "Alexa".
Với khả năng này, chúng tôi có thể thu thập một lượng dữ liệu * khổng lồ * chứa các ví dụ về âm thanh và gắn nhãn cho những hành động * thực hiện* và * không thực hiện* khi từ đánh thức xuất hiện
Theo cách tiếp cận của học máy, chúng tôi không cố gắng thiết kế một hệ thống * rõ ràng * để nhận ra từ đánh thức.
Thay vào đó, chúng tôi định nghĩa một chương trình linh hoạt mà hành vi của nó được xác định bởi một số * tham số *.
Sau đó, chúng tôi sử dụng bộ dữ liệu để xác định bộ tham số tốt nhất có thể, những tham số này cải thiện hiệu suất của chương trình theo hiệu năng thực hiện công việc.


<!--
You can think of the parameters as knobs that we can turn,
manipulating the behavior of the program.
Fixing the parameters, we call the program a *model*.
The set of all distinct programs (input-output mappings)
that we can produce just by manipulating the parameters
is called a *family* of models.
And the *meta-program* that uses our dataset
to choose the parameters is called a *learning algorithm*.
-->

*dịch đoạn phía trên*

Bạn có thể nghĩ về các tham số như các nút mà chúng ta có thể xoay, điều khiển hành vi của chương trình. Khi chọn được tham số, chúng ta có được * mô hình *.
Tập hợp tất cả các chương trình riêng biệt (ánh xạ đầu vào-đầu ra) mà chúng ta có thể tạo ra chỉ bằng cách điều chỉnh các tham số được gọi là * họ * của các mô hình.
Và * chương trình meta * sử dụng tập dữ liệu của chúng tôi để chọn ra các tham số được gọi là * thuật toán học tập *.


<!-- =================== Kết thúc dịch Phần 2 ==================== -->

<!-- =================== Bắt đầu dịch Phần 3 ==================== -->

<!--
Before we can go ahead and engage the learning algorithm,
we have to define the problem precisely,
pinning down the exact nature of the inputs and outputs,
and choosing an appropriate model family.
In this case, our model receives a snippet of audio as *input*,
and it generates a selection among ``{yes, no}`` as *output*.
If all goes according to plan the model's guesses will
typically be correct as to whether (or not) the snippet contains the wake word.
-->

*dịch đoạn phía trên*


Trước khi chúng ta có thể tiếp tục và tham gia vào thuật toán học tập, chúng ta phải xác định chính xác vấn đề, xác định chính xác bản chất của đầu vào và đầu ra và chọn một họ mô hình phù hợp. 
Trong trường hợp này, mô hình của chúng tôi nhận được một đoạn âm thanh dưới dạng * input * và nó tạo ra một lựa chọn trong số `` {yes, no} `` như là * đầu ra *. 
Nếu tất cả diễn ra theo kế hoạch, việc dự đoán mô hình thường chính xác, có (hay không có) từ đánh thức.


<!--
If we choose the right family of models,
then there should exist one setting of the knobs
such that the model fires ``yes`` every time it hears the word "Alexa".  Because the exact choice of the wake word is arbitrary,
we will probably need a model family sufficiently rich that,
via another setting of the knobs, it could fire ``yes``
only upon hearing the word "Apricot".
We expect that the same model family should be suitable
for *"Alexa" recognition* and *"Apricot" recognition*
because they seem, intuitively, to be similar tasks.
However, we might need a different family of models entirely
if we want to deal with fundamentally different inputs or outputs,
say if we wanted to map from images to captions,
or from English sentences to Chinese sentences.
-->

*dịch đoạn phía trên*

Nếu chúng ta chọn đúng họ mô hình, thì sẽ tồn tại một mô hình cho phép kích hoạt khi nghe thấy từ "Alexa". Do lựa chọn chính xác từ đánh thức là tùy ý, chúng ta sẽ cần một họ mẫu có tính đa dạng cao, thông qua nhiều thiết lập, để có thể kích hoạt khi nghe từ "Apricot".
Chúng tôi hy vọng rằng cùng một họ gia đình phù hợp sẽ có đủ khả năng nhận dạng * "Alexa" * và * "Apricot" * do sự tương đồng của chúng.
Tuy nhiên, chúng ta có thể cần một họ mô hình hoàn toàn khác nếu chúng ta muốn xử lý các đầu vào hoặc đầu ra khác nhau rõ rệt, chẳng hạn như chúng ta muốn ánh xạ từ hình ảnh sang chú thích hoặc từ câu tiếng Anh sang câu tiếng Trung.


<!--
As you might guess, if we just set all of the knobs randomly,
it is not likely that our model will recognize "Alexa",
"Apricot", or any other English word.
In deep learning, the *learning* is the process
by which we discover the right setting of the knobs
coercing the desired behavior from our model.
-->

*dịch đoạn phía trên*

Như bạn có thể đoán, nếu chúng ta chỉ đặt ngẫu nhiên tất cả các tham số, mô hình sẽ không nhận ra được từ "Alexa", "Apricot", hoặc bất kỳ từ tiếng Anh nào khác.
Trong học sâu, * học * là quá trình chúng ta khám phá các thiết lập đúng buộc mô hình thực hiện những hành vi như chúng ta mong muốn


<!--
As shown in :numref:`fig_ml_loop`, the training process usually looks like this:
-->

*dịch đoạn phía trên*


Như được hiển thị trong: numref: `fig_ml_loop`, quá trình đào tạo thường trông như thế này:


<!--
1. Start off with a randomly initialized model that cannot do anything useful.
1. Grab some of your labeled data (e.g., audio snippets and corresponding ``{yes, no}`` labels)
1. Tweak the knobs so the model sucks less with respect to those examples
1. Repeat until the model is awesome.
-->

*dịch đoạn phía trên*

1. Bắt đầu với một mô hình khởi tạo ngẫu nhiên, nó  không thể dự báo bất cứ điều gì.
1. Lấy một số dữ liệu được bạn gắn nhãn (ví dụ: đoạn âm thanh và các nhãn tương ứng `` {yes, no} ``)
1. Tinh chỉnh các tham số để hạn chế dữ liệu đầu vào cho mô hình
1. Lặp lại cho đến khi có được mô hình mong muốn.


<!--
![A typical training process. ](../img/ml-loop.svg)
-->

![*dịch chú thích ảnh phía trên*](../img/ml-loop.svg)
:label:`fig_ml_loop`


[Tiến trình đào tạo điển hình] (../ img / ml-loop.svg)


<!-- =================== Kết thúc dịch Phần 3 ==================== -->

<!-- =================== Bắt đầu dịch Phần 4 ==================== -->

<!--
To summarize, rather than code up a wake word recognizer,
we code up a program that can *learn* to recognize wake words,
*if we present it with a large labeled dataset*.
You can think of this act of determining a program's behavior
by presenting it with a dataset as *programming with data*.
We can "program" a cat detector by providing our machine learning system
with many examples of cats and dogs, such as the images below:
-->

*dịch đoạn phía trên*

Để tóm tắt, thay vì mã hóa một bộ nhận dạng từ đánh thức, chúng tôi mã hóa một chương trình có thể * học * để nhận ra các từ đánh thức, * nếu chúng tôi trình bày nó với một tập dữ liệu lớn có nhãn *.
Bạn có thể nghĩ về hành động xác định hành vi của chương trình bằng cách mô tả nó với bộ dữ liệu dưới dạng * lập trình với dữ liệu *.
Chúng ta có thể "lập trình" để nhận dạng mèo bằng cách cung cấp cho hệ thống máy học của chúng ta nhiều ví dụ về mèo và chó, chẳng hạn như các hình ảnh dưới đây:


<!--
| ![cat1](../img/cat1.png) | ![cat2](../img/cat2.jpg) | ![dog1](../img/dog1.jpg) |![dog2](../img/dog2.jpg) |
|:---------------:|:---------------:|:---------------:|:---------------:|
|cat|cat|dog|dog|
-->

*dịch đoạn phía trên*

<!--
| ![cat1](../img/cat1.png) | ![cat2](../img/cat2.jpg) | ![dog1](../img/dog1.jpg) |![dog2](../img/dog2.jpg) |
|:---------------:|:---------------:|:---------------:|:---------------:|
|cat|cat|dog|dog|
-->


<!--
This way the detector will eventually learn to emit a very large positive number if it is a cat, a very large negative number if it is a dog,
and something closer to zero if it is not sure,
and this barely scratches the surface of what ML can do.
-->

*dịch đoạn phía trên*

Bằng cách này, bộ nhận dạng sẽ học cách cho một kết quả dương lớn khi nó nhận ra đó là mèo, một số âm lớn nếu đó là chó và một cái gì đó gần bằng 0 nếu không chắc chắn, và điều này hầu như không làm ảnh hưởng tới những công việc của học máy.


<!--
Deep learning is just one among many popular methods
for solving machine learning problems.
Thus far, we have only talked about machine learning broadly
and not deep learning. To see why deep learning is important,
we should pause for a moment to highlight a couple crucial points.
-->

*dịch đoạn phía trên*

Học sâu chỉ là một trong nhiều phương pháp phổ biến để giải quyết các vấn đề về máy học.
Nhưng cho đến nay, chúng ta chỉ nói nhiều về học máy, nhưng không nói nhiều về học sâu. Để xem tại sao học sâu là quan trọng, chúng ta nên tạm dừng một lát để làm rõ một vài điểm quan trọng.


<!--
First, the problems that we have discussed thus far---learning
from raw audio signal, the raw pixel values of images,
or mapping between sentences of arbitrary lengths and
their counterparts in foreign languages---are problems
where deep learning excels and where traditional ML methods faltered.
Deep models are *deep* in precisely the sense
that they learn many *layers* of computation.
It turns out that these many-layered (or hierarchical) models
are capable of addressing low-level perceptual data
in a way that previous tools could not.
In bygone days, the crucial part of applying ML to these problems
consisted of coming up with manually-engineered ways
of transforming the data into some form amenable to *shallow* models.
One key advantage of deep learning is that it replaces not
only the *shallow* models at the end of traditional learning pipelines,
but also the labor-intensive process of feature engineering.
Second, by replacing much of the *domain-specific preprocessing*,
deep learning has eliminated many of the boundaries
that previously separated computer vision, speech recognition,
natural language processing, medical informatics, and other application areas,
offering a unified set of tools for tackling diverse problems.
-->

*dịch đoạn phía trên*

Đầu tiên, các vấn đề mà chúng ta đã thảo luận từ trước đến nay --- học từ tín hiệu âm thanh gốc, giá trị pixel của hình ảnh gốc hoặc ánh xạ giữa các câu có độ dài tùy ý và các đối tác của chúng bằng tiếng nước ngoài --- là những vấn đề mà học sâu đã giải quyết tốt hơn nhiều so với phương pháp học máy truyền thống.
Trong các mô hình này, thì * deep - sâu * được hiểu chính xác theo nghĩa là chúng học nhiều * lớp *. Nó chỉ ra rằng các mô hình nhiều lớp này (hoặc phân cấp) có khả năng giải quyết dữ liệu nhận thức ở mức thấp theo cách mà các công cụ trước đây không thể.
Trong những ngày qua, phần quan trọng của việc áp dụng học máy cho các vấn đề này bao gồm việc đưa ra các cách chuyển đổi dữ liệu trong một số dạng có thể hiệu chỉnh thành các mô hình nông “shallow model”     
Một điểm thuận lợi chính của học sâu không chỉ là nó thay thế các mô hình * nông * ở bước cuối của tiến trình đào tạo mà nó còn giảm tải cho quá trình trích chọn đặc trưng (feature engineering).
Thứ hai, bằng cách thay thế phần lớn việc xác định domain khi tiền xử lý (domain-specific preprocessing), học sâu đã loại bỏ nhiều hạn chế trong việc xử lý ảnh, nhận dạng giọng nói, xử lý ngôn ngữ tự nhiên, tin học y tế và các lĩnh vực ứng dụng khác, đưa ra một bộ công cụ thống nhất để giải quyết nhiều vấn đề.


<!-- =================== Kết thúc dịch Phần 4 ==================== -->

<!-- =================== Bắt đầu dịch Phần 5 ==================== -->

<!--
## The Key Components: Data, Models, and Algorithms
-->

## *dịch tiêu đề phía trên*

Các thành phần chính: Dữ liệu, Mô hình và Thuật toán


<!--
In our *wake-word* example, we described a dataset
consisting of audio snippets and binary labels
gave a hand-wavy sense of how we might *train*
a model to approximate a mapping from snippets to classifications.
This sort of problem, where we try to predict a designated unknown *label*
given known *inputs*, given a dataset consisting of examples,
for which the labels are known is called *supervised learning*,
and it is just one among many *kinds* of machine learning problems.
In the next section, we will take a deep dive into the different ML problems.
First, we'd like to shed more light on some core components
that will follow us around, no matter what kind of ML problem we take on:
-->

*dịch đoạn phía trên*

Trong ví dụ nhận dạng từ đánh thức * Wake-word *, chúng tôi đã mô tả một tập dữ liệu bao gồm các đoạn âm thanh và nhãn nhị phân để tạo ảo giác  về cách chúng tôi có thể huấn luyện một mô hình để ước tính ánh xạ từ trích chọn đến phân loại.
Loại vấn đề này, ở đó chúng tôi cố gắng dự đoán một nhãn * không xác định * được gắn với các đầu vào xác định, cung cấp một tập dữ liệu bao gồm các ví dụ, trong đó các nhãn xác định được gọi là * học có giám sát *, và nó chỉ là một trong số rất nhiều * các loại * của vấn đề học máy.
Trong phần tiếp theo, chúng ta sẽ đi sâu vào các vấn đề học máy khác nhau. Đầu tiên, chúng tôi muốn làm sáng tỏ hơn về một số thành phần cốt lõi của học máy


<!--
1. The *data* that we can learn from.
2. A *model* of how to transform the data.
3. A *loss* function that quantifies the *badness* of our model.
4. An *algorithm* to adjust the model's parameters to minimize the loss.
-->

*dịch đoạn phía trên*

1. Dữ liệu * mà chúng ta có thể học.
2. Mô hình * chuyển đổi dữ liệu như thế nào
3. Hàm tổn thất (loss) để định lượng phần không ổn (badness) trong mô hình.
4. Một thuật toán nhằm điều chỉnh các tham số của mô hình để giảm thiểu tổn thất.


<!--
### Data
-->

### *dịch tiêu đề phía trên*

Dữ liệu


<!--
It might go without saying that you cannot do data science without data.
We could lose hundreds of pages pondering what precisely constitutes data,
but for now we will err on the practical side
and focus on the key properties to be concerned with.
Generally we are concerned with a collection of *examples*
(also called *data points*, *samples*, or *instances*).
In order to work with data usefully, we typically
need to come up with a suitable numerical representation.
Each *example* typically consists of a collection
of numerical attributes called *features*.
In the supervised learning problems above,
a special feature is designated as the prediction *target*,
(sometimes called the *label* or *dependent variable*).
The given features from which the model must make its predictions
can then simply be called the *features*,
(or often, the *inputs*, *covariates*, or *independent variables*).
-->

*dịch đoạn phía trên*

Có thể nói rằng bạn không thể làm khoa học dữ liệu (data science) mà không có dữ liệu. Chúng tôi có thể mất hàng trăm trang để suy nghĩ chính xác những gì cấu thành dữ liệu, nhưng bây giờ chúng tôi sẽ xem khía cạnh thực tế và tập trung vào các thuộc tính quan trọng cần quan tâm.
Nói chung, chúng tôi quan tâm đến một tập hợp * ví dụ * (còn được gọi là * các điểm dữ liệu - data points *, * mẫu - samples * hoặc * các trường hợp cụ thể - instances *).
Để làm việc với dữ liệu một cách hữu ích, thông thường chúng ta cần đưa ra một biểu diễn số phù hợp.
Mỗi * ví dụ * thường bao gồm một tập các thuộc tính số được gọi là đặc trưng (features). Trong các vấn đề học tập có giám sát ở trên, một tính năng đặc biệt được chỉ định là dự đoán mục tiêu (target), (đôi khi được gọi là * nhãn - label* hoặc * biến phụ thuộc - dependent variable *).
Các tính năng đã cho từ mô hình phải đưa ra dự đoán của nó sau đó có thể được gọi một cách đơn giản là đặc trưng, (hoặc thường là * đầu vào *, * đồng biến - covariates * hoặc * biến độc lập - independent variables *).


<!--
If we were working with image data,
each individual photograph might constitute an *example*,
each represented by an ordered list of numerical values
corresponding to the brightness of each pixel.
A $200\times 200$ color photograph would consist of $200\times200\times3=120000$
numerical values, corresponding to the brightness
of the red, green, and blue channels for each spatial location.
In a more traditional task, we might try to predict
whether or not a patient will survive,
given a standard set of features such as age, vital signs, diagnoses, etc.
-->

*dịch đoạn phía trên*

Nếu chúng tôi đang làm việc với dữ liệu ảnh, mỗi bức ảnh riêng lẻ có thể tạo thành một * ví dụ *, mỗi bức ảnh được biểu thị bằng một danh sách các giá trị số tương ứng với độ sáng của từng pixel.
Một bức ảnh màu $ 200 \ lần 200 $ ($200\times 200$ color photograph) sẽ bao gồm $ 200 \ times200 \ times3 ($200\times200\times3) = 120000 $ giá trị số, tương ứng với độ sáng của các kênh màu đỏ, xanh lục và xanh lam cho mỗi vị trí không gian.
Trong một nhiệm vụ truyền thống hơn, chúng tôi cố gắng dự đoán một bệnh nhân sẽ sống hay không, được cung cấp bởi một số tính năng tiêu chuẩn như tuổi, các dấu hiệu quan trọng, chẩn đoán, v.v.


<!-- =================== Kết thúc dịch Phần 5 ==================== -->

<!-- =================== Bắt đầu dịch Phần 6 ==================== -->

<!--
When every example is characterized by the same number of numerical values,
we say that the data consists of *fixed-length* vectors
and we describe the (constant) length of the vectors
as the *dimensionality* of the data.
As you might imagine, fixed length can be a convenient property.
If we wanted to train a model to recognize cancer in microscopy images,
fixed-length inputs means we have one less thing to worry about.
-->

*dịch đoạn phía trên*

Khi mọi ví dụ được đặc trưng bởi cùng một số giá trị số, chúng tôi nói rằng dữ liệu gồm các vectơ * chiều dài cố định (fixed-length) và chúng tôi mô tả độ dài (không đổi) của vectơ như là * chiều - dimensionality * của dữ liệu.
Như bạn có thể tưởng tượng, chiều dài cố định có thể là một thuộc tính tiện lợi. Nếu chúng ta muốn đào tạo một mô hình để nhận biết ung thư trong hình ảnh kính hiển vi, đầu vào có độ dài cố định có nghĩa là chúng ta có ít đi một điều phải lo lắng.


<!--
However, not all data can easily be represented as fixed length vectors.
While we might expect microscope images to come from standard equipment,
we cannot expect images mined from the Internet
to all show up with the same resolution or shape.
For images, we might consider cropping them all to a standard size,
but that strategy only gets us so far.
We risk losing information in the cropped out portions.
Moreover, text data resists fixed-length representations even more stubbornly.
Consider the customer reviews left on e-commerce sites
like Amazon, IMDB, or TripAdvisor.
Some are short: "it stinks!". Others ramble for pages.
One major advantage of deep learning over traditional methods
is the comparative grace with which modern models
can handle *varying-length* data.
-->

*dịch đoạn phía trên*

Tuy nhiên, không phải tất cả dữ liệu có thể dễ dàng được biểu diễn dưới dạng vectơ có chiều dài cố định. Mặc dù chúng ta có được các dữ liệu ảnh từ kính hiển tiêu chuẩn, nhưng chúng ta không thể dùng hình ảnh trên Internet sẽ hiển thị với cùng độ phân giải hoặc kích cỡ.
Đối với hình ảnh, chúng tôi có thể điều chỉnh để đưa chúng về cùng một kích thước, nhưng cách làm này không đưa chúng ta đến những kết quả như mong muốn. Có thể, chúng ta sẽ mất thông tin trong các phần bị cắt.
Hơn nữa, dữ liệu văn bản thường không phù hợp với cách biểu diễn có độ dài cố định. Kiểu như các đánh giá của khách hàng để lại trên các trang web thương mại điện tử như Amazon, IMDB hoặc TripAdvisor.
Nói ngắn gọn: "nó bốc mùi!". Những người khác lan man trên các trang. Một điểm thuận lợi chính của học sâu so với các phương pháp truyền thống là khả năng xử lý dữ liệu có độ dài biến đổi (varying-length).


<!--
Generally, the more data we have, the easier our job becomes.
When we have more data, we can train more powerful models,
and rely less heavily on pre-conceived assumptions.
The regime change from (comparatively small) to big data
is a major contributor to the success of modern deep learning.
To drive the point home, many of the most exciting models in deep learning either do not work without large datasets.
Some others work in the low-data regime,
but no better than traditional approaches.
-->

*dịch đoạn phía trên*

Nói chung, chúng ta càng có nhiều dữ liệu, công việc của chúng ta càng trở nên dễ dàng hơn. Khi chúng ta có nhiều dữ liệu hơn, chúng ta có thể đào tạo nhiều mô hình tốt hơn và ít phụ thuộc hơn vào các giả định được hình thành từ trước.
Sự thay đổi chế độ từ (tương đối nhỏ) sang dữ liệu lớn là một đóng góp chính cho sự thành công của học sâu hiện đại. Nhiều mô hình học sâu tiên tiến không hoạt động nếu không có bộ dữ liệu lớn. Còn ở chế độ ít dữ liệu (low-data regime), nó không tốt hơn các phương pháp học máy truyền thống.


<!--
Finally it is not enough to have lots of data and to process it cleverly.
We need the *right* data. If the data is full of mistakes,
or if the chosen features are not predictive
of the target quantity of interest, learning is going to fail.
The situation is captured well by the cliché: *garbage in, garbage out*.
Moreover, poor predictive performance is not the only potential consequence.
In sensitive applications of machine learning,
like predictive policing, resumé screening, and risk models used for lending,
we must be especially alert to the consequences of garbage data.
One common failure mode occurs in datasets where some groups of people
are unrepresented in the training data.
Imagine applying a skin cancer recognition system in the wild
that had never seen black skin before.
Failure can also occur when the data
does not merely under-represent some groups,
but reflects societal prejudices.
For example if past hiring decisions are used to train a predictive model
that will be used to screen resumes,
then machine learning models could inadvertently
capture and automate historical injustices.
Note that this can all happen without the data scientist
actively conspiring, or even being aware.
-->

*dịch đoạn phía trên*

Cuối cùng, khi không đủ dữ liệu, chúng ta phải xử lý nó một cách khéo léo. Chúng ta cần đúng dữ liệu. Nếu dữ liệu có nhiều lỗi, hoặc nếu các tính năng được chọn không phù hợp với mục tiêu dự đoán, việc học sẽ thất bại. Kiểu như * rác vào, rác ra *. Hơn nữa, điều này cũng ảnh hưởng tới hiệu suất dự báo.
Trong các ứng dụng nhạy cảm của học máy, như kiểm soát dự đoán, sàng lọc liên tục và mô hình đánh giá rủi ro trong ngân hàng, chúng ta phải đặc biệt cảnh giác với hậu quả của dữ liệu rác.
Một trong các nguyên nhân thất bại hay xảy ra là do việc tạo dữ liệu để đưa vào đào tạo 
Hãy tưởng tượng áp dụng một hệ thống nhận dạng ung thư da trong tự nhiên mà chưa từng có dữ liệu của người da màu.
Thất bại cũng có thể xảy ra khi dữ liệu không chỉ đại diện cho một số nhóm, mà phản ánh định kiến xã hội.
Ví dụ: nếu các quyết định tuyển dụng trong quá khứ được sử dụng để huấn luyện một mô hình dự đoán sẽ được sử dụng để sàng lọc sơ yếu lý lịch, thì các mô hình học máy có thể vô tình nắm bắt và tự động hóa những bất công lịch sử.
Lưu ý rằng tất cả các điều này có thể xảy ra do sự chủ quan hoặc không nhận thức được của các nhà khoa học dữ liệu


<!-- =================== Kết thúc dịch Phần 6 ==================== -->

<!-- =================== Bắt đầu dịch Phần 7 ==================== -->

<!--
### Models
-->

### *dịch tiêu đề phía trên*

### Mô hình


<!--
Most machine learning involves *transforming* the data in some sense.
We might want to build a system that ingests photos and predicts *smiley-ness*.
Alternatively, we might want to ingest a set of sensor readings
and predict how *normal* vs *anomalous* the readings are.
By *model*, we denote the computational machinery for ingesting data
of one type, and spitting out predictions of a possibly different type.
In particular, we are interested in statistical models
that can be estimated from data.
While simple models are perfectly capable of addressing
appropriately simple problems the problems
that we focus on in this book stretch the limits of classical methods.
Deep learning is differentiated from classical approaches
principally by the set of powerful models that it focuses on.
These models consist of many successive transformations of the data
that are chained together top to bottom, thus the name *deep learning*.
On our way to discussing deep neural networks,
we will discuss some more traditional methods.
-->

*dịch đoạn phía trên*

Thường, học máy được hiểu theo nghĩa biến đổi (transforming) dữ liệu theo một bối cảnh (sense) nào đó. Chúng tôi có thể muốn để xây dựng một hệ thống nhận dạng ảnh và dự đoán * mặt cười *. Ngoài ra, chúng tôi có thể muốn sử dụng một tập hợp các dữ liệu nhận dạng giọng nói và dự đoán mức độ * bình thường * so với * dị thường * của các bài đọc.
Bằng mô hình * model *, chúng ta có thể đưa dữ liệu một loại và đưa ra dự đoán về một loại khác. 
Đặc biệt, chúng tôi quan tâm tới việc ước tính các mô hình thống kê có thể được từ dữ liệu.
 Trong khi các mô hình đơn giản hoàn toàn có khả năng giải quyết các vấn đề đơn giản một cách phù hợp, các vấn đề mà chúng tôi tập trung vào cuốn sách này đã mở rộng giới hạn cho các phương pháp cổ điển.
Học sâu được phân biệt với các phương pháp cổ điển chủ yếu bằng tập hợp các mô hình mạnh mẽ mà nó tập trung vào.
Các mô hình này bao gồm nhiều biến đổi liên tiếp của dữ liệu được nối với nhau từ trên xuống, do đó nó có tên là * học sâu *.
Trên đường thảo luận về các mạng lưới thần kinh sâu sắc, chúng ta sẽ thảo luận về một số phương pháp truyền thống.


<!--
###  Objective functions
-->

### *dịch tiêu đề phía trên*

###  Các hàm mục tiêu

<!--
Earlier, we introduced machine learning as "learning from experience".
By *learning* here, we mean *improving* at some task over time.
But who is to say what constitutes an improvement?
You might imagine that we could propose to update our model,
and some people might disagree on whether the proposed update
constituted an improvement or a decline.
-->

*dịch đoạn phía trên*

Trước đó, chúng tôi đã giới thiệu học máy là "học hỏi kinh nghiệm". Bằng cách * học * ở đây, chúng tôi có nghĩa là * cải thiện * một số nhiệm vụ theo thời gian.
Nhưng ai là người nói điều gì tạo nên sự cải tiến? Bạn có thể tưởng tượng rằng chúng tôi có thể đề xuất cập nhật mô hình của mình và một số người có thể không đồng ý về việc liệu bản cập nhật được đề xuất có tạo ra sự cải thiện hay không.


<!--
In order to develop a formal mathematical system of learning machines,
we need to have formal measures of how good (or bad) our models are.
In machine learning, and optimization more generally,
we call these objective functions.
By convention, we usually define objective functions
so that *lower* is *better*.
This is merely a convention. You can take any function $f$
for which higher is better, and turn it into a new function $f'$
that is qualitatively identical but for which lower is better
by setting $f' = -f$.
Because lower is better, these functions are sometimes called
*loss functions* or *cost functions*.
-->

*dịch đoạn phía trên*

Để phát triển một hệ thống tính toán chính thức của máy học, chúng ta cần có các biện pháp đo kiểm mức độ tốt (hoặc xấu) của các mô hình.
Trong học máy, và tối ưu hóa nói chung, chúng ta gọi đó là các hàm mục tiêu.
Theo quy ước, chúng ta thường định nghĩa các hàm mục tiêu có giá trị * thấp hơn * sẽ * tốt hơn *.
Đây chỉ đơn thuần là một quy ước. Bạn có thể nhận bất kỳ hàm nào $ f $ với mức cao hơn là tốt hơn và biến nó thành hàm mới $ f '$ giống hệt nhau về mặt chất lượng nhưng với mức thấp hơn thì tốt hơn bằng cách đặt $ f' = -f $.
Vì thấp hơn là tốt hơn, các hàm này đôi khi được gọi là * hàm tổn thất * hoặc * hàm chi phí *.


<!-- =================== Kết thúc dịch Phần 7 ==================== -->

<!-- =================== Bắt đầu dịch Phần 8 ==================== -->

<!--
When trying to predict numerical values,
the most common objective function is squared error $(y-\hat{y})^2$.
For classification, the most common objective is to minimize error rate,
i.e., the fraction of instances on which
our predictions disagree with the ground truth.
Some objectives (like squared error) are easy to optimize.
Others (like error rate) are difficult to optimize directly,
owing to non-differentiability or other complications.
In these cases, it is common to optimize a *surrogate objective*.
-->

*dịch đoạn phía trên*

Khi cố gắng dự đoán các giá trị số, hàm mục tiêu phổ biến nhất là lỗi bình phương $ (y- \ hat {y}) ^ 2 $.
Để phân loại, mục tiêu chung nhất là giảm thiểu tỷ lệ lỗi, tức là tỷ lệ các trường hợp ở đó dự đoán của chúng tôi không đồng ý với dữ liệu vào.
Một số mục tiêu (như lỗi bình phương) rất dễ tối ưu hóa. Những người khác (như tỷ lệ lỗi) rất khó để tối ưu hóa trực tiếp, do không khác biệt hoặc các biến chứng khác.
Trong những trường hợp này, thông thường để tối ưu hóa một mục tiêu * thay thế - surrogate objective*.


<!--
Typically, the loss function is defined
with respect to the model's parameters
and depends upon the dataset.
The best values of our model's parameters are learned
by minimizing the loss incurred on a *training set*
consisting of some number of *examples* collected for training.
However, doing well on the training data
does not guarantee that we will do well on (unseen) test data.
So we will typically want to split the available data into two partitions:
the training data (for fitting model parameters)
and the test data (which is held out for evaluation),
reporting the following two quantities:
-->

*dịch đoạn phía trên*

Thông thường, hàm mất được xác định theo các tham số của mô hình và phụ thuộc vào tập dữ liệu.
Các giá trị tốt nhất của các tham số mô hình được học bằng cách giảm thiểu tổn thất phát sinh trên * tập huấn luyện * bao gồm một số * ví dụ * được thu thập để đào tạo.
Tuy nhiên, làm tốt trên dữ liệu đào tạo không đảm bảo rằng chúng tôi sẽ làm tốt trên tập dữ liệu thử nghiệm (chưa biết trước).
Vì vậy, chúng tôi thường muốn chia dữ liệu có sẵn thành hai phân vùng: 
dữ liệu đào tạo (cho các tham số mô hình phù hợp) 
và dữ liệu thử nghiệm (được tổ chức để đánh giá), 
báo cáo hai đại lượng sau:


<!--
 * **Training Error:**
 The error on that data on which the model was trained.
 You could think of this as being like
 a student's scores on practice exams
 used to prepare for some real exam.
 Even if the results are encouraging,
 that does not guarantee success on the final exam.
 * **Test Error:** This is the error incurred on an unseen test set.
 This can deviate significantly from the training error.
 When a model performs well on the training data
 but fails to generalize to unseen data,
 we say that it is *overfitting*.
 In real-life terms, this is like flunking the real exam
 despite doing well on practice exams.
-->

*dịch đoạn phía trên*

Lỗi trên dữ liệu mà mô hình đã được đào tạo. Bạn có thể nghĩ về điều này giống như điểm số của học sinh trong các kỳ thi thực hành được sử dụng để chuẩn bị cho một số kỳ thi thực sự.
Thậm chí, ngay cả khi kết quả rất đáng khích lệ, điều đó không đảm bảo thành công cho kỳ thi cuối cùng.
 * ** Lỗi kiểm tra: ** Đây là lỗi phát sinh trên bộ kiểm tra không biết trước. Nó có thể sai lệch đáng kể so với lỗi đào tạo.
Khi một mô hình thực hiện tốt dữ liệu huấn luyện nhưng không thể khái quát hóa thành dữ liệu chưa biết trước, chúng tôi gọi là * quá mức *.
Trong thực tế, nó giống như làm sai bài kiểm tra thực mặc dù làm tốt bài kiểm tra thử.


<!-- =================== Kết thúc dịch Phần 8 ==================== -->

<!-- =================== Bắt đầu dịch Phần 9 ==================== -->

<!--
### Optimization algorithms
-->

### *dịch tiêu đề phía trên*

### Thuật toán tối ưu


<!--
Once we have got some data source and representation,
a model, and a well-defined objective function,
we need an algorithm capable of searching
for the best possible parameters for minimizing the loss function.
The most popular optimization algorithms for neural networks
follow an approach called gradient descent.
In short, at each step, they check to see, for each parameter,
which way the training set loss would move
if you perturbed that parameter just a small amount.
They then update the parameter in the direction that reduces the loss.
-->

*dịch đoạn phía trên*

Ngay khi chúng tôi đã có một số nguồn dữ liệu, mô tả dữ liệu, một mô hình và một hàm mục tiêu được xác định rõ, chúng ta cần một thuật toán có khả năng tìm kiếm các tham số tốt nhất để tối thiểu giá trị hàm mục tiêu. Các thuật toán tối ưu phổ biến nhất cho các mạng thần kinh (neural networks) theo một cách tiếp cận được gọi là giảm độ dốc. 
Nói tóm lại, ở mỗi bước, họ kiểm tra xem, cho từng tham số, cách tập dữ liệu tổn thất sẽ di chuyển nếu bạn làm nhiễu tham số đó chỉ một lượng nhỏ. Sau đó, họ cập nhật tham số theo hướng giảm tổn thất.


<!--
## Kinds of Machine Learning
-->

## *dịch tiêu đề phía trên*

## Các loại học máy


<!--
In the following sections, we discuss a few *kinds*
of machine learning problems in greater detail.
We begin with a list of *objectives*, i.e.,
a list of things that we would like machine learning to do.
Note that the objectives are complemented
with a set of techniques of *how* to accomplish them,
including types of data, models, training techniques, etc.
The list below is just a sampling of the problems ML can tackle
to motivate the reader and provide us with some common language
for when we talk about more problems throughout the book.
-->

*dịch đoạn phía trên*

Trong các phần sau, chúng tôi thảo luận một vài * loại * vấn đề về học máy một cách chi tiết hơn.
Chúng tôi bắt đầu với một danh sách * mục tiêu *, tức là danh sách những điều mà chúng tôi muốn học máy thực hiện.
Lưu ý rằng các mục tiêu được bổ sung bằng một tập các kỹ thuật để thực hiện chúng như thế nào, bao gồm các loại dữ liệu, mô hình, kỹ thuật đào tạo, vv
Danh sách dưới đây chỉ là một ví dụ về các vấn đề ML có thể giải quyết để thúc đẩy người đọc và đưa ra một số thuật ngữ chung khi chúng ta nói nhiều về vấn đề này hơn trong cuốn sách.


<!-- =================== Kết thúc dịch Phần 9 ==================== -->

<!-- =================== Bắt đầu dịch Phần 10 ==================== -->

<!--
### Supervised learning
-->

### *dịch tiêu đề phía trên*

### Học có giám sát


<!--
Supervised learning addresses the task of
predicting *targets* given *inputs*.
The targets, which we often call *labels*, are generally denoted by *y*.
The input data, also called the *features* or covariates,
are typically denoted $\mathbf{x}$.
Each (input, target) pair is called an *examples* or an *instances*.
Some times, when the context is clear, we may use the term examples,
to refer to a collection of inputs,
even when the corresponding targets are unknown.
We denote any particular instance with a subscript, typically $i$,
for instance ($\mathbf{x}_i, y_i$).
A dataset is a collection of $n$ instances $\{\mathbf{x}_i, y_i\}_{i=1}^n$.
Our goal is to produce a model $f_\theta$ that maps any input $\mathbf{x}_i$
 to a prediction $f_{\theta}(\mathbf{x}_i)$.
-->

*dịch đoạn phía trên*

Học có giám sát giải quyết nhiệm vụ dự đoán * mục tiêu * cho các * đầu vào * đã biết. Các mục tiêu này thường gọi là * nhãn *, thường được ký hiệu là * y *. Dữ liệu đầu vào, còn được gọi là * tính năng - features* hoặc đồng biến, thường được ký hiệu là $ \ mathbf {x} $.
Mỗi cặp (đầu vào, đích) được gọi là một * ví dụ * hoặc * thể hiện - instances *. Đôi khi, trong bối cảnh rõ ràng, chúng tôi có thể sử dụng thuật ngữ “ví dụ”, để chỉ một tập các đầu vào, thậm chí ngay cả khi các mục tiêu tương ứng không xác định.
Ví dụ, chúng tôi biểu thị bất kỳ trường hợp cụ thể nào với một chỉ mục, thường là $ i $ ($ \ mathbf {x} _i, y_i $).
Tập dữ liệu là tập hợp của $ n $ cụ thể $ \ {\ mathbf {x} _i, y_i \} _ {i = 1} ^ n $. Mục tiêu của chúng tôi là tạo ra một mô hình $ f_ \ theta $ ánh xạ mọi đầu vào $ \ mathbf {x} _i $ theo dự đoán $ f _ {\ theta} (\ mathbf {x} _i) $.


<!--
To ground this description in a concrete example,
if we were working in healthcare,
then we might want to predict whether or not
a patient would have a heart attack.
This observation, *heart attack* or *no heart attack*,
would be our label $y$.
The input data $\mathbf{x}$ might be vital signs
such as heart rate, diastolic and systolic blood pressure, etc.
-->

*dịch đoạn phía trên*

Làm rõ mô tả này trong một ví dụ cụ thể, nếu chúng ta làm việc trong lĩnh vực chăm sóc sức khỏe, thì chúng ta có thể muốn dự đoán liệu bệnh nhân có bị đau tim hay không.
Quan sát này, * đau tim * hoặc * không đau tim *,
sẽ là nhãn của chúng tôi $ y $.
Dữ liệu đầu vào $ \ mathbf {x} $ có thể là các dấu hiệu quan trọng như nhịp tim, huyết áp tâm trương và huyết áp tâm thu, v.v.


<!--
The supervision comes into play because for choosing the parameters $\theta$, we (the supervisors) provide the model with a dataset
consisting of *labeled examples* ($\mathbf{x}_i, y_i$),
where each example $\mathbf{x}_i$ is matched with the correct label.
-->

*dịch đoạn phía trên*

Việc giám sát đóng vai trò quan trọng trong việc chọn các tham số $\theta $, chúng tôi (bộ giám sát) cung cấp mô hình với một tập dữ liệu bao gồm * dữ liệu được gắn nhãn * ($ \ mathbf {x} _i, y_i $), ở đó mỗi ví dụ $ \ mathbf {x} _i $ khớp với một đúng nhãn.


<!--
In probabilistic terms, we typically are interested in estimating
the conditional probability $P(y|x)$.
While it is just one among several paradigms within machine learning,
supervised learning accounts for the majority of successful
applications of machine learning in industry.
Partly, that is because many important tasks
can be described crisply as estimating the probability
of something unknown given a particular set of available data:
-->

*dịch đoạn phía trên*

Theo thuật ngữ xác suất, chúng tôi thường quan tâm đến việc ước tính xác suất có điều kiện $ P (y | x) $.
Mặc dù nó chỉ là một trong số nhiều mô hình trong học máy, nhưng học có giám sát lại chiếm phần lớn trong các ứng dụng thành công của học máy trong công nghiệp.
Một phần, đó là bởi vì nhiều nhiệm vụ quan trọng có thể được mô tả rõ ràng khi ước tính xác suất của một cái gì đó chưa biết với một bộ dữ liệu sẵn có


<!--
* Predict cancer vs not cancer, given a CT image.
* Predict the correct translation in French, given a sentence in English.
* Predict the price of a stock next month based on this month's financial reporting data.
-->

*dịch đoạn phía trên*

* Dự đoán ung thư hay không, dựa trên hình ảnh CT.
* Dự đoán bản dịch chính xác bằng tiếng Pháp, đưa ra một câu bằng tiếng Anh.
* Dự đoán giá của một cổ phiếu vào tháng tới dựa trên dữ liệu báo cáo tài chính của tháng này.


<!-- =================== Kết thúc dịch Phần 10 ==================== -->

<!-- =================== Bắt đầu dịch Phần 11 ==================== -->

<!--
Even with the simple description "predict targets from inputs"
supervised learning can take a great many forms
and require a great many modeling decisions,
depending on (among other considerations) the type, size,
and the number of inputs and outputs.
For example, we use different models to process sequences
(like strings of text or time series data)
and for processing fixed-length vector representations.
We will visit many of these problems in depth
throughout the first 9 parts of this book.
-->

*dịch đoạn phía trên*

Ngay cả với mô tả đơn giản "dự đoán mục tiêu từ đầu vào", việc học có giám sát có thể có rất nhiều dạng và yêu cầu nhiều quyết định mô hình hóa, tùy thuộc vào (những vấn đề cần quan tâm) loại, kích cỡ và số lượng của đầu vào và đầu ra.
Ví dụ: chúng tôi sử dụng các mô hình khác nhau để xử lý các chuỗi (như chuỗi văn bản hoặc chuỗi dữ liệu thời gian) và để xử lý các biểu diễn dưới dạng vectơ có chiều dài cố định.
Chúng tôi sẽ đề cập chi tiết về vấn đề này trong 9 phần đầu tiên của cuốn sách.


<!--
Informally, the learning process looks something like this:
Grab a big collection of examples for which the covariates are known
and select from them a random subset,
acquiring the ground truth labels for each.
Sometimes these labels might be available data that has already been collected
(e.g., did a patient die within the following year?)
and other times we might need to employ human annotators to label the data,
(e.g., assigning images to categories).
-->

*dịch đoạn phía trên*

Một cách không chính thức, quá trình học máy sẽ như sau:
Thu thập một lượng lớn các mẫu có hiệp phương biến đã biết và chọn từ chúng một tập con ngẫu nhiên, thu được các nhãn có độ chính xác cao trong quá trình đào tạo (ground truth labels) ở mỗi tập hợp.
Đôi khi các nhãn này có thể là dữ liệu đã thu thập được (ví dụ: bệnh nhân có chết trong năm sau không?) Và những lần khác chúng tôi có thể cần sử dụng các chú thích của con người để gắn nhãn dữ liệu, (ví dụ: gán hình ảnh cho các danh mục).


<!--
Together, these inputs and corresponding labels comprise the training set.
We feed the training dataset into a supervised learning algorithm,
a function that takes as input a dataset
and outputs another function, *the learned model*.
Finally, we can feed previously unseen inputs to the learned model,
using its outputs as predictions of the corresponding label.
The full process in drawn in :numref:`fig_supervised_learning`.
-->

*dịch đoạn phía trên*

Cuối cùng, chúng ta có thể cung cấp các đầu vào không xác định trước cho mô hình đã qua đào tạo, sử dụng các đầu ra của nó làm dự đoán cho các nhãn tương ứng.
Toàn bộ quá trình được mô tả trong: numref: `fig_supervised_learning`.


<!-- =================== Kết thúc dịch Phần 11 ==================== -->

<!-- =================== Bắt đầu dịch Phần 12 ==================== -->

<!--
![Supervised learning.](../img/supervised-learning.svg)
-->

![*dịch chú thích ảnh phía trên*](../img/supervised-learning.svg)
:label:`fig_supervised_learning`

! [Học có giám sát.] (../ img / giám sát-học.svg)


<!--
#### Regression
-->

#### *dịch tiêu đề phía trên*

#### Hồi quy
<!--
Perhaps the simplest supervised learning task
to wrap your head around is *regression*.
Consider, for example a set of data harvested
from a database of home sales.
We might construct a table, where each row corresponds to a different house,
and each column corresponds to some relevant attribute,
such as the square footage of a house, the number of bedrooms, the number of bathrooms, and the number of minutes (walking) to the center of town.
In this dataset each *example* would be a specific house,
and the corresponding *feature vector* would be one row in the table.
-->

*dịch đoạn phía trên*

Có lẽ mô hình học giám sát đơn giản, nhưng quan trọng nhất là * hồi quy *.
Hãy xem một ví dụ về một tập dữ liệu được thu thập từ cơ sở dữ liệu bán hàng tại nhà.
Chúng ta có thể xây dựng một bảng, trong đó mỗi hàng tương ứng với một ngôi nhà khác nhau và mỗi cột tương ứng với một số thuộc tính có liên quan, chẳng hạn như diện tích của ngôi nhà, số phòng ngủ, số phòng tắm và số phút (đi bộ) đến trung tâm thị trấn.
Trong tập dữ liệu này, mỗi * ví dụ * sẽ là một ngôi nhà cụ thể và * vectơ đặc trưng - feature vector * tương ứng sẽ là một hàng trong bảng.


<!--
If you live in New York or San Francisco,
and you are not the CEO of Amazon, Google, Microsoft, or Facebook,
the (sq. footage, no. of bedrooms, no. of bathrooms, walking distance)
feature vector for your home might look something like: $[100, 0, .5, 60]$.
However, if you live in Pittsburgh, it might look more like $[3000, 4, 3, 10]$.
Feature vectors like this are essential
for most classic machine learning algorithms.
We will continue to denote the feature vector correspond
to any example $i$ as $\mathbf{x}_i$ and we can compactly refer
to the full table containing all of the feature vectors as $X$.
-->

*dịch đoạn phía trên*

Nếu bạn sống ở New York hoặc San Francisco và bạn không phải là Giám đốc điều hành của Amazon, Google, Microsoft hoặc Facebook, thì véc tơ đặc trưng (diện tích, số phòng ngủ, phòng tắm, khoảng cách đi bộ) cho ngôi nhà của bạn trông giống như: $ [100, 0, .5, 60] $.
Tuy nhiên, nếu bạn sống ở Pittsburgh, nó có thể trông giống như $ [3000, 4, 3, 10] $. Các vectơ đặc trưng rất cần thiết cho hầu hết các thuật toán học máy cổ điển.
Chúng tôi sẽ tiếp tục biểu thị vectơ đặc trưng tương ứng với bất kỳ ví dụ $ i $ nào như $ \ mathbf {x} _i $ và chúng tôi đưa ra bảng tham khảo ngắn gọn cho các vectơ đặc trưng là $ X $.


<!--
What makes a problem a *regression* is actually the outputs.
Say that you are in the market for a new home.
You might want to estimate the fair market value of a house,
given some features like these.
The target value, the price of sale, is a *real number*.
If you remember the formal definition of the reals
you might be scratching your head now.
Homes probably never sell for fractions of a cent,
let alone prices expressed as irrational numbers.
In cases like this, when the target is actually discrete,
but where the rounding takes place on a sufficiently fine scale,
we will abuse language just a bit cn continue to describe
our outputs and targets as real-valued numbers.
-->

*dịch đoạn phía trên*

Vấn đề * hồi quy * liên quan mật thiết tới các đầu ra. Khi bạn đang tham khảo thị trường nhà đất. Bạn sẽ muốn ước tính giá trị thị trường của một ngôi nhà, có một số tính năng như thế này.
Giá trị mục tiêu, giá bán, là * số thực *. Nếu bạn nhớ định nghĩa về số thực, bạn có thể rất bất ngờ.
Giá bán của các ngôi nhà không bao giờ được biểu diễn ở dạng phân số, chứ đừng nói đến số vô tỷ.
Trong những trường hợp như thế này, khi mục tiêu là các giá trị rời rạc, nhưng ở đó việc làm tròn diễn ra ở thang đo đủ lớn (but where the rounding takes place on a sufficiently fine scale), chúng ta sẽ lạm dụng một chút ngôn ngữ để tiếp tục mô tả kết quả đầu ra và mục tiêu của chúng ta là số có giá trị thực.


<!-- =================== Kết thúc dịch Phần 12 ==================== -->

<!-- =================== Bắt đầu dịch Phần 13 ==================== -->

<!--
We denote any individual target $y_i$
(corresponding to example $\mathbf{x_i}$)
and the set of all targets $\mathbf{y}$
(corresponding to all examples $X$).
When our targets take on arbitrary values in some range,
we call this a regression problem.
Our goal is to produce a model whose predictions
closely approximate the actual target values.
We denote the predicted target for any instance $\hat{y}_i$.
Do not worry if the notation is bogging you down.
We will unpack it more thoroughly in the subsequent chapters.
-->

*dịch đoạn phía trên*

Chúng tôi biểu thị bất kỳ mục tiêu riêng lẻ $ y_i $ (tương ứng với ví dụ $ \ mathbf {x_i} $) và tập hợp tất cả các mục tiêu $ \ mathbf {y} $ (tương ứng với tất cả các ví dụ $ X $).
Khi các mục tiêu nhận các giá trị tùy ý trong một phạm vi nào đó, chúng tôi gọi đây là vấn đề hồi quy.
Mục tiêu của chúng tôi là tạo ra một mô hình có dự đoán gần đúng với các giá trị đích thực tế.
Chúng tôi biểu thị mục tiêu dự đoán cho mọi trường hợp $ \ hat {y} _i $.
Đừng quan tâm tới các ký hiệu. Chúng tôi sẽ giải thích nó kỹ hơn trong các chương tiếp theo.


<!--
Lots of practical problems are well-described regression problems.
Predicting the rating that a user will assign to a movie
can be thought of as a regression problem
and if you designed a great algorithm to accomplish this feat in 2009,
you might have won the [1-million-dollar Netflix prize](https://en.wikipedia.org/wiki/Netflix_Prize).
Predicting the length of stay for patients in the hospital
is also a regression problem.
A good rule of thumb is that any *How much?* or *How many?* problem
should suggest regression.
-->

*dịch đoạn phía trên*

Rất nhiều vấn đề thực tế có thể dùng mô hình hồi quy để mô tả.
Dự đoán xếp hạng mà người xem đánh giá một bộ phim có thể được coi là vấn đề hồi quy và nếu bạn đưa ra một thuật toán tuyệt vời để hoàn thành kỳ tích này trong năm 2009, bạn có thể giành được [giải thưởng Netflix 1 triệu đô la] (https: //en.wikipedia.org/wiki/Netflix_Prize).
Dự đoán thời gian nằm viện cho bệnh nhân trong bệnh viện cũng là một vấn đề hồi quy.
Một quy tắc trong việc sử dụng hồi quy sẽ liên quan tới câu hỏi * Bao nhiêu? * Hoặc * Bao nhiêu? * 


<!--
* "How many hours will this surgery take?": *regression*
* "How many dogs are in this photo?": *regression*.
-->

*dịch đoạn phía trên*

* "Phẫu thuật này sẽ mất bao nhiêu giờ?": * Hồi quy *
* "Có bao nhiêu con chó trong bức ảnh này?": * Hồi quy *.

<!--
However, if you can easily pose your problem as "Is this a _ ?",
then it is likely, classification, a different kind
of supervised problem that we will cover next.
Even if you have never worked with machine learning before,
you have probably worked through a regression problem informally.
Imagine, for example, that you had your drains repaired
and that your contractor spent $x_1=3$ hours
removing gunk from your sewage pipes.
Then she sent you a bill of $y_1 = \$350$.
Now imagine that your friend hired the same contractor for $x_2 = 2$ hours
and that she received a bill of $y_2 = \$250$.
If someone then asked you how much to expect
on their upcoming gunk-removal invoice
you might make some reasonable assumptions,
such as more hours worked costs more dollars.
You might also assume that there is some base charge
and that the contractor then charges per hour.
If these assumptions held true, then given these two data points,
you could already identify the contractor's pricing structure:
\$100 per hour plus \$50 to show up at your house.
If you followed that much then you already understand
the high-level idea behind linear regression
(and you just implicitly designed a linear model with a bias term).
-->

*dịch đoạn phía trên*

Tuy nhiên, nếu bạn có thể dễ dàng đặt ra vấn đề của mình là "Đây có phải là một lớp không?", thì nó có khả năng, là phân loại, một dạng khác của việc giám sát mà chúng tôi sẽ đề cập sau.
Ngay cả khi bạn chưa bao giờ làm việc với học máy, thì có lẽ bạn cũng đã làm việc với những vấn đề hồi quy một cách không chính thức.
Ví dụ, hãy tưởng tượng rằng bạn đã sửa chữa cống của mình và nhà thầu của bạn đã chi $ x_1 = 3 $ giờ để loại bỏ rác khỏi đường ống nước thải của bạn.
Sau đó, cô ấy đã gửi cho bạn một hóa đơn $ y_1 = \ $ 350 $. Bây giờ hãy tưởng tượng rằng bạn của bạn đã thuê cùng một nhà thầu với giá $ x_2 = 2 $ giờ và cô ấy đã nhận được hóa đơn $ y_2 = \ $ 250 $.
Nếu sau đó ai đó hỏi bạn cần bao nhiêu tiền cho hóa đơn loại bỏ rác ở nhà của họ trong thời gian tới, bạn có thể đưa ra một số giả định hợp lý, chẳng hạn như nhiều giờ làm việc tốn nhiều đô la hơn.
Bạn cũng có thể giả định rằng có một số khoản phí cơ bản và sau đó nhà thầu tính phí mỗi giờ. Nếu các giả định này là đúng, thì với hai điểm dữ liệu này, bạn đã có thể xác định cấu trúc giá của nhà thầu:
\ $ 100 mỗi giờ cộng với $ 50 để xuất hiện tại nhà của bạn. Nếu bạn đã làm như vậy thì bạn đã hiểu ý tưởng cấp cao đằng sau hồi quy tuyến tính (và bạn chỉ ngầm thiết kế một mô hình tuyến tính có sai lệch).


<!-- =================== Kết thúc dịch Phần 13 ==================== -->

<!-- =================== Bắt đầu dịch Phần 14 ==================== -->

<!--
In this case, we could produce the parameters
that exactly matched the contractor's prices.
Sometimes that is not possible, e.g., if some of
the variance owes to some factors besides your two features.
In these cases, we will try to learn models
that minimize the distance between our predictions and the observed values.
In most of our chapters, we will focus on one of two very common losses,
the [L1 loss](http://mxnet.incubator.apache.org/api/python/gluon/loss.html#mxnet.gluon.loss.L1Loss)
where
-->

*dịch đoạn phía trên*

Trong trường hợp này, chúng tôi có thể tạo ra các tham số, phù hợp với giá của nhà thầu.
Đôi khi điều đó là không thể, ví dụ, nếu một số phương sai còn nợ một số yếu tố bên cạnh hai đặc tính của bạn.
Trong những trường hợp này, chúng tôi sẽ cố gắng đưa ra các mô hình giảm thiểu khoảng cách giữa giá dự đoán của chúng tôi và các giá trị quan sát được.
Trong hầu hết các chương của chúng tôi, chúng tôi sẽ tập trung vào một trong hai mất mát rất phổ biến, [mất L1] (http://mxnet.incubator.apache.org/api/python/gluon/loss.html#mxnet.gluon.loss .L1Loss) ở đó


$$l(y, y') = \sum_i |y_i-y_i'|$$

<!--
and the least mean squares loss, or
[L2 loss](http://mxnet.incubator.apache.org/api/python/gluon/loss.html#mxnet.gluon.loss.L2Loss),
where
-->

*dịch đoạn phía trên*

Hàm tổn thất bình phương trung bình nhỏ nhất hoặc [L2 loss] (http://mxnet.incubator.apache.org/api/python/gluon/loss.html#mxnet.gluon.loss.L2Loss),
ở đó


$$l(y, y') = \sum_i (y_i - y_i')^2.$$

<!--
As we will see later, the $L_2$ loss corresponds to the assumption
that our data was corrupted by Gaussian noise,
whereas the $L_1$ loss corresponds to an assumption
of noise from a Laplace distribution.
-->

*dịch đoạn phía trên*

Như chúng ta sẽ thấy sau đó, hàm tổn thất $ L_2 $ tương ứng với giả định rằng dữ liệu của chúng ta bị ảnh hưởng bởi nhiễu Gaussian, trong khi hàm tổn thất $ L_1 $ tương ứng với giả định bị nhiễu từ phân phối Laplace.


<!-- =================== Kết thúc dịch Phần 14 ==================== -->

<!-- =================== Bắt đầu dịch Phần 15 ==================== -->

<!--
#### Classification
-->

#### *dịch tiêu đề phía trên*

#### Phân loại


<!--
While regression models are great for addressing *how many?* questions,
lots of problems do not bend comfortably to this template.
For example, a bank wants to add check scanning to their mobile app.
This would involve the customer snapping a photo of a check
with their smart phone's camera
and the machine learning model would need to be able
to automatically understand text seen in the image.
It would also need to understand hand-written text to be even more robust.
This kind of system is referred to as optical character recognition (OCR),
and the kind of problem it addresses is called *classification*.
It is treated with a different set of algorithms
than those used for regression (although many techniques will carry over).
-->

*dịch đoạn phía trên*

Mặc dù mô hình hồi quy rất tốt để giải quyết câu hỏi * có bao nhiêu? *, nhưng có rất nhiều vấn đề không phù hợp với mẫu này.
Ví dụ: một ngân hàng muốn thêm ứng dụng quét séc trên di động. Điều này sẽ liên quan đến việc khách hàng phải chụp ảnh tấm séc bằng camera thông minh của họ và mô hình học máy sẽ cần tự động hiểu hình ảnh có trong ảnh.
Thậm chí, nó cũng cần phải hiểu rõ văn bản viết tay. Loại hệ thống này được gọi là nhận dạng ký tự quang học (OCR) và loại vấn đề mà nó giải quyết được gọi là * phân loại *. Nó được xử lý bằng một bộ thuật toán khác với các thuật toán được sử dụng cho hồi quy (mặc dù nhiều kỹ thuật sẽ khắc phục).


<!--
In classification, we want our model to look at a feature vector,
e.g., the pixel values in an image,
and then predict which category (formally called *classes*),
among some (discrete) set of options, an example belongs.
For hand-written digits, we might have 10 classes,
corresponding to the digits 0 through 9.
The simplest form of classification is when there are only two classes,
a problem which we call binary classification.
For example, our dataset $X$ could consist of images of animals
and our *labels* $Y$ might be the classes $\mathrm{\{cat, dog\}}$.
While in regression, we sought a *regressor* to output a real value $\hat{y}$,
in classification, we seek a *classifier*, whose output $\hat{y}$ is the predicted class assignment.
-->

*dịch đoạn phía trên*

Trong phân loại, chúng tôi muốn mô hình của chúng tôi xem xét một vectơ đặc trưng, ví dụ: các giá trị pixel trong một ảnh, sau đó dự đoán loại nào (thường được gọi là * lớp - class *), trong vài bộ tùy chọn (có giá trị rời rạc), một ví dụ thuộc về.
Đối với các chữ số viết tay, chúng ta có thể có 10 lớp, tương ứng với các chữ số 0 đến 9.

Hình thức phân loại đơn giản nhất là khi chỉ có hai lớp, một vấn đề mà chúng ta gọi là phân loại nhị phân.
Ví dụ: tập dữ liệu của chúng tôi $ X $ có thể bao gồm hình ảnh của động vật và * nhãn * $ Y $ của chúng tôi có thể là các lớp $ \ mathrm {\ {cat, dog \}} $.
Trong khi hồi quy, chúng tôi đã tìm kiếm một * hồi quy * để tạo ra giá trị thực $ \ hat {y} $, trong phân loại, chúng tôi tìm kiếm một * trình phân loại *, với đầu ra $ \ hat {y} $ là gán lớp được dự đoán.


<!--
For reasons that we will get into as the book gets more technical,
it can be hard to optimize a model that can only output
a hard categorical assignment, e.g., either *cat* or *dog*.
In these cases, it is usually much easier to instead express
our model in the language of probabilities.
Given an example $x$, our model assigns a probability $\hat{y}_k$
to each label $k$. Because these are probabilities,
they need to be positive numbers and add up to $1$
and thus we only need $K-1$ numbers
to assign probabilities of $K$ categories.
This is easy to see for binary classification.
If there is a $0.6$ ($60\%$) probability that an unfair coin comes up heads,
then there is a $0.4$ ($40\%$) probability that it comes up tails.
Returning to our animal classification example,
a classifier might see an image and output the probability
that the image is a cat $P(y=\text{cat} \mid x) = 0.9$.
We can interpret this number by saying that the classifier
is $90\%$ sure that the image depicts a cat.
The magnitude of the probability for the predicted class
conveys one notion of uncertainty.
It is not the only notion of uncertainty
and we will discuss others in more advanced chapters.
-->

*dịch đoạn phía trên*

Vì những lý do đó mà chúng tôi sẽ bổ sung nhiều phần kỹ thuật hơn trong cuốn sách, thật khó để tối ưu hóa một mô hình chỉ có thể tạo ra một nhãn loại phức tạp, ví dụ: * cat * hoặc * dog *.
Trong những trường hợp này, việc sử dụng mô hình bằng ngôn ngữ của xác suất sẽ dễ dàng hơn nhiều.
Cho một ví dụ $ x $, mô hình của chúng tôi gán xác suất $ \ hat {y} _k $ cho mỗi nhãn $ k $. Vì đây là các xác suất, nên chúng là các số dương và tổng xác suất là $ 1 $ và do đó chúng tôi chỉ cần số $ K-1 $ để gán xác suất của danh mục $ K $.
Điều này là dễ dàng để thực hiện phân loại nhị phân.
Nếu có xác suất $ 0,6 $ ($ 60 \% $) mà một đồng xu không xuất hiện, thì xác suất xuất hiện của nó là $ 0,4 $ ($ 40 \% $).
Quay trở lại ví dụ phân loại động vật của chúng tôi, một bộ phân loại có thể thấy một ảnh và đưa ra xác suất rằng hình ảnh đó là một con mèo $ P (y = \ text {cat} \ mid x) = 0.9 $.
Chúng ta có thể diễn giải con số này bằng cách nói rằng bộ phân loại là $ 90 \% $ chắc chắn rằng hình ảnh đó mô tả một con mèo.
Độ lớn của xác suất cho lớp dự đoán đưa ra một khái niệm về sự không chắc chắn. Đó không phải là khái niệm duy nhất về sự không chắc chắn và chúng tôi sẽ thảo luận những khái niệm khác trong các chương sau.


<!--
When we have more than two possible classes,
we call the problem *multiclass classification*.
Common examples include hand-written character recognition
`[0, 1, 2, 3 ... 9, a, b, c, ...]`.
While we attacked regression problems by trying
to minimize the L1 or L2 loss functions,
the common loss function for classification problems is called cross-entropy.
In MXNet Gluon, the corresponding loss function can be found [here](https://mxnet.incubator.apache.org/api/python/gluon/loss.html#mxnet.gluon.loss.SoftmaxCrossEntropyLoss).
-->

*dịch đoạn phía trên*

Khi chúng tôi có nhiều hơn hai lớp, chúng tôi gọi nó là * phân loại đa lớp *.
Các ví dụ phổ biến bao gồm nhận dạng ký tự viết tay `[0, 1, 2, 3 ... 9, a, b, c, ...]`.
Mặc dù chúng tôi đã thực hiện các vấn đề hồi quy bằng cách cố gắng giảm thiểu các hàm mất L1 hoặc L2, hàm mất chung cho các vấn đề phân loại được gọi là  entropy chéo (cross-entropy).
Trong MXNet Glamon, hàm tổn thất tương ứng có thể được tìm thấy [tại đây] (https://mxnet.incubator.apache.org/api/python/gluon/loss.html#mxnet.gluon.loss.SoftmaxCrossEntropyLoss).


<!-- =================== Kết thúc dịch Phần 15 ==================== -->

<!-- =================== Bắt đầu dịch Phần 16 ==================== -->

<!--
Note that the most likely class is not necessarily
the one that you are going to use for your decision.
Assume that you find this beautiful mushroom in your backyard
as shown in :numref:`fig_death_cap`.
-->

*dịch đoạn phía trên*

Lưu ý rằng lớp có khả năng nhất không nhất thiết là lớp bạn sẽ sử dụng cho quyết định của mình. Giả sử rằng bạn tìm thấy cây nấm xinh đẹp này trong sân sau của bạn như trong: numref: `fig_death_cap`.


<!--
![Death cap---do not eat!](../img/death_cap.jpg)
-->

![*dịch chú thích ảnh phía trên*](../img/death_cap.jpg)
:width:`200px`
:label:`fig_death_cap`


! [Mũ tử thần --- không ăn!] (../ img / death_cap.jpg)


<!--
Now, assume that you built a classifier and trained it
to predict if a mushroom is poisonous based on a photograph.
Say our poison-detection classifier outputs
$P(y=\mathrm{death cap}|\mathrm{image}) = 0.2$.
In other words, the classifier is $80\%$ sure
that our mushroom *is not* a death cap.
Still, you'd have to be a fool to eat it.
That is because the certain benefit of a delicious dinner
is not worth a $20\%$ risk of dying from it.
In other words, the effect of the *uncertain risk*
outweighs the benefit by far. We can look at this more formally.
Basically, we need to compute the expected risk that we incur,
i.e., we need to multiply the probability of the outcome
with the benefit (or harm) associated with it:
-->

*dịch đoạn phía trên*

Bây giờ, giả sử rằng bạn đã xây dựng một bộ phân loại và huấn luyện nó để dự đoán xem trong ảnh là một cây nấm có độc hay không.
Giả sử trình phân loại phát hiện chất độc của chúng tôi đưa ra $ P (y = \ mathrm {death cap} | \ mathrm {image}) = 0,2 $.
Nói cách khác, bộ phân loại là $ 80 \% $ chắc chắn rằng nấm của chúng ta * không phải là * mũ tử thần (nấm độc). Tuy nhiên, bạn là một kẻ ngốc khi ăn nó.
Đó là bởi vì lợi ích cho một bữa tối ngon miệng không đáng có rủi ro $ 20 \% $ để chết vì nó.
Nói cách khác, ảnh hưởng của * rủi ro không chắc chắn * vượt xa lợi ích nó mang lại. Chúng ta có thể xem điều này rõ rang hơn.
Về cơ bản, chúng ta cần tính toán rủi ro dự kiến mà chúng ta phải chịu, tức là, chúng ta cần nhân xác suất của kết quả với lợi ích (hoặc tác hại) liên quan đến nó:


$$L(\mathrm{action}| x) = E_{y \sim p(y| x)}[\mathrm{loss}(\mathrm{action},y)].$$

<!--
Hence, the loss $L$ incurred by eating the mushroom
is $L(a=\mathrm{eat}| x) = 0.2 * \infty + 0.8 * 0 = \infty$,
whereas the cost of discarding it is
$L(a=\mathrm{discard}| x) = 0.2 * 0 + 0.8 * 1 = 0.8$.
-->

Do đó, tổn thất $ L $ khi ăn nấm là $ L (a = \ mathrm {eat} | x) = 0.2 * \ infty + 0.8 * 0 = \ infty $, trong khi đó chi phí loại bỏ nó là $ L (a = \ mathrm {loại bỏ} | x) = 0,2 * 0 + 0,8 * 1 = 0,8 $.


<!--
Our caution was justified: as any mycologist would tell us,
the above mushroom actually *is* a death cap.
Classification can get much more complicated than just
binary, multiclass, or even multi-label classification.
For instance, there are some variants of classification
for addressing hierarchies.
Hierarchies assume that there exist some relationships among the many classes.
So not all errors are equal---if we must err, we would prefer
to misclassify to a related class rather than to a distant class.
Usually, this is referred to as *hierarchical classification*.
One early example is due to [Linnaeus](https://en.wikipedia.org/wiki/Carl_Linnaeus), who organized the animals in a hierarchy.
-->

*dịch đoạn phía trên*

Sự thận trọng của chúng tôi là có lý: bất kỳ nhà nấm học nào cũng cho rằng, nấm trên thực tế * là * một cái mũ tử thần.
Phân loại có thể trở nên phức tạp hơn nhiều so với phân loại nhị phân, đa lớp hoặc thậm chí đa nhãn.
Ví dụ, có một số biến thể của phân loại để giải quyết các phân cấp. Các hệ thống phân cấp cho rằng tồn tại một số mối quan hệ giữa nhiều lớp.
Vì vậy, không phải tất cả các lỗi đều như nhau --- nếu chúng ta mắc lỗi, chúng ta thích phân loại nhầm vào một lớp có liên quan hơn là một lớp ở xa.
Thông thường, điều này được gọi là * phân loại phân cấp *. Một ví dụ ban đầu là do [Linnaeus] (https://en.wikipedia.org/wiki/Carl_Linnaeus), người đã tổ chức các động vật theo một hệ thống phân cấp.


<!--
In the case of animal classification,
it might not be so bad to mistake a poodle for a schnauzer,
but our model would pay a huge penalty
if it confused a poodle for a dinosaur.
Which hierarchy is relevant might depend
on how you plan to use the model.
For example, rattle snakes and garter snakes
might be close on the phylogenetic tree,
but mistaking a rattler for a garter could be deadly.
-->

*dịch đoạn phía trên*

Trong trường hợp phân loại động vật, có thể không quá tệ khi nhầm một con chó xù với một con chó schnauzer, nhưng mô hình của chúng tôi sẽ phải chịu một hình phạt rất lớn nếu nó nhầm lẫn một con chó xù với một con khủng long. Hệ thống phân cấp nào liên quan có thể phụ thuộc vào cách bạn dự định sử dụng mô hình như thế nào.
Ví dụ, rắn rakes và rắn garter có thể ở gần trên cây phát sinh gen (phylogenetic tree), nhưng nhầm lẫn một rattler với một garter có thể gây chết người.


<!-- =================== Kết thúc dịch Phần 16 ==================== -->

<!-- =================== Bắt đầu dịch Phần 17 ==================== -->

<!--
#### Tagging
-->

#### *dịch tiêu đề phía trên*

### Gắn thẻ
<!--
Some classification problems do not fit neatly
into the binary or multiclass classification setups.
For example, we could train a normal binary classifier
to distinguish cats from dogs.
Given the current state of computer vision,
we can do this easily, with off-the-shelf tools.
Nonetheless, no matter how accurate our model gets,
we might find ourselves in trouble when the classifier
encounters an image of the Town Musicians of Bremen.
-->

*dịch đoạn phía trên*

Một số vấn đề phân loại không phù hợp với các thiết lập phân loại nhị phân hoặc phân loại đa lớp. Ví dụ, chúng ta có thể huấn luyện một bộ phân loại nhị phân bình thường để phân biệt mèo với chó.
Với hiện trạng của xử lý ảnh, chúng ta có thể thực hiện điều này một cách dễ dàng, với các công cụ sẵn có. Tuy nhiên, cho dù mô hình của chúng tôi có chính xác đến đâu, chúng tôi có thể gặp rắc rối khi bộ phân loại phải xử lý hình ảnh của Nhạc sĩ Town đến từ thành phố Bremen.


<!--
![A cat, a roster, a dog and a donkey](../img/stackedanimals.jpg)
-->

![*dịch chú thích ảnh phía trên*](../img/stackedanimals.jpg)
:width:`300px`
-->

*dịch đoạn phía trên*

! [Một con mèo, một danh sách, một con chó và một con lừa] (../ img / stackedanimals.jpg)


<!--
As you can see, there is a cat in the picture,
and a rooster, a dog, a donkey and a bird,
with some trees in the background.
Depending on what we want to do with our model
ultimately, treating this as a binary classification problem
might not make a lot of sense.
Instead, we might want to give the model the option of
saying the image depicts a cat *and* a dog *and* a donkey
*and* a rooster *and* a bird.
-->

*dịch đoạn phía trên*

Như bạn có thể thấy, có một con mèo, và một con gà trống, một con chó, một con lừa và một con chim, với một số cây trên nền của bức tranh.
Tùy thuộc vào những gì chúng tôi muốn làm với mô hình của chúng tôi, nếu coi đây là một vấn đề phân loại nhị phân có thể không có nhiều ý nghĩa.
Thay vào đó, chúng tôi có thể muốn đưa ra tùy chọn cho mô hình để đưa ra loại: một con mèo * và *một con chó * và * một con lừa * và * một con gà trống * và * một con chim.


<!--
The problem of learning to predict classes that are
*not mutually exclusive* is called multi-label classification.
Auto-tagging problems are typically best described
as multi-label classification problems.
Think of the tags people might apply to posts on a tech blog,
e.g., "machine learning", "technology", "gadgets",
"programming languages", "linux", "cloud computing", "AWS".
A typical article might have 5-10 tags applied
because these concepts are correlated.
Posts about "cloud computing" are likely to mention "AWS"
and posts about "machine learning" could also deal
with "programming languages".
-->

*dịch đoạn phía trên*

Vấn đề học cách dự đoán các lớp * không loại trừ lẫn nhau * được gọi là phân loại đa nhãn. Việc tự động gắn thẻ thường được mô tả tốt nhất là vấn đề phân loại đa nhãn.
Hãy nghĩ về các thẻ mọi người có thể áp dụng cho các bài đăng trên blog công nghệ, ví dụ: " học máy", "công nghệ", "tiện ích", "ngôn ngữ lập trình", "linux", "điện toán đám mây", "AWS".
Một bài viết điển hình có thể có 5-10 thẻ được áp dụng vì các khái niệm này có tương quan.
Các bài đăng về "điện toán đám mây" có thể đề cập đến "AWS" và các bài đăng về "học máy" cũng có thể liên quan đến "ngôn ngữ lập trình".


<!--
We also have to deal with this kind of problem when dealing
with the biomedical literature, where correctly tagging articles is important
because it allows researchers to do exhaustive reviews of the literature.
At the National Library of Medicine, a number of professional annotators
go over each article that gets indexed in PubMed
to associate it with the relevant terms from MeSH,
a collection of roughly 28k tags.
This is a time-consuming process and the
annotators typically have a one year lag between archiving and tagging.
Machine learning can be used here to provide provisional tags
until each article can have a proper manual review.
Indeed, for several years, the BioASQ organization
has [hosted a competition](http://bioasq.org/) to do precisely this.
-->

*dịch đoạn phía trên*

Chúng ta cũng phải đối phó với loại vấn đề này khi xử lý tài liệu y sinh, trong đó việc gắn thẻ chính xác rất quan trọng vì nó cho phép các nhà nghiên cứu thực hiện các đánh giá toàn diện về tài liệu.
Tại Thư viện Y khoa Quốc gia, một số nhà chú thích chuyên nghiệp duyệt qua từng bài viết được lập chỉ mục trong PubMed để liên kết nó với các thuật ngữ có liên quan từ MeSH, một bộ sưu tập khoảng 28k thẻ.
Đây là một quá trình tốn thời gian và các trình chú thích thường có độ trễ một năm giữa lưu trữ và gắn thẻ. Học máy có thể được sử dụng ở đây để cung cấp các thẻ tạm thời cho đến khi mỗi bài viết có thể có một đánh giá thủ công thích hợp.
Thật vậy, trong vài năm, tổ chức BioASQ đã [tổ chức một cuộc thi] (http://bioasq.org/) để thực hiện chính xác điều này.


<!-- =================== Kết thúc dịch Phần 17 ==================== -->

<!-- =================== Bắt đầu dịch Phần 18 ==================== -->

<!--
#### Search and ranking
-->

#### *dịch tiêu đề phía trên*

#### Tìm kiếm và xếp hạng


<!--
Sometimes we do not just want to assign each example to a bucket
or to a real value. In the field of information retrieval,
we want to impose a ranking on a set of items.
Take web search for example, the goal is less to determine whether
a particular page is relevant for a query, but rather,
which one of the plethora of search results is *most relevant*
for a particular user.
We really care about the ordering of the relevant search results
and our learning algorithm needs to produce ordered subsets
of elements from a larger set.
In other words, if we are asked to produce the first 5 letters from the alphabet, there is a difference
between returning ``A B C D E`` and ``C A B E D``.
Even if the result set is the same,
the ordering within the set matters.
-->

*dịch đoạn phía trên*

Đôi khi chúng ta không chỉ muốn gán từng ví dụ cho một nhóm hoặc cho một giá trị thực. Trong lĩnh vực truy xuất thông tin, chúng tôi muốn áp đặt thứ hạng cho một tập hợp các mục.
Lấy ví dụ về tìm kiếm trên web, mục tiêu sẽ ít hơn để xác định xem một trang cụ thể có phù hợp với truy vấn hay không, nhưng thay vào đó, một trong số rất nhiều kết quả tìm kiếm là * phù hợp nhất * cho một người dùng cụ thể.
Chúng tôi thực sự quan tâm đến việc sắp xếp các kết quả tìm kiếm có liên quan và thuật toán học tập của chúng tôi cần tạo ra các tập hợp con của các phần tử từ một tập hợp lớn hơn.
Nói cách khác, nếu chúng ta được yêu cầu tạo ra 5 chữ cái đầu tiên từ bảng chữ cái, có một sự khác biệt giữa việc trả về `` A B C D E`` và `` C A B E D``.
Ngay cả khi tập kết quả là như nhau, nhưng thứ tự trong tập lại rất quan trọng.


<!--
One possible solution to this problem is to first assign
to every element in the set a corresponding relevance score
and then to retrieve the top-rated elements.
[PageRank](https://en.wikipedia.org/wiki/PageRank),
the original secret sauce behind the Google search engine
was an early example of such a scoring system but it was
peculiar in that it did not depend on the actual query.
Here they relied on a simple relevance filter
to identify the set of relevant items
and then on PageRank to order those results
that contained the query term.
Nowadays, search engines use machine learning and behavioral models
to obtain query-dependent relevance scores.
There are entire academic conferences devoted to this subject.
-->

*dịch đoạn phía trên*

Một giải pháp khả thi cho vấn đề này là trước tiên gán cho mọi phần tử trong tập hợp điểm tương ứng tương ứng và sau đó truy xuất các phần tử được xếp hạng cao nhất.
[PageRank] (https://en.wikipedia.org/wiki/PageRank), nước sốt bí mật ban đầu đằng sau công cụ tìm kiếm Google là một ví dụ ban đầu của một hệ thống tính điểm như vậy nhưng nó đặc biệt ở chỗ nó không phụ thuộc vào thực tế truy vấn.
Ở đây, họ đã dựa vào một bộ lọc liên quan đơn giản để xác định tập hợp các mục có liên quan và sau đó trên PageRank để đặt hàng các kết quả có chứa thuật ngữ truy vấn.
Ngày nay, các công cụ tìm kiếm sử dụng các mô hình hành vi và học máy để đạt được điểm phù hợp phụ thuộc truy vấn. Có toàn bộ hội nghị học thuật dành cho chủ đề này.


<!-- =================== Kết thúc dịch Phần 18 ==================== -->

<!-- =================== Bắt đầu dịch Phần 19 ==================== -->

<!--
#### Recommender systems
-->

#### *dịch tiêu đề phía trên*
:label:`subsec_recommender_systems`

#### Hệ thống giới thiệu


<!--
Recommender systems are another problem setting
that is related to search and ranking.
The problems are similar insofar as the goal
is to display a set of relevant items to the user.
The main difference is the emphasis on *personalization*
to specific users in the context of recommender systems.
For instance, for movie recommendations,
the results page for a SciFi fan and the results page
for a connoisseur of Peter Sellers comedies might differ significantly.
Similar problems pop up in other recommendation settings,
e.g., for retail products, music, or news recommendation.
-->

*dịch đoạn phía trên*

Hệ thống đề xuất là một thiết lập vấn đề khác có liên quan đến tìm kiếm và xếp hạng.
Các vấn đề tương tự trong chừng mực vì mục tiêu là hiển thị một tập hợp các mục có liên quan cho người dùng.
Sự khác biệt chính là sự nhấn mạnh vào * cá nhân hóa * cho người dùng cụ thể trong bối cảnh các hệ thống đề xuất.
Chẳng hạn, đối với các đề xuất phim, trang kết quả cho người hâm mộ SciFi và trang kết quả cho người sành phim hài Peter Sellers có thể khác nhau đáng kể.
Các vấn đề tương tự xuất hiện trong các cài đặt đề xuất khác, ví dụ: đối với các sản phẩm bán lẻ, âm nhạc hoặc đề xuất tin tức.


<!--
In some cases, customers provide explicit feedback communicating
how much they liked a particular product
(e.g., the product ratings and reviews on Amazon, IMDB, GoodReads, etc.).
In some other cases, they provide implicit feedback,
e.g., by skipping titles on a playlist,
which might indicate dissatisfaction but might just indicate
that the song was inappropriate in context.
In the simplest formulations, these systems are trained
to estimate some score $y_{ij}$, such as an estimated rating
or the probability of purchase, given a user $u_i$ and product $p_j$.
-->

*dịch đoạn phía trên*

Trong một số trường hợp, khách hàng cung cấp phản hồi rõ ràng truyền đạt mức độ họ thích một sản phẩm cụ thể (ví dụ: xếp hạng và đánh giá sản phẩm trên Amazon, IMDB, GoodReads, v.v.).
Trong một số trường hợp khác, họ cung cấp phản hồi ngầm, ví dụ: bằng cách bỏ qua các tiêu đề trên danh sách phát, điều này có thể cho thấy sự không hài lòng nhưng có thể chỉ ra rằng bài hát không phù hợp trong ngữ cảnh.
Trong các công thức đơn giản nhất, các hệ thống này được đào tạo để ước tính một số điểm $ y_ {ij} $, chẳng hạn như xếp hạng ước tính hoặc xác suất mua hàng, được cung cấp cho người dùng $ u_i $ và sản phẩm $ p_j $.


<!--
Given such a model, then for any given user,
we could retrieve the set of objects with the largest scores $y_{ij}$,
which are could then be recommended to the customer.
Production systems are considerably more advanced and take
detailed user activity and item characteristics into account
when computing such scores. :numref:`fig_deeplearning_amazon` is an example
of deep learning books recommended by Amazon based on personalization algorithms tuned to capture the author's preferences.
-->

*dịch đoạn phía trên*

Với một mô hình như vậy, sau đó đối với bất kỳ người dùng cụ thể nào, chúng tôi có thể truy xuất tập hợp các đối tượng có điểm số lớn nhất $ y_ {ij} $, sau đó có thể được đề xuất cho khách hàng.
Các hệ thống sản xuất tiên tiến hơn đáng kể và tính đến hoạt động chi tiết của người dùng và các đặc điểm của mặt hàng khi tính toán các điểm số đó. : numref: `fig_deeplearning_amazon` là một ví dụ về những cuốn sách học sâu được Amazon khuyến nghị dựa trên các thuật toán cá nhân hóa được điều chỉnh để nắm bắt sở thích của tác giả.


<!--
![Deep learning books recommended by Amazon.](../img/deeplearning_amazon.png)
-->

![*dịch chú thích ảnh phía trên*](../img/deeplearning_amazon.png)
:label:`fig_deeplearning_amazon`


! [Sách học sâu được đề xuất bởi Amazon.] (../ img / deeplearning_amazon.png)


<!--
Despite their tremendous economic value, recommendation systems
naively built on top of predictive models
suffer some serious conceptual flaws.
To start, we only observe *censored feedback*.
Users preferentially rate movies that they feel strongly about:
you might notice that items receive many 5 and 1 star ratings
but that there are conspicuously few 3-star ratings.
Moreover, current purchase habits are often a result
of the recommendation algorithm currently in place,
but learning algorithms do not always take this detail into account.
Thus it is possible for feedback loops to form
where a recommender system preferentially pushes an item
that is then taken to be better (due to greater purchases)
and in turn is recommended even more frequently.
Many of these problems about how to deal with censoring,
incentives, and feedback loops, are important open research questions.
-->

*dịch đoạn phía trên*

Mặc dù có giá trị kinh tế to lớn, các hệ thống khuyến nghị được xây dựng một cách ngây thơ trên các mô hình dự đoán phải chịu một số sai sót nghiêm trọng về mặt khái niệm.
Để bắt đầu, chúng tôi chỉ quan sát * phản hồi bị kiểm duyệt *. Người dùng ưu tiên đánh giá những bộ phim mà họ cảm thấy thích thú:
bạn có thể nhận thấy rằng các mục nhận được nhiều xếp hạng 5 và 1 sao nhưng có rất ít xếp hạng 3 sao. Hơn nữa, thói quen mua hàng hiện tại thường là kết quả của thuật toán đề xuất hiện tại, nhưng thuật toán học tập không phải lúc nào cũng tính đến chi tiết này.
Do đó, các vòng phản hồi có thể hình thành trong đó một hệ thống đề xuất ưu tiên đẩy một mặt hàng sau đó trở nên tốt hơn (do mua nhiều hơn) và đến lượt nó được đề xuất thường xuyên hơn.
Nhiều trong số những vấn đề này về cách đối phó với kiểm duyệt, khuyến khích và các vòng phản hồi, là những câu hỏi nghiên cứu mở quan trọng.


<!-- =================== Kết thúc dịch Phần 19 ==================== -->

<!-- =================== Bắt đầu dịch Phần 20 ==================== -->

<!--
#### Sequence Learning
-->

#### *dịch tiêu đề phía trên*

#### Trình tự học


<!--
So far, we have looked at problems where we have
some fixed number of inputs and produce a fixed number of outputs.
Before we considered predicting home prices from a fixed set of features: square footage, number of bedrooms,
number of bathrooms, walking time to downtown.
We also discussed mapping from an image (of fixed dimension)
to the predicted probabilities that it belongs to each
of a fixed number of classes, or taking a user ID and a product ID,
and predicting a star rating. In these cases,
once we feed our fixed-length input
into the model to generate an output,
the model immediately forgets what it just saw.
-->

*dịch đoạn phía trên*

Cho đến nay, chúng tôi đã xem xét các vấn đề trong đó chúng tôi có một số đầu vào cố định và sản xuất một số lượng đầu ra cố định.
Trước khi chúng tôi xem xét dự đoán giá nhà từ một bộ tính năng cố định: diện tích, số phòng ngủ, số phòng tắm, thời gian đi bộ đến trung tâm thành phố.
Chúng tôi cũng đã thảo luận về ánh xạ từ một hình ảnh (có kích thước cố định) đến các xác suất dự đoán rằng nó thuộc về một số lớp cố định hoặc lấy ID người dùng và ID sản phẩm và dự đoán xếp hạng sao. Trong những trường hợp này, một khi chúng ta đưa đầu vào có độ dài cố định vào mô hình để tạo đầu ra, mô hình sẽ ngay lập tức quên đi những gì nó vừa thấy.


<!--
This might be fine if our inputs truly all have the same dimensions
and if successive inputs truly have nothing to do with each other.
But how would we deal with video snippets?
In this case, each snippet might consist of a different number of frames.
And our guess of what is going on in each frame might be much stronger
if we take into account the previous or succeeding frames.
Same goes for language. One popular deep learning problem
is machine translation: the task of ingesting sentences
in some source language and predicting their translation in another language.
-->

*dịch đoạn phía trên*

Điều này có thể ổn nếu tất cả các đầu vào của chúng ta thực sự có cùng kích thước và nếu các đầu vào kế tiếp thực sự không liên quan gì đến nhau.
Nhưng làm thế nào chúng ta sẽ đối phó với đoạn video? Trong trường hợp này, mỗi đoạn có thể bao gồm một số khung khác nhau.
Và dự đoán của chúng tôi về những gì đang diễn ra trong mỗi khung hình có thể mạnh hơn nhiều nếu chúng ta tính đến các khung trước đó hoặc thành công.
Ngôn ngữ cũng vậy. Một vấn đề học sâu phổ biến là dịch máy: nhiệm vụ nhập câu trong một số ngôn ngữ nguồn và dự đoán bản dịch của chúng bằng ngôn ngữ khác.


<!--
These problems also occur in medicine.
We might want a model to monitor patients in the intensive care unit
and to fire off alerts if their risk of death
in the next 24 hours exceeds some threshold.
We definitely would not want this model to throw away
everything it knows about the patient history each hour
and just make its predictions based on the most recent measurements.
-->

*dịch đoạn phía trên*

Những vấn đề này cũng xảy ra trong y học. Chúng tôi có thể muốn một mô hình giám sát bệnh nhân trong phòng chăm sóc đặc biệt và tắt cảnh báo nếu nguy cơ tử vong trong 24 giờ tới vượt quá ngưỡng.
Chúng tôi chắc chắn sẽ không muốn mô hình này vứt bỏ mọi thứ nó biết về lịch sử bệnh nhân mỗi giờ và chỉ đưa ra dự đoán dựa trên các phép đo gần đây nhất.


<!--
These problems are among the most exciting applications of machine learning
and they are instances of *sequence learning*.
They require a model to either ingest sequences of inputs
or to emit sequences of outputs (or both!).
These latter problems are sometimes referred to as ``seq2seq`` problems.  Language translation is a ``seq2seq`` problem.
Transcribing text from spoken speech is also a ``seq2seq`` problem.
While it is impossible to consider all types of sequence transformations,
a number of special cases are worth mentioning:
-->

*dịch đoạn phía trên*

Những vấn đề này là một trong những ứng dụng thú vị nhất của học máy và chúng là những trường hợp của * học theo trình tự *.
Họ yêu cầu một mô hình để nhập các chuỗi đầu vào hoặc để phát ra các chuỗi đầu ra (hoặc cả hai!).
Những vấn đề sau này đôi khi được gọi là các vấn đề `` seq2seq``. bản dịch ngôn ngữ là một vấn đề `` seq2seq``.
Việc sao chép văn bản từ lời nói cũng là một vấn đề `` seq2seq``. Mặc dù không thể xem xét tất cả các loại biến đổi trình tự, một số trường hợp đặc biệt đáng được đề cập:


<!-- =================== Kết thúc dịch Phần 20 ==================== -->

<!-- =================== Bắt đầu dịch Phần 21 ==================== -->

<!--
**Tagging and Parsing**. This involves annotating a text sequence with attributes.
In other words, the number of inputs and outputs is essentially the same.
For instance, we might want to know where the verbs and subjects are.
Alternatively, we might want to know which words are the named entities.
In general, the goal is to decompose and annotate text based on structural
and grammatical assumptions to get some annotation.
This sounds more complex than it actually is.
Below is a very simple example of annotating a sentence
with tags indicating which words refer to named entities.
-->

*dịch đoạn phía trên*

** Gắn thẻ và phân tích cú pháp **. Điều này liên quan đến việc chú thích một chuỗi văn bản với các thuộc tính.
Nói cách khác, số lượng đầu vào và đầu ra về cơ bản là giống nhau.
Chẳng hạn, chúng ta có thể muốn biết động từ và chủ ngữ ở đâu.
Ngoài ra, chúng tôi có thể muốn biết những từ nào là các thực thể được đặt tên.
Nói chung, mục tiêu là phân tách và chú thích văn bản dựa trên các giả định về cấu trúc và ngữ pháp để có được một số chú thích.
Điều này nghe có vẻ phức tạp hơn thực tế. Dưới đây là một ví dụ rất đơn giản về việc chú thích một câu với các thẻ chỉ ra những từ nào đề cập đến các thực thể được đặt tên.


```text
Tom has dinner in Washington with Sally.
Ent  -    -    -     Ent      -    Ent
```

Tom ăn tối ở Washington với Sally.


<!--
**Automatic Speech Recognition**. With speech recognition, the input sequence $x$
is an audio recording of a speaker (shown in :numref:`fig_speech`), and the output $y$
is the textual transcript of what the speaker said.
The challenge is that there are many more audio frames
(sound is typically sampled at 8kHz or 16kHz)
than text, i.e., there is no 1:1 correspondence between audio and text,
since thousands of samples correspond to a single spoken word.
These are ``seq2seq`` problems where the output is much shorter than the input.
-->

*dịch đoạn phía trên*

** Tự động nhận dạng giọng nói **. Với nhận dạng giọng nói, chuỗi đầu vào $ x $ là bản ghi âm của loa (hiển thị trong: numref: `fig_speech`) và đầu ra $ y $ là bản ghi văn bản của những gì người nói nói.
Thách thức là có nhiều khung âm thanh hơn (âm thanh thường được lấy mẫu ở mức 8kHz hoặc 16kHz) so với văn bản, tức là, không có sự tương ứng 1: 1 giữa âm thanh và văn bản, vì hàng ngàn mẫu tương ứng với một từ được nói.
Đây là những vấn đề `` seq2seq`` trong đó đầu ra ngắn hơn nhiều so với đầu vào.


<!--
![`-D-e-e-p- L-ea-r-ni-ng-`](../img/speech.png)
-->

![*dịch chú thích ảnh phía trên*](../img/speech.png)
:width:`700px`
:label:`fig_speech`

<!--
**Text to Speech**. Text-to-Speech (TTS) is the inverse of speech recognition.
In other words, the input $x$ is text
and the output $y$ is an audio file.
In this case, the output is *much longer* than the input.
While it is easy for *humans* to recognize a bad audio file,
this is not quite so trivial for computers.
-->

*dịch đoạn phía trên*

** Văn bản thành lời nói **. Chuyển văn bản thành giọng nói (TTS) là nghịch đảo của nhận dạng giọng nói.
Nói cách khác, đầu vào $ x $ là văn bản và đầu ra $ y $ là một tệp âm thanh.
Trong trường hợp này, đầu ra * dài hơn * nhiều so với đầu vào. Mặc dù rất dễ để * người * nhận ra một tệp âm thanh xấu, nhưng điều này không quá tầm thường đối với máy tính.


<!--
**Machine Translation**. Unlike the case of speech recognition, where corresponding
inputs and outputs occur in the same order (after alignment),
in machine translation, order inversion can be vital.
In other words, while we are still converting one sequence into another,
neither the number of inputs and outputs nor the order
of corresponding data points are assumed to be the same.
Consider the following illustrative example
of the peculiar tendency of Germans
to place the verbs at the end of sentences.
-->

*dịch đoạn phía trên*

**Dịch máy**. Không giống như trường hợp nhận dạng giọng nói, trong đó đầu vào và đầu ra tương ứng xảy ra theo cùng một thứ tự (sau khi căn chỉnh), trong dịch máy, đảo ngược thứ tự có thể rất quan trọng. Nói cách khác, trong khi chúng ta vẫn đang chuyển đổi một chuỗi thành một chuỗi khác, thì cả số lượng đầu vào và đầu ra cũng như thứ tự của các điểm dữ liệu tương ứng đều được coi là giống nhau. Hãy xem xét ví dụ minh họa sau đây về xu hướng đặc biệt của người Đức để đặt các động từ ở cuối câu.


```text
German:           Haben Sie sich schon dieses grossartige Lehrwerk angeschaut?
English:          Did you already check out this excellent tutorial?
Wrong alignment:  Did you yourself already this excellent tutorial looked-at?
```


<!--
Many related problems pop up in other learning tasks.
For instance, determining the order in which a user
reads a Webpage is a two-dimensional layout analysis problem.
Dialogue problems exhibit all kinds of additional complications,
where determining what to say next requires taking into account
real-world knowledge and the prior state of the conversation
across long temporal distances. This is an active area of research.
-->

*dịch đoạn phía trên*

Nhiều vấn đề liên quan nổi lên trong các nhiệm vụ học tập khác. Chẳng hạn, việc xác định thứ tự người dùng đọc một trang web là một vấn đề phân tích bố cục hai chiều.
Các vấn đề đối thoại thể hiện tất cả các loại phức tạp bổ sung, trong đó việc xác định những gì cần nói tiếp theo đòi hỏi phải tính đến kiến thức trong thế giới thực và trạng thái trước của cuộc trò chuyện qua các khoảng cách thời gian dài. Đây là một lĩnh vực hoạt động nghiên cứu.


<!-- =================== Kết thúc dịch Phần 21 ==================== -->

<!-- =================== Bắt đầu dịch Phần 22 ==================== -->

<!--
### Unsupervised learning
-->

### *dịch tiêu đề phía trên*

### Học không giám sát

<!--
All the examples so far were related to *Supervised Learning*,
i.e., situations where we feed the model a giant dataset
containing both the features and corresponding target values.
You could think of the supervised learner as having
an extremely specialized job and an extremely anal boss.
The boss stands over your shoulder and tells you exactly what to do
in every situation until you learn to map from situations to actions.
Working for such a boss sounds pretty lame.
On the other hand, it is easy to please this boss.
You just recognize the pattern as quickly as possible
and imitate their actions.
-->

*dịch đoạn phía trên*

Tất cả các ví dụ cho đến nay đều liên quan đến * Học có giám sát *, tức là, các tình huống chúng tôi cung cấp cho mô hình một tập dữ liệu khổng lồ chứa cả các tính năng và giá trị đích tương ứng.
Bạn có thể nghĩ về người học được giám sát là có một công việc cực kỳ chuyên môn và một ông chủ cực kỳ hậu môn.
Sếp đứng trên vai bạn và cho bạn biết chính xác phải làm gì trong mọi tình huống cho đến khi bạn học cách lập bản đồ từ các tình huống đến hành động.
Làm việc cho một ông chủ như vậy nghe có vẻ khá khập khiễng. Mặt khác, thật dễ dàng để làm hài lòng ông chủ này. Bạn chỉ cần nhận ra mô hình càng nhanh càng tốt và bắt chước hành động của họ.


<!--
In a completely opposite way, it could be frustrating
to work for a boss who has no idea what they want you to do.
However, if you plan to be a data scientist, you'd better get used to it.
The boss might just hand you a giant dump of data and tell you to *do some data science with it!* This sounds vague because it is.
We call this class of problems *unsupervised learning*,
and the type and number of questions we could ask
is limited only by our creativity.
We will address a number of unsupervised learning techniques
in later chapters. To whet your appetite for now,
we describe a few of the questions you might ask:
-->

*dịch đoạn phía trên*

Theo một cách hoàn toàn ngược lại, nó có thể gây khó chịu khi làm việc cho một ông chủ không biết họ muốn bạn làm gì.
Tuy nhiên, nếu bạn có kế hoạch trở thành một nhà khoa học dữ liệu, bạn nên làm quen với nó. Sếp có thể chỉ đưa cho bạn một đống dữ liệu khổng lồ và bảo bạn * làm một số khoa học dữ liệu với nó! * Điều này nghe có vẻ mơ hồ bởi vì nó là.
Chúng tôi gọi lớp vấn đề này là * học tập không giám sát *, và loại và số lượng câu hỏi chúng tôi có thể hỏi chỉ bị giới hạn bởi sự sáng tạo của chúng tôi.
Chúng tôi sẽ giải quyết một số kỹ thuật học tập không giám sát trong các chương sau. Để kích thích sự thèm ăn của bạn bây giờ, chúng tôi mô tả một số câu hỏi bạn có thể hỏi:


<!--
* Can we find a small number of prototypes
that accurately summarize the data?
Given a set of photos, can we group them into landscape photos,
pictures of dogs, babies, cats, mountain peaks, etc.?
Likewise, given a collection of users' browsing activity,
can we group them into users with similar behavior?
This problem is typically known as *clustering*.
* Can we find a small number of parameters
that accurately capture the relevant properties of the data?
The trajectories of a ball are quite well described
by velocity, diameter, and mass of the ball.
Tailors have developed a small number of parameters
that describe human body shape fairly accurately
for the purpose of fitting clothes.
These problems are referred to as *subspace estimation* problems.
If the dependence is linear, it is called *principal component analysis*.
* Is there a representation of (arbitrarily structured) objects
in Euclidean space (i.e., the space of vectors in $\mathbb{R}^n$)
such that symbolic properties can be well matched?
This is called *representation learning* and it is used
to describe entities and their relations,
such as Rome $-$ Italy $+$ France $=$ Paris.
* Is there a description of the root causes
of much of the data that we observe?
For instance, if we have demographic data
about house prices, pollution, crime, location,
education, salaries, etc., can we discover
how they are related simply based on empirical data?
The fields concerned with *causality* and
*probabilistic graphical models* address this problem.
* Another important and exciting recent development in unsupervised learning
is the advent of *generative adversarial networks*.
These give us a procedural way to synthesize data,
even complicated structured data like images and audio.
The underlying statistical mechanisms are tests
to check whether real and fake data are the same.
We will devote a few notebooks to them.
-->

*dịch đoạn phía trên*

* Chúng ta có thể tìm thấy một số lượng nhỏ các nguyên mẫu tóm tắt chính xác dữ liệu không?
Đưa ra một bộ ảnh, chúng ta có thể nhóm chúng thành ảnh phong cảnh, hình ảnh của chó, trẻ sơ sinh, mèo, đỉnh núi, v.v.?
Tương tự, với một bộ sưu tập các hoạt động duyệt web của người dùng, chúng ta có thể nhóm họ thành những người dùng có hành vi tương tự không?
Vấn đề này thường được gọi là * phân cụm *. * Chúng ta có thể tìm thấy một số lượng nhỏ các tham số nắm bắt chính xác các thuộc tính có liên quan của dữ liệu không?
Các quỹ đạo của một quả bóng được mô tả khá tốt bởi vận tốc, đường kính và khối lượng của quả bóng.
Thợ may đã phát triển một số lượng nhỏ các thông số mô tả hình dạng cơ thể con người khá chính xác cho mục đích phù hợp với quần áo.
Những vấn đề này được gọi là các vấn đề * ước tính không gian con *. Nếu sự phụ thuộc là tuyến tính, nó được gọi là * phân tích thành phần chính *.
* Có đại diện cho các đối tượng (có cấu trúc tùy ý) trong không gian Euclide (tức là không gian của vectơ trong $ \ mathbb {R} ^ n $) sao cho các thuộc tính tượng trưng có thể được kết hợp tốt?
Điều này được gọi là * học đại diện * và nó được sử dụng để mô tả các thực thể và mối quan hệ của chúng, chẳng hạn như Rome $ - $ Italy $ + $ France $ = $ Paris.
* Có mô tả về nguyên nhân gốc rễ của phần lớn dữ liệu mà chúng ta quan sát không?
Chẳng hạn, nếu chúng ta có dữ liệu nhân khẩu học về giá nhà, ô nhiễm, tội phạm, địa điểm, giáo dục, tiền lương, v.v., chúng ta có thể khám phá ra chúng có liên quan đơn giản dựa trên dữ liệu thực nghiệm không?
Các trường liên quan đến * mô hình nhân quả * và * xác suất * giải quyết vấn đề này.
* Một sự phát triển quan trọng và thú vị gần đây trong học tập không giám sát là sự ra đời của * mạng đối thủ thế hệ *. Chúng cho chúng ta một cách thủ tục để tổng hợp dữ liệu, thậm chí dữ liệu có cấu trúc phức tạp như hình ảnh và âm thanh.
Các cơ chế thống kê cơ bản là các thử nghiệm để kiểm tra xem dữ liệu thật và giả có giống nhau hay không. Chúng tôi sẽ dành một vài cuốn sổ cho họ.


<!-- =================== Kết thúc dịch Phần 22 ==================== -->

<!-- =================== Bắt đầu dịch Phần 23 ==================== -->

<!--
### Interacting with an Environment
-->

### *dịch tiêu đề phía trên*

### Tương tác với môi trường


<!--
So far, we have not discussed where data actually comes from,
or what actually *happens* when a machine learning model generates an output.
That is because supervised learning and unsupervised learning
do not address these issues in a very sophisticated way.
In either case, we grab a big pile of data up front,
then set our pattern recognition machines in motion
without ever interacting with the environment again.
Because all of the learning takes place
after the algorithm is disconnected from the environment,
this is sometimes called *offline learning*.
For supervised learning, the process looks like :numref:`fig_data_collection`.
-->

*dịch đoạn phía trên*

Cho đến nay, chúng ta vẫn chưa thảo luận về việc dữ liệu thực sự đến từ đâu, hoặc những gì thực sự * xảy ra * khi một mô hình học máy tạo ra một đầu ra.
Đó là bởi vì học có giám sát và học không giám sát không giải quyết những vấn đề này một cách rất tinh vi.
Trong cả hai trường hợp, chúng tôi lấy một đống dữ liệu lớn lên phía trước, sau đó đặt các máy nhận dạng mẫu của chúng tôi chuyển động mà không bao giờ tương tác với môi trường nữa.
Bởi vì tất cả việc học diễn ra sau khi thuật toán bị ngắt kết nối với môi trường, nên đôi khi nó được gọi là * học ngoại tuyến *.
Đối với việc học có giám sát, quá trình này có dạng: numref: `fig_data_collection`.


<!--
![Collect data for supervised learning from an environment.](../img/data-collection.svg)
-->

! [Thu thập dữ liệu để học có giám sát từ một môi trường.] (../ img / data-sưu tập.svg)


![*dịch chú thích ảnh phía trên*](../img/data-collection.svg)
:label:`fig_data_collection`

<!--
This simplicity of offline learning has its charms.
The upside is we can worry about pattern recognition
in isolation, without any distraction from these other problems.
But the downside is that the problem formulation is quite limiting.
If you are more ambitious, or if you grew up reading Asimov's Robot Series,
then you might imagine artificially intelligent bots capable
not only of making predictions, but of taking actions in the world.
We want to think about intelligent *agents*, not just predictive *models*.
That means we need to think about choosing *actions*,
not just making *predictions*. Moreover, unlike predictions,
actions actually impact the environment.
If we want to train an intelligent agent,
we must account for the way its actions might
impact the future observations of the agent.
-->

*dịch đoạn phía trên*

Sự đơn giản này của học ngoại tuyến có sức hấp dẫn của nó. Ưu điểm là chúng ta có thể lo lắng về việc nhận dạng mẫu trong sự cô lập, mà không có bất kỳ sự phân tâm nào từ những vấn đề khác này.
Nhưng nhược điểm là việc xây dựng vấn đề khá hạn chế. Nếu bạn tham vọng hơn, hoặc nếu bạn lớn lên đọc Sê-ri Robot của Asimov, thì bạn có thể tưởng tượng các bot thông minh nhân tạo không chỉ có khả năng đưa ra dự đoán mà còn thực hiện các hành động trên thế giới.
Chúng tôi muốn nghĩ về các tác nhân * thông minh *, không chỉ là các mô hình * dự đoán *. Điều đó có nghĩa là chúng ta cần suy nghĩ về việc chọn * hành động *, không chỉ đưa ra * dự đoán *. Hơn nữa, không giống như dự đoán, hành động thực sự tác động đến môi trường.
Nếu chúng ta muốn đào tạo một tác nhân thông minh, chúng ta phải tính đến cách hành động của nó có thể ảnh hưởng đến các quan sát trong tương lai của tác nhân.


<!--
Considering the interaction with an environment
opens a whole set of new modeling questions.
Does the environment:
-->

*dịch đoạn phía trên*

Việc xem xét sự tương tác với một môi trường sẽ mở ra một loạt các câu hỏi mô hình mới.
Môi trường:

<!--
* Remember what we did previously?
* Want to help us, e.g., a user reading text into a speech recognizer?
* Want to beat us, i.e., an adversarial setting like spam filtering (against spammers) or playing a game (vs an opponent)?
* Not care (as in many cases)?
* Have shifting dynamics (does future data always resemble the past or do the patterns change over time, either naturally or in response to our automated tools)?
-->

*dịch đoạn phía trên*

* Hãy nhớ những gì chúng ta đã làm trước đây? 
* Bạn muốn giúp chúng tôi, ví dụ: người dùng đọc văn bản vào trình nhận dạng giọng nói? 
* Bạn muốn đánh bại chúng tôi, tức là, một cài đặt đối nghịch như lọc thư rác (chống lại kẻ gửi thư rác) hoặc chơi trò chơi (so với đối thủ)? 
* Không quan tâm (như trong nhiều trường hợp)? * Có sự thay đổi động lực (dữ liệu trong tương lai luôn giống với quá khứ hoặc các mô hình thay đổi theo thời gian, một cách tự nhiên hoặc đáp ứng với các công cụ tự động của chúng tôi)?


<!--
This last question raises the problem of *distribution shift*,
(when training and test data are different).
It is a problem that most of us have experienced
when taking exams written by a lecturer,
while the homeworks were composed by her TAs.
We will briefly describe reinforcement learning and adversarial learning,
two settings that explicitly consider interaction with an environment.
-->

*dịch đoạn phía trên*

Câu hỏi cuối cùng này đặt ra vấn đề về * sự thay đổi phân phối *, (khi dữ liệu đào tạo và kiểm tra khác nhau).
Đó là một vấn đề mà hầu hết chúng ta đã trải qua khi làm bài kiểm tra được viết bởi một giảng viên, trong khi các bài tập về nhà được sáng tác bởi các TA của cô ấy.
Chúng tôi sẽ mô tả ngắn gọn về học tập củng cố và học tập đối nghịch, hai cài đặt xem xét rõ ràng sự tương tác với một môi trường.


<!-- =================== Kết thúc dịch Phần 23 ==================== -->

<!-- =================== Bắt đầu dịch Phần 24 ==================== -->

<!--
### Reinforcement learning
-->

### *dịch tiêu đề phía trên*

### Học tăng cường

<!--
If you are interested in using machine learning
to develop an agent that interacts with an environment
and takes actions, then you are probably going to wind up
focusing on *reinforcement learning* (RL).
This might include applications to robotics,
to dialogue systems, and even to developing AI for video games.
*Deep reinforcement learning* (DRL), which applies
deep neural networks to RL problems, has surged in popularity.
The breakthrough [deep Q-network that beat humans at Atari games using only the visual input](https://www.wired.com/2015/02/google-ai-plays-atari-like-pros/),
and the [AlphaGo program that dethroned the world champion at the board game Go](https://www.wired.com/2017/05/googles-alphago-trounces-humans-also-gives-boost/) are two prominent examples.
-->

*dịch đoạn phía trên*

Nếu bạn quan tâm đến việc sử dụng máy học để phát triển một tác nhân tương tác với môi trường và thực hiện các hành động, thì có lẽ bạn sẽ kết thúc
tập trung vào * học tăng cường * (RL).
Điều này có thể bao gồm các ứng dụng cho robot, cho các hệ thống đối thoại và thậm chí để phát triển AI cho các trò chơi video.
* Học tập củng cố sâu * (DRL), áp dụng mạng lưới thần kinh sâu cho các vấn đề RL, đã tăng phổ biến.
Bước đột phá [mạng Q sâu đánh bại con người tại các trò chơi Atari chỉ bằng cách sử dụng đầu vào trực quan] (https://www.wired.com/2015/02/google-ai-plays-atari-like-pros/),
và [Chương trình AlphaGo đã truất ngôi nhà vô địch thế giới tại trò chơi cờ vây] (https://www.wired.com/2017/05/googles-alphago-trounces-humans-also-gives-boost/) là hai ví dụ nổi bật .


<!--
Reinforcement learning gives a very general statement of a problem,
in which an agent interacts with an environment over a series of *timesteps*.
At each timestep $t$, the agent receives some observation $o_t$
from the environment and must choose an action $a_t$
that is subsequently transmitted back to the environment
via some mechanism (sometimes called an actuator).
Finally, the agent receives a reward $r_t$ from the environment.
The agent then receives a subsequent observation,
and chooses a subsequent action, and so on.
The behavior of an RL agent is governed by a *policy*.
In short, a *policy* is just a function that maps
from observations (of the environment) to actions.
The goal of reinforcement learning is to produce a good policy.
-->

*dịch đoạn phía trên*

Học tăng cường đưa ra một tuyên bố rất chung về một vấn đề, trong đó một tác nhân tương tác với một môi trường qua một loạt * dấu thời gian *.
Tại mỗi dấu thời gian $ t $, tác nhân nhận được một số quan sát $ o_t $ từ môi trường và phải chọn một hành động $ a_t $ sau đó được truyền trở lại môi trường thông qua một số cơ chế (đôi khi được gọi là bộ chấp hành).
Cuối cùng, đại lý nhận được phần thưởng $ r_t $ từ môi trường. Tác nhân sau đó nhận được một quan sát tiếp theo và chọn một hành động tiếp theo, v.v.
Hành vi của một đại lý RL được điều chỉnh bởi một * chính sách *. Nói tóm lại, một * chính sách * chỉ là một chức năng ánh xạ từ các quan sát (của môi trường) đến các hành động.
Mục tiêu của học tập củng cố là tạo ra một chính sách tốt.


<!--
![The interaction between reinforcement learning and an environment.](../img/rl-environment.svg)
-->

![*dịch chú thích ảnh phía trên*](../img/rl-environment.svg)


! [Sự tương tác giữa học tập củng cố và môi trường.] (../ img / rl-môi trường.svg)


<!--
It is hard to overstate the generality of the RL framework.
For example, we can cast any supervised learning problem as an RL problem.
Say we had a classification problem.
We could create an RL agent with one *action* corresponding to each class.
We could then create an environment which gave a reward
that was exactly equal to the loss function
from the original supervised problem.
-->

*dịch đoạn phía trên*

Thật khó để nói quá về tính tổng quát của khung RL.
Ví dụ: chúng ta có thể đặt bất kỳ vấn đề học tập có giám sát nào thành vấn đề RL.
Nói rằng chúng tôi đã có một vấn đề phân loại.
Chúng ta có thể tạo một tác nhân RL với một * hành động * tương ứng với mỗi lớp.
Sau đó chúng ta có thể tạo ra một môi trường đưa ra phần thưởng hoàn toàn bằng với hàm tổn thất từ vấn đề được giám sát ban đầu.


<!-- =================== Kết thúc dịch Phần 24 ==================== -->

<!-- =================== Bắt đầu dịch Phần 25 ==================== -->

<!--
That being said, RL can also address many problems
that supervised learning cannot.
For example, in supervised learning we always expect
that the training input comes associated with the correct label.
But in RL, we do not assume that for each observation,
the environment tells us the optimal action.
In general, we just get some reward.
Moreover, the environment may not even tell us which actions led to the reward.
-->

*dịch đoạn phía trên*

Điều đó đang được nói, RL cũng có thể giải quyết nhiều vấn đề mà việc học có giám sát không thể.
Ví dụ, trong học tập có giám sát, chúng tôi luôn mong đợi rằng đầu vào đào tạo đi kèm với nhãn chính xác.
Nhưng trong RL, chúng tôi không cho rằng với mỗi quan sát, môi trường cho chúng ta biết hành động tối ưu.
Nói chung, chúng tôi chỉ nhận được một số phần thưởng. Hơn nữa, môi trường thậm chí có thể không cho chúng ta biết hành động nào dẫn đến phần thưởng.


<!--
Consider for example the game of chess.
The only real reward signal comes at the end of the game
when we either win, which we might assign a reward of 1,
or when we lose, which we could assign a reward of -1.
So reinforcement learners must deal with the *credit assignment problem*:
determining which actions to credit or blame for an outcome.
The same goes for an employee who gets a promotion on October 11.
That promotion likely reflects a large number
of well-chosen actions over the previous year.
Getting more promotions in the future requires figuring out
what actions along the way led to the promotion.
-->

*dịch đoạn phía trên*

Hãy xem xét ví dụ như trò chơi cờ vua. Tín hiệu phần thưởng thực sự duy nhất xuất hiện vào cuối trò chơi khi chúng tôi thắng, chúng tôi có thể chỉ định phần thưởng là 1 hoặc khi chúng tôi thua, chúng tôi có thể chỉ định phần thưởng là -1.
Vì vậy, người học củng cố phải đối phó với * vấn đề chuyển nhượng tín dụng *: xác định hành động nào để ghi có hoặc đổ lỗi cho kết quả.
Điều tương tự cũng xảy ra với một nhân viên được thăng chức vào ngày 11 tháng 10.
Khuyến mãi đó có khả năng phản ánh một số lượng lớn các hành động được lựa chọn tốt trong năm trước.
Nhận được nhiều khuyến mãi hơn trong tương lai đòi hỏi phải tìm ra những hành động trên đường dẫn đến chương trình khuyến mãi.


<!--
Reinforcement learners may also have to deal
with the problem of partial observability.
That is, the current observation might not
tell you everything about your current state.
Say a cleaning robot found itself trapped
in one of many identical closets in a house.
Inferring the precise location (and thus state) of the robot
might require considering its previous observations before entering the closet.
-->

*dịch đoạn phía trên*

Người học tăng cường cũng có thể phải đối phó với vấn đề quan sát một phần.
Đó là, quan sát hiện tại có thể không cho bạn biết mọi thứ về tình trạng hiện tại của bạn.
Nói rằng một robot làm sạch thấy mình bị mắc kẹt trong một trong nhiều tủ quần áo giống hệt nhau trong một ngôi nhà.
Suy ra vị trí chính xác (và do đó là trạng thái) của robot có thể yêu cầu xem xét các quan sát trước đó của nó trước khi vào tủ.


<!--
Finally, at any given point, reinforcement learners
might know of one good policy,
but there might be many other better policies
that the agent has never tried.
The reinforcement learner must constantly choose
whether to *exploit* the best currently-known strategy as a policy,
or to *explore* the space of strategies,
potentially giving up some short-run reward in exchange for knowledge.
-->

*dịch đoạn phía trên*

Cuối cùng, tại bất kỳ thời điểm nào, người học củng cố có thể biết về một chính sách tốt, nhưng có thể có nhiều chính sách khác tốt hơn mà đại lý chưa bao giờ thử.
Người học củng cố phải liên tục chọn xem * khai thác * chiến lược được biết đến nhiều nhất hiện nay như một chính sách, hay * khám phá * không gian của các chiến lược, có khả năng từ bỏ một số phần thưởng ngắn hạn để đổi lấy kiến thức.


<!-- =================== Kết thúc dịch Phần 25 ==================== -->

<!-- =================== Bắt đầu dịch Phần 26 ==================== -->

<!--
#### MDPs, bandits, and friends
-->

#### *dịch tiêu đề phía trên*

#### MDP, kẻ cướp và bạn bè


<!--
The general reinforcement learning problem
is a very general setting.
Actions affect subsequent observations.
Rewards are only observed corresponding to the chosen actions.
The environment may be either fully or partially observed.
Accounting for all this complexity at once may ask too much of researchers.
Moreover, not every practical problem exhibits all this complexity.
As a result, researchers have studied a number of
*special cases* of reinforcement learning problems.
-->

*dịch đoạn phía trên*

Các vấn đề học tập củng cố chung là một thiết lập rất chung chung.
Các hành động ảnh hưởng đến các quan sát tiếp theo. Phần thưởng chỉ được quan sát tương ứng với các hành động đã chọn.
Môi trường có thể được quan sát đầy đủ hoặc một phần.
Kế toán cho tất cả sự phức tạp này cùng một lúc có thể yêu cầu quá nhiều nhà nghiên cứu.
Hơn nữa, không phải mọi vấn đề thực tế đều thể hiện tất cả sự phức tạp này.
Do đó, các nhà nghiên cứu đã nghiên cứu một số * trường hợp đặc biệt * về các vấn đề học tập củng cố.


<!--
When the environment is fully observed,
we call the RL problem a *Markov Decision Process* (MDP).
When the state does not depend on the previous actions,
we call the problem a *contextual bandit problem*.
When there is no state, just a set of available actions
with initially unknown rewards, this problem
is the classic *multi-armed bandit problem*.
-->

*dịch đoạn phía trên*

Khi môi trường được quan sát đầy đủ, chúng tôi gọi vấn đề RL là * Quy trình quyết định Markov * (MDP).
Khi trạng thái không phụ thuộc vào các hành động trước đó, chúng tôi gọi vấn đề này là * vấn đề tên cướp theo ngữ cảnh *.
Khi không có trạng thái, chỉ cần một tập hợp các hành động có sẵn với phần thưởng ban đầu chưa biết, vấn đề này là vấn đề cổ điển * đa vũ trang *.


<!-- =================== Kết thúc dịch Phần 26 ==================== -->

<!-- =================== Bắt đầu dịch Phần 27 ==================== -->

<!--
## Roots
-->

## *dịch tiêu đề phía trên*

## Nguồn gốc

<!--
Although many deep learning methods are recent inventions,
humans have held the desire to analyze data
and to predict future outcomes for centuries.
In fact, much of natural science has its roots in this.
For instance, the Bernoulli distribution is named after
[Jacob Bernoulli (1655-1705)](https://en.wikipedia.org/wiki/Jacob_Bernoulli), and the Gaussian distribution was discovered
by [Carl Friedrich Gauss (1777-1855)](https://en.wikipedia.org/wiki/Carl_Friedrich_Gauss).
He invented for instance the least mean squares algorithm,
which is still used today for countless problems
from insurance calculations to medical diagnostics.
These tools gave rise to an experimental approach
in the natural sciences---for instance, Ohm's law
relating current and voltage in a resistor
is perfectly described by a linear model.
-->

*dịch đoạn phía trên*

Mặc dù nhiều phương pháp học sâu là những phát minh gần đây, con người đã có mong muốn phân tích dữ liệu và dự đoán kết quả trong tương lai trong nhiều thế kỷ.
Trên thực tế, phần lớn khoa học tự nhiên có nguồn gốc từ điều này. Chẳng hạn, bản phân phối Bernoulli được đặt tên theo [Jacob Bernoulli (1655-1705)] (https://en.wikipedia.org/wiki/Jacob_Bernoulli) và bản phân phối Gaussian được phát hiện bởi [Carl Friedrich Gauss (1777-1855) ] (https://en.wikipedia.org/wiki/Carl_Friedrich_Gauss).
Ví dụ, ông đã phát minh ra thuật toán bình phương nhỏ nhất, vẫn được sử dụng cho vô số vấn đề từ tính toán bảo hiểm đến chẩn đoán y khoa.
Những công cụ này đã tạo ra một cách tiếp cận thử nghiệm trong khoa học tự nhiên --- ví dụ, định luật Ohm liên quan đến dòng điện và điện áp trong một điện trở được mô tả hoàn hảo bằng mô hình tuyến tính.


<!--
Even in the middle ages, mathematicians had a keen intuition of estimates.
For instance, the geometry book of [Jacob Köbel (1460-1533)](https://www.maa.org/press/periodicals/convergence/mathematical-treasures-jacob-kobels-geometry) illustrates
averaging the length of 16 adult men's feet to obtain the average foot length.
-->

*dịch đoạn phía trên*

Ngay cả trong thời trung cổ, các nhà toán học đã có một trực giác nhạy bén của các ước tính.
Chẳng hạn, cuốn sách hình học của [Jacob Köbel (1460-1533)] (https://www.maa.org/press/apseicals/convergence/mathologists-treasures-jacob-kobels-geometry) minh họa trung bình chiều dài của 16 người trưởng thành chân nam để có được chiều dài chân trung bình.


<!--
![Estimating the length of a foot](../img/koebel.jpg)
-->

![*dịch chú thích ảnh phía trên*](../img/koebel.jpg)
:width:`500px`
:label:`fig_koebel`

! [Ước tính chiều dài của một bàn chân] (../ img / koebel.jpg)

<!--
:numref:`fig_koebel` illustrates how this estimator works.
The 16 adult men were asked to line up in a row, when leaving church.
Their aggregate length was then divided by 16
to obtain an estimate for what now amounts to 1 foot.
This "algorithm" was later improved to deal with misshapen feet---the
2 men with the shortest and longest feet respectively were sent away,
averaging only over the remainder.
This is one of the earliest examples of the trimmed mean estimate.
-->

*dịch đoạn phía trên*

: numref: `fig_koebel` minh họa cách công cụ ước tính này hoạt động. 16 người đàn ông trưởng thành được yêu cầu xếp hàng liên tiếp, khi rời nhà thờ.
Tổng chiều dài của chúng sau đó được chia cho 16 để có được ước tính cho khoảng thời gian hiện tại là 1 feet.
"Thuật toán" này sau đó đã được cải tiến để đối phó với bàn chân biến dạng --- 2 người đàn ông có bàn chân ngắn nhất và dài nhất tương ứng được gửi đi, trung bình chỉ trong phần còn lại.
Đây là một trong những ví dụ sớm nhất về ước tính trung bình cắt xén.


<!--
Statistics really took off with the collection and availability of data.
One of its titans, [Ronald Fisher (1890-1962)](https://en.wikipedia.org/wiki/Ronald_Fisher), contributed significantly to its theory
and also its applications in genetics.
Many of his algorithms (such as Linear Discriminant Analysis)
and formula (such as the Fisher Information Matrix)
are still in frequent use today (even the Iris dataset
that he released in 1936 is still used sometimes
to illustrate machine learning algorithms).
Fisher was also a proponent of eugenics,
which should remind us that the morally dubious use data science
has as long and enduring a history as its productive use
in industry and the natural sciences.
-->

*dịch đoạn phía trên*

Thống kê thực sự cất cánh với việc thu thập và sẵn có dữ liệu.
Một trong những người khổng lồ của nó, [Ronald Fisher (1890-1962)] (https://en.wikipedia.org/wiki/Ronald_Fisher), đã đóng góp đáng kể vào lý thuyết của nó và cả những ứng dụng của nó trong di truyền học.
Nhiều thuật toán của ông (như Phân tích phân biệt tuyến tính) và công thức (như Ma trận thông tin Fisher) vẫn được sử dụng thường xuyên cho đến ngày nay (ngay cả bộ dữ liệu Iris mà ông phát hành năm 1936 đôi khi vẫn được sử dụng để minh họa các thuật toán học máy).
Fisher cũng là một người ủng hộ thuyết ưu sinh, điều này sẽ nhắc nhở chúng ta rằng khoa học sử dụng dữ liệu không rõ ràng về mặt đạo đức đã tồn tại lâu dài và bền vững trong lịch sử như việc sử dụng nó trong công nghiệp và khoa học tự nhiên.


<!-- =================== Kết thúc dịch Phần 27 ==================== -->

<!-- =================== Bắt đầu dịch Phần 28 ==================== -->

<!--
A second influence for machine learning came from Information Theory
[(Claude Shannon, 1916-2001)](https://en.wikipedia.org/wiki/Claude_Shannon) and the Theory of computation via [Alan Turing (1912-1954)](https://en.wikipedia.org/wiki/Alan_Turing).
Turing posed the question "can machines think?”
in his famous paper [Computing machinery and intelligence](https://en.wikipedia.org/wiki/Computing_Machinery_and_Intelligence) (Mind, October 1950).
In what he described as the Turing test, a machine
can be considered intelligent if it is difficult
for a human evaluator to distinguish between the replies
from a machine and a human based on textual interactions.
-->

*dịch đoạn phía trên*

Ảnh hưởng thứ hai đối với học máy đến từ Lý thuyết thông tin [(Claude Shannon, 1916-2001)] (https://en.wikipedia.org/wiki/Claude_Shannon) và Lý thuyết tính toán thông qua [Alan Turing (1912-1954)] (https://en.wikipedia.org/wiki/Alan_Turing).
Turing đã đặt ra câu hỏi "máy móc có thể nghĩ gì không? Trong bài báo nổi tiếng của anh ấy [Máy ​​tính và trí thông minh] (https://en.wikipedia.org/wiki/Computing_Machowder_and_Intellect) (Mind, tháng 10 năm 1950).
Trong những gì ông mô tả là thử nghiệm Turing, một cỗ máy có thể được coi là thông minh nếu người đánh giá con người khó phân biệt giữa trả lời từ máy và con người dựa trên tương tác văn bản.


<!--
Another influence can be found in neuroscience and psychology.
After all, humans clearly exhibit intelligent behavior.
It is thus only reasonable to ask whether one could explain
and possibly reverse engineer this capacity.
One of the oldest algorithms inspired in this fashion
was formulated by [Donald Hebb (1904-1985)](https://en.wikipedia.org/wiki/Donald_O._Hebb).
In his groundbreaking book The Organization of Behavior :cite:`Hebb.Hebb.1949`,
he posited that neurons learn by positive reinforcement.
This became known as the Hebbian learning rule.
It is the prototype of Rosenblatt's perceptron learning algorithm
and it laid the foundations of many stochastic gradient descent algorithms
that underpin deep learning today: reinforce desirable behavior
and diminish undesirable behavior to obtain good settings
of the parameters in a neural network.
-->

*dịch đoạn phía trên*

Một ảnh hưởng khác có thể được tìm thấy trong khoa học thần kinh và tâm lý học.
Rốt cuộc, con người thể hiện rõ ràng hành vi thông minh. Do đó, chỉ hợp lý để hỏi liệu người ta có thể giải thích và có thể đảo ngược khả năng này không.
Một trong những thuật toán lâu đời nhất được truyền cảm hứng theo kiểu này được xây dựng bởi [Donald Hebb (1904-1985)] (https://en.wikipedia.org/wiki/Donald_O._Hebb).
Trong cuốn sách đột phá của mình Tổ chức hành vi: trích dẫn: `Hebb.Hebb.1949`, ông đã đặt ra rằng các tế bào thần kinh học bằng cách củng cố tích cực.
Điều này đã được biết đến như là quy tắc học tập của người Do Thái. Nó là nguyên mẫu của thuật toán học tri giác của Rosenblatt và nó đặt nền móng cho nhiều thuật toán giảm độ dốc ngẫu nhiên làm nền tảng cho việc học sâu ngày nay: củng cố hành vi mong muốn và giảm bớt hành vi không mong muốn để có được các cài đặt tốt của các tham số trong mạng lưới thần kinh.


<!--
Biological inspiration is what gave *neural networks* their name.
For over a century (dating back to the models of Alexander Bain, 1873
and James Sherrington, 1890), researchers have tried to assemble
computational circuits that resemble networks of interacting neurons.
Over time, the interpretation of biology has become less literal
but the name stuck. At its heart, lie a few key principles
that can be found in most networks today:
-->

*dịch đoạn phía trên*

Cảm hứng sinh học là những gì đã cho * mạng lưới thần kinh * tên của họ. Trong hơn một thế kỷ (bắt nguồn từ các mô hình của Alexander Bain, 1873 và James Sherrington, 1890), các nhà nghiên cứu đã cố gắng lắp ráp các mạch tính toán giống như các mạng lưới các nơ-ron tương tác.
Theo thời gian, việc giải thích sinh học đã trở nên ít nghĩa đen hơn nhưng tên bị kẹt. Tại trung tâm của nó, nói dối một số nguyên tắc chính có thể được tìm thấy trong hầu hết các mạng ngày nay:


<!--
* The alternation of linear and nonlinear processing units, often referred to as *layers*.
* The use of the chain rule (also known as *backpropagation*) for adjusting parameters in the entire network at once.
-->

*dịch đoạn phía trên*

* Sự xen kẽ của các đơn vị xử lý tuyến tính và phi tuyến, thường được gọi là * lớp *.
* Việc sử dụng quy tắc chuỗi (còn được gọi là * backpropagation *) để điều chỉnh các tham số trong toàn bộ mạng cùng một lúc.


<!--
After initial rapid progress, research in neural networks
languished from around 1995 until 2005.
This was due to a number of reasons.
Training a network is computationally very expensive.
While RAM was plentiful at the end of the past century,
computational power was scarce.
Second, datasets were relatively small.
In fact, Fisher's Iris dataset from 1932
was a popular tool for testing the efficacy of algorithms.
MNIST with its 60,000 handwritten digits was considered huge.
-->

*dịch đoạn phía trên*

Sau những tiến bộ nhanh chóng ban đầu, nghiên cứu về các mạng lưới thần kinh đã mất dần từ khoảng năm 1995 đến năm 2005.
Điều này là do một số lý do. Đào tạo một mạng là tính toán rất tốn kém.
Trong khi RAM rất dồi dào vào cuối thế kỷ qua, sức mạnh tính toán còn khan hiếm.
Thứ hai, bộ dữ liệu tương đối nhỏ. Trên thực tế, bộ dữ liệu Iris của Fisher từ năm 1932 là một công cụ phổ biến để kiểm tra tính hiệu quả của các thuật toán.
MNIST với 60.000 chữ số viết tay được coi là rất lớn


<!--
Given the scarcity of data and computation,
strong statistical tools such as Kernel Methods,
Decision Trees and Graphical Models proved empirically superior.
Unlike neural networks, they did not require weeks to train
and provided predictable results with strong theoretical guarantees.
-->

*dịch đoạn phía trên*


Với sự khan hiếm của dữ liệu và tính toán,
các công cụ thống kê mạnh như Phương pháp hạt nhân,
Cây quyết định và mô hình đồ họa tỏ ra vượt trội về mặt thực nghiệm.
Không giống như mạng lưới thần kinh, họ không cần nhiều tuần để đào tạo
và cung cấp kết quả dự đoán với sự đảm bảo lý thuyết mạnh mẽ.


<!-- =================== Kết thúc dịch Phần 28 ==================== -->

<!-- =================== Bắt đầu dịch Phần 29 ==================== -->

<!--
## The Road to Deep Learning
-->

## *dịch tiêu đề phía trên*

## Con đường tới Học sâu


<!--
Much of this changed with the ready availability of large amounts of data,
due to the World Wide Web, the advent of companies serving
hundreds of millions of users online, a dissemination of cheap,
high quality sensors, cheap data storage (Kryder's law),
and cheap computation (Moore's law), in particular in the form of GPUs, originally engineered for computer gaming.
Suddenly algorithms and models that seemed computationally infeasible
became relevant (and vice versa).
This is best illustrated in :numref:`tab_intro_decade`.
-->

*dịch đoạn phía trên*

Phần lớn điều này đã thay đổi với sự sẵn có của một lượng lớn dữ liệu,
do World Wide Web, sự ra đời của các công ty phục vụ
Hàng trăm triệu người dùng trực tuyến, phổ biến giá rẻ,
cảm biến chất lượng cao, lưu trữ dữ liệu giá rẻ (luật Kryder),
và tính toán giá rẻ (định luật Moore), đặc biệt ở dạng GPU, ban đầu được thiết kế để chơi game trên máy tính.
Đột nhiên các thuật toán và mô hình dường như không thể tính toán được
trở nên có liên quan (và ngược lại).
Điều này được minh họa rõ nhất trong: numref: `tab_intro_decade`.


<!--
:Dataset versus computer memory and computational power
-->

*dịch đoạn phía trên*

: Bộ dữ liệu so với bộ nhớ máy tính và sức mạnh tính toán


<!--
|Decade|Dataset|Memory|Floating Point Calculations per Second|
|:--|:-|:-|:-|
|1970|100 (Iris)|1 KB|100 KF (Intel 8080)|
|1980|1 K (House prices in Boston)|100 KB|1 MF (Intel 80186)|
|1990|10 K (optical character recognition)|10 MB|10 MF (Intel 80486)|
|2000|10 M (web pages)|100 MB|1 GF (Intel Core)|
|2010|10 G (advertising)|1 GB|1 TF (Nvidia C2050)|
|2020|1 T (social network)|100 GB|1 PF (Nvidia DGX-2)|
:label:`tab_intro_decade`

| Thập kỷ | Bộ dữ liệu | Bộ nhớ | Tính toán dấu phẩy động mỗi giây |
|: - |: - |: - |: - |
| 1970 | 100 (Iris) | 1 KB | 100 KF (Intel 8080) |
| 1980 | 1 K (Giá nhà tại Boston) | 100 KB | 1 MF (Intel 80186) |
| 1990 | 10 K (nhận dạng ký tự quang học) | 10 MB | 10 MF (Intel 80486) |
| 2000 | 10 M (trang web) | 100 MB | 1 GF (Intel Core) |
| 2010 | 10 G (quảng cáo) | 1 GB | 1 TF (Nvidia C2050) |
| 2020 | 1 T (mạng xã hội) | 100 GB | 1 PF (Nvidia DGX-2) |
: nhãn: `tab_intro_decade`


<!--
It is evident that RAM has not kept pace with the growth in data.
At the same time, the increase in computational power
has outpaced that of the data available.
This means that statistical models needed to become more memory efficient
(this is typically achieved by adding nonlinearities)
while simultaneously being able to spend more time
on optimizing these parameters, due to an increased compute budget.
Consequently the sweet spot in machine learning and statistics
moved from (generalized) linear models and kernel methods to deep networks.
This is also one of the reasons why many of the mainstays
of deep learning, such as multilayer perceptrons
:cite:`McCulloch.Pitts.1943`, convolutional neural networks
:cite:`LeCun.Bottou.Bengio.ea.1998`, Long Short-Term Memory
:cite:`Hochreiter.Schmidhuber.1997`,
and Q-Learning :cite:`Watkins.Dayan.1992`,
were essentially "rediscovered" in the past decade,
after laying comparatively dormant for considerable time.
-->

*dịch đoạn phía trên*


Rõ ràng là RAM đã không theo kịp tốc độ tăng trưởng của dữ liệu.
Đồng thời, sự gia tăng sức mạnh tính toán
đã vượt qua dữ liệu có sẵn.
Điều này có nghĩa là các mô hình thống kê cần thiết để trở nên hiệu quả hơn về bộ nhớ
(điều này thường đạt được bằng cách thêm phi tuyến)
đồng thời có thể dành nhiều thời gian hơn
về việc tối ưu hóa các tham số này, do ngân sách tính toán tăng lên.
Do đó, điểm ngọt trong học máy và thống kê
chuyển từ mô hình tuyến tính (tổng quát) và phương thức kernel sang mạng sâu.
Đây cũng là một trong những lý do tại sao nhiều trụ cột
học sâu, chẳng hạn như tri giác đa lớp
: trích dẫn: `McCulloch.Pitts.1943`, mạng lưới thần kinh tích chập
: trích dẫn: `LeCun.Bottou.Bengio.ea.1998`, Bộ nhớ ngắn hạn dài
: trích dẫn: `Hồ sơ.Schmidhuber.1997`,
và Q-Learning: trích dẫn: `Watkins.Dayan.1992`,
về cơ bản là "tái khám phá" trong thập kỷ qua,
sau khi đặt tương đối im lìm trong thời gian đáng kể.


<!--
The recent progress in statistical models, applications, and algorithms,
has sometimes been likened to the Cambrian Explosion:
a moment of rapid progress in the evolution of species.
Indeed, the state of the art is not just a mere consequence
of available resources, applied to decades old algorithms.
Note that the list below barely scratches the surface
of the ideas that have helped researchers achieve tremendous progress
over the past decade.
-->

*dịch đoạn phía trên*

Những tiến bộ gần đây trong các mô hình thống kê, ứng dụng và thuật toán,
đôi khi được ví như vụ nổ Cambrian:
một khoảnh khắc của sự tiến bộ nhanh chóng trong sự tiến hóa của các loài.
Thật vậy, tình trạng của nghệ thuật không chỉ là một hệ quả
tài nguyên có sẵn, áp dụng cho các thuật toán cũ hàng thập kỷ.
Lưu ý rằng danh sách dưới đây hầu như không làm trầy xước bề mặt
về những ý tưởng đã giúp các nhà nghiên cứu đạt được tiến bộ to lớn
trong thập kỷ qua.


<!-- =================== Kết thúc dịch Phần 29 ==================== -->

<!-- =================== Bắt đầu dịch Phần 30 ==================== -->

<!--
* Novel methods for capacity control, such as Dropout
  :cite:`Srivastava.Hinton.Krizhevsky.ea.2014`
  have helped to mitigate the danger of overfitting.
  This was achieved by applying noise injection :cite:`Bishop.1995`
  throughout the network, replacing weights by random variables
  for training purposes.
-->

*dịch đoạn phía trên*

* Phương pháp tiểu thuyết để kiểm soát năng lực, chẳng hạn như bỏ học
  : trích dẫn: `Srivastava.Hinton.Krizhevsky.ea.2014`
  đã giúp giảm thiểu nguy cơ quá mức.
  Điều này đã đạt được bằng cách áp dụng phương pháp tiêm nhiễu: trích dẫn: `Giám mục.1995`
  trên toàn mạng, thay thế trọng số bằng các biến ngẫu nhiên
  cho mục đích đào tạo.


<!--
* Attention mechanisms solved a second problem
  that had plagued statistics for over a century:
  how to increase the memory and complexity of a system without
  increasing the number of learnable parameters.
  :cite:`Bahdanau.Cho.Bengio.2014` found an elegant solution
  by using what can only be viewed as a learnable pointer structure.
  Rather than having to remember an entire sentence, e.g.,
  for machine translation in a fixed-dimensional representation,
  all that needed to be stored was a pointer to the intermediate state
  of the translation process. This allowed for significantly
  increased accuracy for long sentences, since the model
  no longer needed to remember the entire sentence before
  commencing the generation of a new sentence.
-->

*dịch đoạn phía trên*

* Cơ chế chú ý đã giải quyết vấn đề thứ hai,
  nó thống kê thảm họa trong hơn một thế kỷ:
  Làm thế nào để tăng bộ nhớ và độ phức tạp của một hệ thống mà không cần
  tăng số lượng tham số có thể học được.
  : trích dẫn: `Bahdanau.Cho.Bengio.2014` tìm thấy một giải pháp tao nhã
  bằng cách sử dụng những gì chỉ có thể được xem như một cấu trúc con trỏ có thể học được.
  Thay vì phải nhớ toàn bộ câu, ví dụ:
  cho dịch máy trong một đại diện chiều cố định,
  tất cả những gì cần được lưu trữ là một con trỏ đến trạng thái trung gian
  của quá trình dịch thuật. Điều này cho phép đáng kể
  tăng độ chính xác cho các câu dài, kể từ mô hình
  không còn cần phải nhớ toàn bộ câu trước
  bắt đầu thế hệ của một câu mới.


<!--
* Multi-stage designs, e.g., via the Memory Networks (MemNets)
  :cite:`Sukhbaatar.Weston.Fergus.ea.2015` and the Neural Programmer-Interpreter :cite:`Reed.De-Freitas.2015`
  allowed statistical modelers to describe iterative approaches to reasoning. These tools allow for an internal state of the deep network
  to be modified repeatedly, thus carrying out subsequent steps
  in a chain of reasoning, similar to how a processor
  can modify memory for a computation.
-->

*dịch đoạn phía trên*

* Thiết kế nhiều giai đoạn, ví dụ: thông qua Mạng bộ nhớ (MemNets)
  : trích dẫn: `Sukhbaatar.Weston.Fergus.ea.2015` và Lập trình viên-Phiên dịch thần kinh: trích dẫn:` Reed.De-Freitas.2015`
  cho phép các nhà lập mô hình thống kê mô tả các phương pháp lặp để lý luận. Những công cụ này cho phép một trạng thái nội bộ của mạng sâu
  được sửa đổi nhiều lần, do đó thực hiện các bước tiếp theo
  trong một chuỗi lý luận, tương tự như cách một bộ xử lý
  có thể sửa đổi bộ nhớ cho một tính toán.


<!--
* Another key development was the invention of GANS
  :cite:`Goodfellow.Pouget-Abadie.Mirza.ea.2014`.
  Traditionally, statistical methods for density estimation
  and generative models focused on finding proper probability distributions
  and (often approximate) algorithms for sampling from them.
  As a result, these algorithms were largely limited by the lack of
  flexibility inherent in the statistical models.
  The crucial innovation in GANs was to replace the sampler
  by an arbitrary algorithm with differentiable parameters.
  These are then adjusted in such a way that the discriminator
  (effectively a two-sample test) cannot distinguish fake from real data. Through the ability to use arbitrary algorithms to generate data,
  it opened up density estimation to a wide variety of techniques.
  Examples of galloping Zebras :cite:`Zhu.Park.Isola.ea.2017`
  and of fake celebrity faces :cite:`Karras.Aila.Laine.ea.2017`
  are both testimony to this progress.
-->

*dịch đoạn phía trên*

* Một phát triển quan trọng khác là phát minh ra Gans
  : trích dẫn: `Goodfellow.Pouget-Abadie.Mirza.ea.2014`.
  Theo truyền thống, phương pháp thống kê để ước tính mật độ
  và các mô hình thế hệ tập trung vào việc tìm phân phối xác suất phù hợp
  và (thường là gần đúng) các thuật toán để lấy mẫu từ chúng.
  Kết quả là, các thuật toán này phần lớn bị hạn chế do thiếu
  tính linh hoạt vốn có trong các mô hình thống kê.
  Sự đổi mới quan trọng trong GAN là thay thế bộ lấy mẫu
  bởi một thuật toán tùy ý với các tham số khác nhau.
  Những điều này sau đó được điều chỉnh theo cách mà người phân biệt đối xử
  (thực tế là một thử nghiệm hai mẫu) không thể phân biệt giả với dữ liệu thực. Thông qua khả năng sử dụng các thuật toán tùy ý để tạo dữ liệu,
  nó đã mở ra ước tính mật độ cho một loạt các kỹ thuật.
  Ví dụ về ngựa vằn phi mã: trích dẫn: `Zhu.Park.Isola.ea.2017`
  và của những gương mặt người nổi tiếng giả mạo: trích dẫn: `Karras.Aila.Laine.ea.2017`
  là cả hai bằng chứng cho sự tiến bộ này.


<!--
* In many cases, a single GPU is insufficient to process
  the large amounts of data available for training.
  Over the past decade the ability to build parallel
  distributed training algorithms has improved significantly.
  One of the key challenges in designing scalable algorithms
  is that the workhorse of deep learning optimization,
  stochastic gradient descent, relies on relatively
  small minibatches of data to be processed.
  At the same time, small batches limit the efficiency of GPUs.
  Hence, training on 1024 GPUs with a minibatch size of,
  say 32 images per batch amounts to an aggregate minibatch
  of 32k images. Recent work, first by Li :cite:`Li.2017`,
  and subsequently by :cite:`You.Gitman.Ginsburg.2017`
  and :cite:`Jia.Song.He.ea.2018` pushed the size up to 64k observations,
  reducing training time for ResNet50 on ImageNet to less than 7 minutes.
  For comparison\-\-initially training times were measured in the order of days.
-->

*dịch đoạn phía trên*

* Trong nhiều trường hợp, một GPU không đủ để xử lý
  số lượng lớn dữ liệu có sẵn cho đào tạo.
  Trong thập kỷ qua, khả năng xây dựng song song
  thuật toán đào tạo phân tán đã được cải thiện đáng kể.
  Một trong những thách thức chính trong việc thiết kế các thuật toán có thể mở rộng
  đó có phải là đặc điểm của tối ưu hóa học tập sâu,
  giảm dần độ dốc ngẫu nhiên, dựa vào tương đối
  xe buýt nhỏ dữ liệu được xử lý.
  Đồng thời, các lô nhỏ làm hạn chế hiệu quả của GPU.
  Do đó, đào tạo trên 1024 GPU với kích thước nhỏ gọn là,
  cho biết 32 hình ảnh trên mỗi lô với số lượng nhỏ
  hình ảnh 32k. Công việc gần đây, đầu tiên bởi Li: trích dẫn: `Li.2017`,
  và sau đó bởi: trích dẫn: `You.Gitman.Ginsburg.2017`
  và: trích dẫn: `Jia.Song.He.ea.2018` đã đẩy kích thước lên tới 64k quan sát,
  giảm thời gian đào tạo cho ResNet50 trên ImageNet xuống dưới 7 phút.
  Để so sánh \ - \ - thời gian đào tạo ban đầu được đo theo thứ tự ngày.


<!--
* The ability to parallelize computation has also contributed quite crucially
  to progress in reinforcement learning, at least whenever simulation is an
  option. This has led to significant progress in computers achieving
  superhuman performance in Go, Atari games, Starcraft, and in physics
  simulations (e.g., using MuJoCo). See e.g.,
  :cite:`Silver.Huang.Maddison.ea.2016` for a description
  of how to achieve this in AlphaGo. In a nutshell,
  reinforcement learning works best if plenty of (state, action, reward)triples are available, i.e., whenever it is possible to try out lots of things to learn how they relate to each
  other. Simulation provides such an avenue.
-->

*dịch đoạn phía trên*

* Khả năng song song hóa tính toán cũng đã đóng góp khá quan trọng
  để tiến bộ trong học tập củng cố, ít nhất là bất cứ khi nào mô phỏng là một
  tùy chọn. Điều này đã dẫn đến sự tiến bộ đáng kể trong máy tính đạt được
  hiệu suất siêu phàm trong Go, trò chơi Atari, Starcraft và trong vật lý
  mô phỏng (ví dụ: sử dụng MuJoCo). Xem ví dụ
  : trích dẫn: `Silver.Huang.Maddison.ea.2016` cho một mô tả
  về cách đạt được điều này trong AlphaGo. Tóm lại,
  học tập củng cố hoạt động tốt nhất nếu có sẵn nhiều bộ ba (trạng thái, hành động, phần thưởng), tức là, bất cứ khi nào có thể thử nhiều thứ để tìm hiểu xem chúng liên quan đến nhau như thế nào
  khác Mô phỏng cung cấp một đại lộ như vậy.


<!--
* Deep Learning frameworks have played a crucial role
  in disseminating ideas. The first generation of frameworks
  allowing for easy modeling encompassed
  [Caffe](https://github.com/BVLC/caffe),
  [Torch](https://github.com/torch), and
  [Theano](https://github.com/Theano/Theano).
  Many seminal papers were written using these tools.
  By now, they have been superseded by
  [TensorFlow](https://github.com/tensorflow/tensorflow),
  often used via its high level API [Keras](https://github.com/keras-team/keras), [CNTK](https://github.com/Microsoft/CNTK), [Caffe 2](https://github.com/caffe2/caffe2), and [Apache MxNet](https://github.com/apache/incubator-mxnet). The third generation of tools, namely imperative tools for deep learning,
  was arguably spearheaded by [Chainer](https://github.com/chainer/chainer),
  which used a syntax similar to Python NumPy to describe models.
  This idea was adopted by [PyTorch](https://github.com/pytorch/pytorch)
  and the [Gluon API](https://github.com/apache/incubator-mxnet) of MXNet.
  It is the latter group that this course uses to teach deep learning.
-->

*dịch đoạn phía trên*

* Khung học tập sâu đã đóng một vai trò quan trọng
  trong việc phổ biến ý tưởng. Thế hệ đầu tiên của khung
  cho phép mô hình hóa dễ dàng bao gồm
  [Caffe] (https://github.com/BVLC/caffe),
  [Ngọn đuốc] (https://github.com/torch) và
  [Theano] (https://github.com/Theano/Theano).
  Nhiều bài báo đã được viết bằng cách sử dụng các công cụ này.
  Đến bây giờ, chúng đã bị thay thế bởi
  [TensorFlow] (https://github.com/tensorflow/tensorflow),
  thường được sử dụng thông qua API cấp cao [Keras] (https://github.com/keras-team/keras), [CNTK] (https://github.com/Microsoft/CNTK), [Caffe 2] (https: //github.com/caffe2/caffe2) và [Apache MxNet] (https://github.com/apache/incubator-mxnet). Thế hệ thứ ba của các công cụ, cụ thể là các công cụ bắt buộc để học sâu,
  được cho là mũi nhọn của [Chainer] (https://github.com/chainer/chainer),
  đã sử dụng một cú pháp tương tự như Python NumPy để mô tả các mô hình.
  Ý tưởng này đã được [PyTorch] (https://github.com/pytorch/pytorch) áp dụng
  và [API Glamon] (https://github.com/apache/incubator-mxnet) của MXNet.
  Đây là nhóm thứ hai mà khóa học này sử dụng để dạy học sâu.


<!--
The division of labor between systems researchers building better tools
and statistical modelers building better networks
has greatly simplified things. For instance,
training a linear logistic regression model
used to be a nontrivial homework problem,
worthy to give to new machine learning
PhD students at Carnegie Mellon University in 2014.
By now, this task can be accomplished with less than 10 lines of code,
putting it firmly into the grasp of programmers.
-->

*dịch đoạn phía trên*

Sự phân công lao động giữa các nhà nghiên cứu hệ thống xây dựng các công cụ tốt hơn
và các nhà lập mô hình thống kê xây dựng mạng lưới tốt hơn
đã đơn giản hóa rất nhiều thứ. Ví dụ,
đào tạo mô hình hồi quy logistic tuyến tính
từng là một vấn đề bài tập về nhà không cần thiết,
xứng đáng để cung cấp cho máy học mới
Nghiên cứu sinh tại Đại học Carnegie Mellon năm 2014.
Đến bây giờ, nhiệm vụ này có thể được thực hiện với ít hơn 10 dòng mã,
đặt nó chắc chắn vào sự nắm bắt của các lập trình viên.


<!-- =================== Kết thúc dịch Phần 30 ==================== -->

<!-- =================== Bắt đầu dịch Phần 31 ==================== -->

<!--
## Success Stories
-->

## *dịch tiêu đề phía trên*

## Những câu chuyện thành công
<!--
Artificial Intelligence has a long history of delivering results
that would be difficult to accomplish otherwise.
For instance, mail is sorted using optical character recognition.
These systems have been deployed since the 90s
(this is, after all, the source of the famous MNIST and USPS sets of handwritten digits).
The same applies to reading checks for bank deposits and scoring
creditworthiness of applicants.
Financial transactions are checked for fraud automatically.
This forms the backbone of many e-commerce payment systems,
such as PayPal, Stripe, AliPay, WeChat, Apple, Visa, MasterCard.
Computer programs for chess have been competitive for decades.
Machine learning feeds search, recommendation, personalization
and ranking on the Internet. In other words, artificial intelligence
and machine learning are pervasive, albeit often hidden from sight.
-->

*dịch đoạn phía trên*

Trí tuệ nhân tạo có một lịch sử lâu dài trong việc cung cấp kết quả
điều đó sẽ khó thực hiện bằng cách khác.
Ví dụ, thư được sắp xếp bằng nhận dạng ký tự quang học.
Các hệ thống này đã được triển khai từ những năm 90
(cuối cùng, đây là nguồn gốc của bộ chữ số viết tay nổi tiếng của MNIST và USPS).
Điều tương tự cũng áp dụng cho việc đọc séc đối với tiền gửi ngân hàng và tính điểm
uy tín của ứng viên.
Giao dịch tài chính được kiểm tra gian lận tự động.
Điều này tạo thành xương sống của nhiều hệ thống thanh toán thương mại điện tử,
chẳng hạn như PayPal, Stripe, AliPay, WeChat, Apple, Visa, MasterCard.
Các chương trình máy tính cho cờ vua đã cạnh tranh trong nhiều thập kỷ.
Máy học thức ăn tìm kiếm, đề xuất, cá nhân hóa
và xếp hạng trên Internet. Nói cách khác, trí tuệ nhân tạo
và học máy là phổ biến, mặc dù thường ẩn khỏi tầm nhìn.


<!--
It is only recently that AI has been in the limelight, mostly due to
solutions to problems that were considered intractable previously.
-->

*dịch đoạn phía trên*

Chỉ gần đây, AI đã ở trong ánh đèn sân khấu, chủ yếu là do
giải pháp cho các vấn đề được coi là khó chữa trước đây.


<!-- =================== Kết thúc dịch Phần 31 ==================== -->

<!-- =================== Bắt đầu dịch Phần 32 ==================== -->

<!--
* Intelligent assistants, such as Apple's Siri, Amazon's Alexa, or Google's
  assistant are able to answer spoken questions with a reasonable degree of
  accuracy. This includes menial tasks such as turning on light switches (a boon to the disabled) up to making barber's appointments and offering phone support dialog. This is likely the most noticeable sign that AI is affecting our lives.
-->

*dịch đoạn phía trên*


* Các trợ lý thông minh, như Siri của Apple, Alexa của Amazon hoặc của Google
  trợ lý có thể trả lời các câu hỏi nói với mức độ hợp lý
  độ chính xác. Điều này bao gồm các nhiệm vụ cấp độ như bật công tắc đèn (một lợi ích cho người khuyết tật) để thực hiện các cuộc hẹn của thợ cắt tóc và cung cấp hộp thoại hỗ trợ qua điện thoại. Đây có thể là dấu hiệu đáng chú ý nhất cho thấy AI đang ảnh hưởng đến cuộc sống của chúng ta.


<!--
* A key ingredient in digital assistants is the ability to recognize speech
  accurately. Gradually the accuracy of such systems has increased to the point
  where they reach human parity :cite:`Xiong.Wu.Alleva.ea.2018` for certain
  applications.
-->

*dịch đoạn phía trên*


* Một thành phần quan trọng trong trợ lý kỹ thuật số là khả năng nhận dạng giọng nói
  một cách chính xác. Dần dần độ chính xác của các hệ thống như vậy đã tăng lên đến mức
  nó đạt đến sự ngang nhau của con người: trích dẫn: `Xiong.Wu.Alleva.ea.2018`
  các ứng dụng.


<!--
* Object recognition likewise has come a long way. Estimating the object in a
  picture was a fairly challenging task in 2010. On the ImageNet benchmark
  :cite:`Lin.Lv.Zhu.ea.2010` achieved a top-5 error rate of 28%. By 2017,
  :cite:`Hu.Shen.Sun.2018` reduced this error rate to 2.25%. Similarly stunning
  results have been achieved for identifying birds, or diagnosing skin cancer.
-->

*dịch đoạn phía trên*

* Nhận dạng đối tượng tương tự đã đi một chặng đường dài. Ước tính đối tượng trong một
  hình ảnh là một nhiệm vụ khá khó khăn trong năm 2010. Trên điểm chuẩn ImageNet
  : trích dẫn: `Lin.Lv.Zhu.ea.2010` đạt tỷ lệ lỗi top 5 là 28%. Vào năm 2017,
  : trích dẫn: `Hu.Shen.Sun.2018` đã giảm tỷ lệ lỗi này xuống 2,25%. Những kết quả tuyệt vời tương tự 
  đã đạt được để xác định chim, hoặc chẩn đoán ung thư da.


<!--
* Games used to be a bastion of human intelligence.
  Starting from TDGammon [23], a program for playing Backgammon
  using temporal difference (TD) reinforcement learning,
  algorithmic and computational progress has led to algorithms
  for a wide range of applications. Unlike Backgammon,
  chess has a much more complex state space and set of actions.
  DeepBlue beat Gary Kasparov, Campbell et al.
  :cite:`Campbell.Hoane-Jr.Hsu.2002`, using massive parallelism,
  special purpose hardware and efficient search through the game tree.
  Go is more difficult still, due to its huge state space.
  AlphaGo reached human parity in 2015, :cite:`Silver.Huang.Maddison.ea.2016` using Deep Learning combined with Monte Carlo tree sampling.
  The challenge in Poker was that the state space is
  large and it is not fully observed (we do not know the opponents'
  cards). Libratus exceeded human performance in Poker using efficiently
  structured strategies :cite:`Brown.Sandholm.2017`.
  This illustrates the impressive progress in games
  and the fact that advanced algorithms played a crucial part in them.
-->

*dịch đoạn phía trên*

* Trò chơi từng là một pháo đài của trí tuệ con người.
  Bắt đầu từ TDGammon [23], một chương trình để chơi Backgammon
  sử dụng học tập củng cố sự khác biệt theo thời gian (TD),
  sự tiến bộ về thuật toán và tính toán đã dẫn đến các thuật toán
  cho một loạt các ứng dụng. Không giống như Backgammon,
  cờ vua có một không gian nhà nước phức tạp hơn nhiều và tập hợp các hành động.
  DeepBlue đánh bại Gary Kasparov, Campbell và cộng sự.
  : trích dẫn: `Campbell.Hoane-Jr.Hsu.2002`, sử dụng song song lớn,
  phần cứng mục đích đặc biệt và tìm kiếm hiệu quả thông qua cây trò chơi.
  Đi vẫn khó khăn hơn, do không gian nhà nước rất lớn.
  AlphaGo đạt được sự bình đẳng của con người vào năm 2015 ,: trích dẫn: `Silver.Huang.Maddison.ea.2016` bằng cách sử dụng Deep Learning kết hợp với lấy mẫu cây Monte Carlo.
  Thách thức trong Poker là không gian nhà nước là
  lớn và nó không được quan sát đầy đủ (chúng tôi không biết đối thủ '
  thẻ). Libratus vượt quá hiệu suất của con người trong Poker bằng cách sử dụng hiệu quả
  chiến lược có cấu trúc: trích dẫn: `Brown.Sandholm.2017`.
  Điều này minh họa cho sự tiến bộ ấn tượng trong các trò chơi
  và thực tế là các thuật toán tiên tiến đã đóng một phần quan trọng trong chúng.


<!--
* Another indication of progress in AI is the advent of self-driving cars
  and trucks. While full autonomy is not quite within reach yet,
  excellent progress has been made in this direction,
  with companies such as Tesla, NVIDIA,
  and Waymo shipping products that enable at least partial autonomy.
  What makes full autonomy so challenging is that proper driving
  requires the ability to perceive, to reason and to incorporate rules
  into a system. At present, deep learning is used primarily
  in the computer vision aspect of these problems.
  The rest is heavily tuned by engineers.
-->

*dịch đoạn phía trên*

* Một dấu hiệu khác cho thấy sự tiến bộ trong AI là sự ra đời của những chiếc xe tự lái
  và xe tải. Mặc dù quyền tự chủ hoàn toàn chưa hoàn toàn nằm trong tầm tay,
  tiến bộ tuyệt vời đã được thực hiện theo hướng này,
  với các công ty như Tesla, NVIDIA,
  và các sản phẩm vận chuyển Waymo cho phép ít nhất một phần tự chủ.
  Điều làm cho sự tự chủ hoàn toàn trở nên thách thức là lái xe đúng cách
  đòi hỏi khả năng nhận thức, lý luận và kết hợp các quy tắc
  thành một hệ thống. Hiện nay, học sâu được sử dụng chủ yếu
  trong khía cạnh tầm nhìn máy tính của những vấn đề này.
  Phần còn lại được điều chỉnh bởi các kỹ sư.


<!-- =================== Kết thúc dịch Phần 32 ==================== -->

<!-- =================== Bắt đầu dịch Phần 33 ==================== -->

<!--
Again, the above list barely scratches the surface of where machine learning has impacted practical applications. For instance, robotics, logistics, computational biology, particle physics, and astronomy owe some of their most impressive recent advances at least in parts to machine learning. ML is thus becoming a ubiquitous tool for engineers and scientists.
-->

*dịch đoạn phía trên*

Một lần nữa, danh sách trên hầu như không làm trầy xước bề mặt nơi học máy đã ảnh hưởng đến các ứng dụng thực tế. Ví dụ, người máy, hậu cần, sinh học tính toán, vật lý hạt và thiên văn học có một số tiến bộ ấn tượng gần đây nhất của họ, ít nhất là trong các phần của học máy. ML vì thế đang trở thành một công cụ phổ biến cho các kỹ sư và nhà khoa học.


<!--
Frequently, the question of the AI apocalypse, or the AI singularity
has been raised in non-technical articles on AI.
The fear is that somehow machine learning systems
will become sentient and decide independently from their programmers
(and masters) about things that directly affect the livelihood of humans.
To some extent, AI already affects the livelihood of humans
in an immediate way---creditworthiness is assessed automatically,
autopilots mostly navigate cars, decisions about
whether to grant bail use statistical data as input.
More frivolously, we can ask Alexa to switch on the coffee machine.
-->

*dịch đoạn phía trên*

Thông thường, câu hỏi về ngày tận thế AI, hay sự kỳ dị của AI
đã được nêu ra trong các bài báo phi kỹ thuật về AI.
Điều đáng sợ là bằng cách nào đó hệ thống máy học
sẽ trở nên đa cảm và quyết định độc lập với các lập trình viên của họ
(và thạc sĩ) về những thứ ảnh hưởng trực tiếp đến sinh kế của con người.
Ở một mức độ nào đó, AI đã ảnh hưởng đến sinh kế của con người
một cách tức thời --- uy tín tín dụng được đánh giá tự động,
autopilots chủ yếu điều hướng xe ô tô, quyết định về
có cho phép tại ngoại sử dụng dữ liệu thống kê làm đầu vào.
Phù phiếm hơn, chúng ta có thể yêu cầu Alexa bật máy pha cà phê.


<!--
Fortunately, we are far from a sentient AI system
that is ready to manipulate its human creators (or burn their coffee).
First, AI systems are engineered, trained and deployed in a specific,
goal-oriented manner. While their behavior might give the illusion
of general intelligence, it is a combination of rules, heuristics
and statistical models that underlie the design.
Second, at present tools for *artificial general intelligence*
simply do not exist that are able to improve themselves,
reason about themselves, and that are able to modify,
extend and improve their own architecture
while trying to solve general tasks.
-->

*dịch đoạn phía trên*

May mắn thay, chúng ta cách xa một hệ thống AI đa cảm
đã sẵn sàng để thao túng người tạo ra nó (hoặc đốt cà phê của họ).
Đầu tiên, các hệ thống AI được thiết kế, đào tạo và triển khai một cách cụ thể,
cách định hướng mục tiêu. Trong khi hành vi của họ có thể tạo ảo giác
của trí thông minh chung, nó là sự kết hợp của các quy tắc, heuristic
và các mô hình thống kê làm nền tảng cho thiết kế.
Thứ hai, hiện tại các công cụ cho * trí thông minh nhân tạo *
chỉ đơn giản là không tồn tại mà có thể cải thiện bản thân,
lý do về bản thân và có thể sửa đổi,
mở rộng và cải thiện kiến trúc của riêng họ
trong khi cố gắng giải quyết các nhiệm vụ chung.


<!--
A much more pressing concern is how AI is being used in our daily lives.
It is likely that many menial tasks fulfilled by truck drivers
and shop assistants can and will be automated.
Farm robots will likely reduce the cost for organic farming
but they will also automate harvesting operations.
This phase of the industrial revolution
may have profound consequences on large swaths of society
(truck drivers and shop assistants are some
of the most common jobs in many states).
Furthermore, statistical models, when applied without care
can lead to racial, gender or age bias and raise
reasonable concerns about procedural fairness
if automated to drive consequential decisions.
It is important to ensure that these algorithms are used with care.
With what we know today, this strikes us a much more pressing concern
than the potential of malevolent superintelligence to destroy humanity.
-->

*dịch đoạn phía trên*

Một mối quan tâm cấp bách hơn nhiều là cách AI đang được sử dụng trong cuộc sống hàng ngày của chúng ta.
Có khả năng nhiều nhiệm vụ nguy hiểm được thực hiện bởi các tài xế xe tải
và trợ lý cửa hàng có thể và sẽ được tự động.
Robot nông nghiệp có thể sẽ giảm chi phí cho canh tác hữu cơ
nhưng họ cũng sẽ tự động hóa hoạt động thu hoạch.
Giai đoạn này của cuộc cách mạng công nghiệp
có thể có những hậu quả sâu sắc đối với những vùng rộng lớn của xã hội
(tài xế xe tải và trợ lý cửa hàng là một số
của các công việc phổ biến nhất ở nhiều tiểu bang).
Hơn nữa, các mô hình thống kê, khi áp dụng mà không cần quan tâm
có thể dẫn đến sự phân biệt chủng tộc, giới tính hoặc tuổi tác và nâng cao
mối quan tâm hợp lý về sự công bằng thủ tục
nếu tự động để lái các quyết định hậu quả.
Điều quan trọng là đảm bảo rằng các thuật toán này được sử dụng cẩn thận.
Với những gì chúng ta biết ngày nay, điều này gây cho chúng ta một mối quan tâm cấp bách hơn nhiều
hơn tiềm năng của siêu trí tuệ độc ác để tiêu diệt loài người.


<!-- =================== Kết thúc dịch Phần 33 ==================== -->

<!-- =================== Bắt đầu dịch Phần 34 ==================== -->

<!--
## Summary
-->

## *dịch tiêu đề phía trên*

## Tóm tắt

<!--
* Machine learning studies how computer systems can leverage *experience* (often data) to improve performance at specific tasks. It combines ideas from statistics, data mining, artificial intelligence, and optimization. Often, it is used as a means of implementing artificially-intelligent solutions.
* As a class of machine learning, representational learning focuses on how to automatically find the appropriate way to represent data. This is often accomplished by a progression of learned transformations.
* Much of the recent progress in deep learning has been triggered by an abundance of data arising from cheap sensors and Internet-scale applications, and by significant progress in computation, mostly through GPUs.
* Whole system optimization is a key component in obtaining good performance. The availability of efficient deep learning frameworks has made design and implementation of this significantly easier.
-->

*dịch đoạn phía trên*

* Học máy nghiên cứu làm thế nào các hệ thống máy tính có thể tận dụng * kinh nghiệm * (thường là dữ liệu) để cải thiện hiệu suất ở các tác vụ cụ thể. Nó kết hợp các ý tưởng từ thống kê, khai thác dữ liệu, trí tuệ nhân tạo và tối ưu hóa. Thông thường, nó được sử dụng như một phương tiện để thực hiện các giải pháp thông minh nhân tạo.
* Là một lớp học máy, học đại diện tập trung vào cách tự động tìm cách thích hợp để biểu diễn dữ liệu. Điều này thường được thực hiện bằng một sự tiến triển của các biến đổi đã học.
* Phần lớn tiến bộ gần đây trong học tập sâu đã được kích hoạt bởi sự phong phú của dữ liệu phát sinh từ các cảm biến giá rẻ và các ứng dụng quy mô Internet và bằng tiến bộ đáng kể trong tính toán, chủ yếu thông qua GPU.
* Tối ưu hóa toàn bộ hệ thống là một thành phần quan trọng để có được hiệu suất tốt. Sự sẵn có của các khung học sâu hiệu quả đã giúp cho việc thiết kế và thực hiện việc này trở nên dễ dàng hơn đáng kể.


<!--
## Exercises
-->

## *dịch tiêu đề phía trên*

## Bài tập


<!--
1. Which parts of code that you are currently writing could be "learned", i.e., improved by learning and automatically determining design choices that are made in your code? Does your code include heuristic design choices?
1. Which problems that you encounter have many examples for how to solve them, yet no specific way to automate them? These may be prime candidates for using deep learning.
1. Viewing the development of artificial intelligence as a new industrial revolution, what is the relationship between algorithms and data? Is it similar to steam engines and coal (what is the fundamental difference)?
1. Where else can you apply the end-to-end training approach? Physics? Engineering? Econometrics?
-->

*dịch đoạn phía trên*

1. Phần nào của mã mà bạn hiện đang viết có thể được "học", tức là, được cải thiện bằng cách học và tự động xác định các lựa chọn thiết kế được thực hiện trong mã của bạn? Mã của bạn có bao gồm các lựa chọn thiết kế tự khám phá (heuristic design choices)?
1. Những vấn đề mà bạn gặp phải có nhiều ví dụ về cách giải quyết chúng, nhưng không có cách cụ thể nào để tự động hóa chúng? Đây có thể là ứng cử viên chính cho việc sử dụng học tập sâu.
1. Xem sự phát triển của trí tuệ nhân tạo như một cuộc cách mạng công nghiệp mới, mối quan hệ giữa thuật toán và dữ liệu là gì? Nó có giống với động cơ hơi nước và than không (sự khác biệt cơ bản) là gì?
1. Trường hợp khác bạn có thể áp dụng phương pháp đào tạo từ đầu đến cuối? Vật lý? Kỹ thuật? Kinh tế lượng?


<!--
## [Discussions](https://discuss.mxnet.io/t/2310)
-->

## *dịch tiêu đề phía trên*

<!--
![](../img/qr_introduction.svg)
-->

![*dịch chú thích ảnh phía trên*](../img/qr_introduction.svg)

<!-- =================== Kết thúc dịch Phần 34 ==================== -->

### Những người thực hiện
Bản dịch trong trang này được thực hiện bởi:
<!--
Tác giả của mỗi Pull Request điền tên mình và tên những người review mà bạn thấy
hữu ích vào từng phần tương ứng. Mỗi dòng một tên.

Lưu ý:
* Mỗi tên chỉ xuất hiện một lần: Nếu bạn đã dịch hoặc review phần 1 của trang này
thì không cần điền vào các phần sau nữa.
* Nếu reviewer không cung cấp tên, bạn có thể dùng tên tài khoản GitHub của họ
với dấu `@` ở đầu. Ví dụ: @aivivn.
-->

<!-- Phần 1 -->
*

<!-- Phần 2 -->
*

<!-- Phần 3 -->
*

<!-- Phần 4 -->
*

<!-- Phần 5 -->
*

<!-- Phần 6 -->
*

<!-- Phần 7 -->
*

<!-- Phần 8 -->
*

<!-- Phần 9 -->
*

<!-- Phần 10 -->
*

<!-- Phần 11 -->
*

<!-- Phần 12 -->
*

<!-- Phần 13 -->
*

<!-- Phần 14 -->
*

<!-- Phần 15 -->
*

<!-- Phần 16 -->
*

<!-- Phần 17 -->
*

<!-- Phần 18 -->
*

<!-- Phần 19 -->
*

<!-- Phần 20 -->
*

<!-- Phần 21 -->
*

<!-- Phần 22 -->
*

<!-- Phần 23 -->
*

<!-- Phần 24 -->
*

<!-- Phần 25 -->
*

<!-- Phần 26 -->
*

<!-- Phần 27 -->
*

<!-- Phần 28 -->
*

<!-- Phần 29 -->
*

<!-- Phần 30 -->
*

<!-- Phần 31 -->
*

<!-- Phần 32 -->
*

<!-- Phần 33 -->
*

<!-- Phần 34 -->
*
