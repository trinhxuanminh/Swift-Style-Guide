# Hướng dẫn phong cách Swift (Swift Style Guide)

- Mục tiêu bao trùm của chúng ta là rõ ràng, nhất quán và ngắn gọn, theo thứ tự, hợp lý hoá luồng nội dung.
- Đảm bảo rằng loại bỏ nhiều gánh nặng cho người đọc.

## Mục lục

* [1 - Tính đúng đắn](#1---tính-đúng-đắn)
* [2 - Sử dụng SwiftLint](#2-sử-dụng-swiftlint)
    * [a. Cài đặt](#a-cài-đặt)
    * [b. Tham chiếu quy tắc](#b-tham-chiếu-quy-tắc)
* [3 - Quy tắc đặt tên](#3-quy-tắc-đặt-tên)
    * [a. Sự rõ ràng tại điểm sử dụng](#a-sự-rõ-ràng-tại-điểm-sử-dụng)
    * [b. Sự rõ ràng quan trọng hơn sự ngắn gọn](#b-sự-rõ-ràng-quan-trọng-hơn-sự-ngắn-gọn)
    * [c. Thúc đẩy sự rõ ràng](#c-thúc-đẩy-sự-rõ-ràng)
    * [d. Phấn đấu để sử dụng thành thạo](#d-phấn-đấu-để-sử-dụng-thành-thạo)
    * [e. Sử dụng thuật ngữ tốt](#e-sử-dụng-thuật-ngữ-tốt)
    * [f. Các quy ước chung](#f-các-quy-ước-chung)
    * [g. Tham số](#g-tham-số)
    * [h. Nhãn đối số](#h-nhãn-đối-số)
    * [i. Hướng dẫn đặc biệt](#i-hướng-dẫn-đặc-biệt)
    * [k. Prose](#k-prose)
    * [l. Tiền tố lớp](#l-tiền-tố-lớp)
    * [m. Delegates](#m-delegates)
    * [n. Sử dụng loại Inferred Context](#n-sử-dụng-loại-inferred-context)
    * [o. Generics](#o-generics)
    * [p. Ngôn ngữ](#p-ngôn-ngữ)
* [4 - Tổ chức mã](#4-tổ-chức-mã)
    * [a. Tuân thủ giao thức](#a-tuân-thủ-giao-thức)
    * [b. Mã không sử dụng](#b-mã-không-sử-dụng)
    * [c. Minimal Imports](#c-minimal-imports)
* [5 - Khoảng cách](#5-khoảng-cách)
* [6 - Bình luận](#6-bình-luận)
    * [a. Sử dụng phương ngữ Markdown](#a-sử-dụng-phương-ngữ-markdown)
    * [b. Bắt đầu bằng một bản tóm tắt](#b-bắt-đầu-bằng-một-bản-tóm-tắt)
    * [c. Theo tuỳ chọn](#c-theo-tuỳ-chọn)
* [7 - Classes and Structures](#7-classes-and-structures)
* [8 - Khai báo hàm](#8-khai-báo-hàm)
* [9 - Lệnh gọi hàm](#9-lệnh-gọi-hàm)
* [10 - Biểu thức Closure](#10-biểu-thức-closure)
* [11 - Types](#11-types)
    * [a. Constants](#a-constants)
    * [b. Phương thức tĩnh và thuộc tính kiểu biến](#b-phương-thức-tĩnh-và-thuộc-tính-kiểu-biến)
    * [c. Optionals](#c-optionals)
    * [d. Khởi tạo Lazy](#d-khởi-tạo-lazy)
    * [e. Kiểu suy luận](#e-kiểu-suy-luận)
    * [f. Syntactic Sugar](#f-syntactic-sugar)
* [12 - Functions vs Methods](#12-functions-vs-methods)
* [13 - Quản lý bộ nhớ](#13-quản-lý-bộ-nhớ)
    * [a. Kéo dài thời gian tồn tại của đối tượng](#a-kéo-dài-thời-gian-tồn-tại-của-đối-tượng)
* [14 - Kiểm soát truy cập](#14-kiểm-soát-truy-cập)
* [15 - Luồng điều khiển](#15-luồng-điều-khiển)
    * [a. Toán tử bậc ba](#a-toán-tử-bậc-ba)
* [16 - Con đường vàng](#16-con-đường-vàng)
    * [a. Failing Guards](#a-failing-guards)
* [17 - Dấu chấm phẩy](#17-dấu-chấm-phẩy)
* [18 - Dấu ngoặc đơn](#18-dấu-ngoặc-đơn)
* [19 - Chữ viết chuỗi nhiều dòng](#19-chữ-viết-chuỗi-nhiều-dòng)
* [20 - Không có biểu tượng cảm xúc](#20-không-có-biểu-tượng-cảm-xúc)
* [21 - Không #imageLiteral hoặc #colorLiteral](#21-không-imageliteral-hoặc-colorliteral)

## 1 - Tính đúng đắn

- Cố gắng làm cho mã của bạn được biên dịch mà không có cảnh báo.
- Quy tắc này thông báo nhiều quyết định về kiểu dáng.

## 2 - Sử dụng SwiftLint

- `SwiftLint` được thiết kế để đảm bảo tuân thủ các quy tắc tiêu chuẩn được cộng đồng Swift chấp nhận.

### a. Cài đặt

- Truy cập [SwiftLint documentation](https://github.com/realm/SwiftLint) để cài đặt, cấu hình Xcode và xử lý ngoại lệ.

### b. Tham chiếu quy tắc

- Truy cập [Thư mục quy tắc](https://realm.github.io/SwiftLint/rule-directory.html)

## 3 - Quy tắc đặt tên

- Đặt tên mô tả và nhất quán giúp phần mềm dễ đọc và dễ hiểu hơn.

### a. Sự rõ ràng tại điểm sử dụng

- Là mục tiêu quan trọng nhất của bạn.
- Các thực thể như phương thức và thuộc tính chỉ được khai báo một lần nhưng được sử dụng nhiều lần.
- Thiết kế các API để làm cho các mục đích sử dụng đó trở nên rõ ràng và ngắn gọn.
- Khi đánh giá một thiết kế, việc đọc một tuyên bố hiếm khi là đủ; luôn kiểm tra một Use Case để đảm bảo rằng nó trông rõ ràng trong ngữ cảnh.

### b. Sự rõ ràng quan trọng hơn sự ngắn gọn

- Mặc dù mã Swift có thể nhỏ gọn, nhưng mục tiêu không phải là kích hoạt mã nhỏ nhất có thể với ít ký tự nhất.
- Sự hấp dẫn trong mã Swift, nơi nó xảy ra, là một tác dụng phụ của hệ thống kiểu mạnh và các tính năng làm giảm tự nhiên các bản soạn sẵn.

### c. Thúc đẩy sự rõ ràng

#### Bao gồm tất cả các từ cần thiết

- Để tránh sự mơ hồ đối với người đọc mã nơi tên được sử dụng.

Ví dụ: hãy xem xét một phương pháp loại bỏ phần tử tại một vị trí nhất định trong một tập hợp

##### ✅ Ưu tiên:

```swift
extension List {
  public mutating func remove(at position: Index) -> Element
}
employees.remove(at: x)
```

Nếu chúng ta bỏ từ **at** khỏi chữ ký của phương thức, nó có thể ngụ ý với người đọc rằng phương thức tìm kiếm và loại bỏ một phần tử bằng **x**, thay vì sử dụng **x** để chỉ ra vị trí của phần tử cần loại bỏ.

##### ⛔️ Không được ưa thích:

```swift
employees.remove(x) // unclear: are we removing x?
```

#### Bỏ qua những từ không cần thiết

- Mỗi từ trong tên phải truyền tải thông tin nổi bật tại nơi sử dụng.

Có thể cần nhiều từ hơn để làm rõ ý định hoặc phân biệt ý nghĩa, nhưng những từ thừa với thông tin mà người đọc đã sở hữu nên được bỏ qua. Đặc biệt, hãy lược bỏ những từ _**chỉ đơn thuần lặp lại**_ thông tin loại.

##### ⛔️ Không được ưa thích:

```swift
public mutating func removeElement(_ member: Element) -> Element?

allViews.removeElement(cancelButton)
```

Trong trường hợp này, từ **Element** này không thêm gì nổi bật tại điểm gọi. API này sẽ tốt hơn:

##### ✅ Ưu tiên:

```swift
public mutating func remove(_ member: Element) -> Element?

allViews.remove(cancelButton) // clearer
```

Đôi khi, thông tin kiểu lặp lại là cần thiết để tránh sự mơ hồ, nhưng nói chung, tốt hơn là sử dụng một từ mô tả vai trò của một tham số hơn là kiểu của nó.

#### Đặt tên cho các biến, tham số và các kiểu được liên kết theo vai trò của chúng

- Không đặt theo các ràng buộc về kiểu của chúng.

##### ⛔️ Không được ưa thích:

```swift
var string = "Hello"
protocol ViewController {
  associatedtype ViewType : View
}
class ProductionLine {
  func restock(from widgetFactory: WidgetFactory)
}
```

Việc đặt tên kiểu theo cách này không thể tối ưu hóa sự rõ ràng và dễ hiểu. Thay vào đó, hãy cố gắng chọn một cái tên thể hiện _**vai trò**_ của nó.

##### ✅ Ưu tiên:

```swift
var greeting = "Hello"
protocol ViewController {
  associatedtype ContentView : View
}
class ProductionLine {
  func restock(from supplier: WidgetFactory)
}
```

Nếu một loại được liên kết bị ràng buộc chặt chẽ với ràng buộc giao thức của nó đến mức tên giao thức là vai trò, hãy tránh xung đột bằng cách thêm Protocol vào tên giao thức:

```swift
protocol Sequence {
  associatedtype Iterator : IteratorProtocol
}
protocol IteratorProtocol { ... }
```

#### Bù cho thông tin loại yếu

- Làm rõ vai trò của tham số.

Đặc biệt khi một loại tham số là NSObject, Any, AnyObject, hoặc một loại cơ bản như là Int hoặc String, loại thông tin và ngữ cảnh tại điểm sử dụng có thể không truyền đạt đầy đủ ý định. Trong ví dụ này, khai báo có thể rõ ràng, nhưng điểm sử dụng thì mơ hồ.

##### ⛔️ Không được ưa thích:

```swift
func add(_ observer: NSObject, for keyPath: String)

grid.add(self, for: graphics) // vague
```

Để khôi phục độ rõ ràng, hãy **đặt trước mỗi tham số được nhập yếu bằng một danh từ mô tả vai trò của nó**:

##### ✅ Ưu tiên:

```swift
func addObserver(_ observer: NSObject, forKeyPath path: String)

grid.addObserver(self, forKeyPath: graphics) // clear
```

### d. Phấn đấu để sử dụng thành thạo

#### Ưu tiên các tên phương pháp và chức năng giúp các điểm sử dụng tạo thành các cụm từ tiếng Anh đúng ngữ pháp

##### ✅ Ưu tiên:

```swift
x.insert(y, at: z) // x, insert y at z
x.subViews(havingColor: y) // x's subviews having color y
x.capitalizingNouns() // x, capitalizing nouns
```

##### ⛔️ Không được ưa thích:

```swift
x.insert(y, position: z)
x.subViews(color: y)
x.nounCapitalize()
```

Có thể chấp nhận được sự trôi chảy suy giảm sau một hoặc hai đối số đầu tiên khi những đối số đó không phải là trọng tâm của ý nghĩa của lệnh gọi:

```swift
AudioUnit.instantiate(
  with: description, 
  options: [.inProcess], completionHandler: stopProgressBar)
```

#### Bắt đầu tên của các phương thức gốc bằng “make”

Ví dụ:

```swift
x.makeIterator()
```

#### Đối số đầu tiên cho các lệnh gọi phương thức khởi tạo và ban đầu không được tạo thành một cụm từ bắt đầu bằng tên cơ sở

Ví dụ: các đối số đầu tiên cho các lệnh gọi này không được đọc như một phần của cùng một cụm từ với tên cơ sở

##### ✅ Ưu tiên:

```swift
let foreground = Color(red: 32, green: 64, blue: 128)
let newPart = factory.makeWidget(gears: 42, spindles: 14)
let ref = Link(target: destination)
```

Trong phần sau, tác giả API đã cố gắng tạo ra sự liên tục về ngữ pháp với đối số đầu tiên.

##### ⛔️ Không được ưa thích:

```swift
let foreground = Color(havingRGBValuesRed: 32, green: 64, andBlue: 128)
let newPart = factory.makeWidget(havingGearCount: 42, andSpindleCount: 14)
let ref = Link(to: destination)
```

Trên thực tế, hướng dẫn này cùng với hướng dẫn dành cho [nhãn đối số](#h-nhãn-đối-số) có nghĩa là đối số đầu tiên sẽ có nhãn trừ khi lệnh gọi đang thực hiện [chuyển đổi kiểu bảo toàn giá trị](#trong-các-trình-khởi-tạo-thực-hiện-chuyển-đổi-kiểu-bảo-toàn-giá-trị-hãy-bỏ-qua-nhãn-đối-số-đầu-tiên).

```swift
let rgbForeground = RGBColor(cmykForeground)
```

#### Đặt tên cho các chức năng và phương pháp theo phản ứng phụ của chúng

- Những loại không có phản ứng phụ nên đặt là cụm danh từ.

```swift
x.distance(to: y)
i.successor()
```

- Những từ có phản ứng phụ nên đặt là cụm động từ mệnh lệnh.

```swift
print(x)
x.sort()
x.append(y)
```

- Đặt tên cho các cặp phương thức đột biến/không thay đổi một cách nhất quán. Một phương thức thay đổi thường sẽ có một biến thể không thay đổi với ngữ nghĩa tương tự, nhưng nó trả về một giá trị mới thay vì cập nhật một thể hiện tại chỗ.

    - Khi thao tác được mô tả một cách tự nhiên bởi một động từ, hãy sử dụng mệnh lệnh của động từ đó cho phương thức biến âm và áp dụng hậu tố “ed” hoặc “ing” để đặt tên cho đối từ không biến âm của nó.
    - Khi thao tác được mô tả một cách tự nhiên bởi một danh từ , hãy sử dụng danh từ cho phương thức không thay đổi và áp dụng tiền tố “form” để đặt tên cho phương thức biến đổi của nó.

- Việc sử dụng các phương thức và thuộc tính Boolean phải được đọc dưới dạng xác nhận khi việc sử dụng là không thay đổi.

```swift
x.isEmpty()
line1.intersects(line2)
```

- Các giao thức mô tả thứ gì đó sẽ được đặt dưới dạng danh từ.
- Các giao thức mô tả một khả năng phải được đặt tên bằng cách sử dụng các hậu tố able, ible, or ing.
- Tên của các kiểu, thuộc tính, biến và hằng số khác nên đặt như danh từ.

### e. Sử dụng thuật ngữ tốt

- **Thuật ngữ nghệ thuật**: danh từ - một từ hoặc cụm từ có nghĩa chính xác, chuyên biệt trong một lĩnh vực hoặc nghề nghiệp cụ thể.

#### Tránh các thuật ngữ khó hiểu

- Dùng một từ phổ biến hơn cùng truyền đạt ý nghĩa.
- Đừng nói “epidermis” nếu “skin” phù hợp với mục đích của bạn.
- Thuật ngữ nghệ thuật là một công cụ giao tiếp thiết yếu, nhưng chỉ nên được sử dụng để nắm bắt ý nghĩa quan trọng mà nếu không sẽ bị mất.

#### Hãy bám sát ý nghĩa đã thiết lập

Lý do duy nhất để sử dụng một thuật ngữ kỹ thuật thay vì một từ phổ biến hơn là nó diễn đạt chính xác một điều gì đó có thể mơ hồ hoặc không rõ ràng. Do đó, một API nên sử dụng thuật ngữ này theo đúng nghĩa được chấp nhận của nó.

- **Đừng làm cho một chuyên gia ngạc nhiên**: bất kỳ ai đã quen thuộc với thuật ngữ này sẽ ngạc nhiên và có thể tức giận nếu chúng ta dường như đã phát minh ra một nghĩa mới cho nó.
- **Đừng gây nhầm lẫn cho người mới bắt đầu**: bất kỳ ai cố gắng học thuật ngữ này đều có khả năng thực hiện tìm kiếm trên web và tìm ra nghĩa truyền thống của nó.

#### Tránh viết tắt

- Các từ viết tắt, đặc biệt là các từ không chuẩn, là thuật ngữ nghệ thuật một cách hiệu quả, bởi vì sự hiểu biết phụ thuộc vào việc dịch chúng thành dạng không viết tắt của chúng một cách chính xác.
- Ý nghĩa dự định cho bất kỳ chữ viết tắt nào bạn sử dụng phải dễ dàng tìm thấy bằng cách tìm kiếm trên web.

#### Ôm tiền lệ

 - Đừng tối ưu hóa các điều khoản cho người mới bắt đầu với chi phí phù hợp với văn hóa hiện có.

    - Tốt hơn là đặt tên Array cho một cấu trúc dữ liệu liền kề hơn là sử dụng một thuật ngữ đơn giản hóa, chẳng hạn như List, mặc dù người mới bắt đầu có thể hiểu ý nghĩa của List dễ dàng hơn. Mảng là yếu tố cơ bản trong máy tính hiện đại, vì vậy mọi lập trình viên đều biết — hoặc sẽ sớm biết — mảng là gì. Sử dụng một thuật ngữ mà hầu hết các lập trình viên đều quen thuộc và các tìm kiếm và câu hỏi trên web của họ sẽ được thưởng.

    - Trong một lĩnh vực lập trình cụ thể, chẳng hạn như toán học, một thuật ngữ chưa từng được biết đến rộng rãi như sin(x) được ưu tiên hơn một cụm từ giải thích chẳng hạn như verticalPositionOnUnitCircleAtOriginOfEndOfRadiusWithAngle(x). Lưu ý rằng trong trường hợp này, tiền lệ vượt trội hơn hướng dẫn tránh viết tắt: mặc dù từ đầy đủ là sine, “sin(x)” đã được sử dụng phổ biến trong các lập trình viên trong nhiều thập kỷ và các nhà toán học trong nhiều thế kỷ.

### f. Các quy ước chung

#### Ghi lại độ phức tạp của bất kỳ thuộc tính tính toán nào không phải là O(1)

- Mọi người thường cho rằng truy cập thuộc tính không liên quan đến tính toán đáng kể, bởi vì chúng có các thuộc tính được lưu trữ dưới dạng mô hình tinh thần. Hãy chắc chắn cảnh báo họ khi giả định đó có thể bị vi phạm.

#### Ưu tiên các phương thức và thuộc tính cho các chức năng miễn phí

- Các chức năng miễn phí chỉ được sử dụng trong các trường hợp đặc biệt:

    - Khi bản thân không có gì rõ ràng: min(x, y, z)
    - Khi hàm là một hàm chung không bị giới hạn: print(x)
    - Khi cú pháp hàm là một phần của ký hiệu miền đã thiết lập: sin(x)

#### Tuân theo các quy ước về trường hợp

- Tên của các loại và giao thức là UpperCamelCase.
- Mọi thứ khác là lowerCamelCase.

Các từ viết tắt và chữ viết tắt thường xuất hiện dưới dạng tất cả các chữ hoa trong tiếng Anh Mỹ phải được viết tắt một cách thống nhất theo quy ước về chữ hoa và chữ thường:

```swift
var utf8Bytes: [UTF8.CodeUnit]
var isRepresentableAsASCII = true
var userSMTPServer: SecureSMTPServer
```

Các từ viết tắt khác nên được coi như những từ thông thường:

```swift
var radarDetector: RadarScanner
var enjoysScubaDiving = true
```

#### Các phương thức có thể dùng chung một tên cơ sở

- Khi chúng có cùng ý nghĩa cơ bản hoặc khi chúng hoạt động trong các miền riêng biệt.

Ví dụ: khuyến khích những điều sau đây, vì các phương pháp này về cơ bản thực hiện những điều giống nhau:

##### ✅ Ưu tiên:

```swift
extension Shape {
  /// Returns `true` iff `other` is within the area of `self`.
  func contains(_ other: Point) -> Bool { ... }

  /// Returns `true` iff `other` is entirely within the area of `self`.
  func contains(_ other: Shape) -> Bool { ... }

  /// Returns `true` iff `other` is within the area of `self`.
  func contains(_ other: LineSegment) -> Bool { ... }
}
```

Và vì các kiểu **shape** và **collection** là các miền riêng biệt, điều này cũng tốt trong cùng một chương trình:

##### ✅ Ưu tiên:

```swift
extension Collection where Element : Equatable {
  /// Returns `true` iff `self` contains an element equal to
  /// `sought`.
  func contains(_ sought: Element) -> Bool { ... }
}
```

Tuy nhiên, các **index** phương thức này có ngữ nghĩa khác nhau và lẽ ra phải được đặt tên khác:

##### ⛔️ Không được ưa thích:

```swift
extension Database {
  /// Rebuilds the database's search index
  func index() { ... }

  /// Returns the `n`th row in the given table.
  func index(_ n: Int, inTable: TableID) -> TableRow { ... }
}
```

Cuối cùng, hãy tránh “quá tải trên kiểu trả về” vì nó gây ra sự mơ hồ khi có kiểu suy luận.

##### ⛔️ Không được ưa thích:

```swift
extension Box {
  /// Returns the `Int` stored in `self`, if any, and
  /// `nil` otherwise.
  func value() -> Int? { ... }

  /// Returns the `String` stored in `self`, if any, and
  /// `nil` otherwise.
  func value() -> String? { ... }
}
```

### g. Tham số

```swift
func move(from start: Point, to end: Point)
```

#### Chọn tên tham số để cung cấp tài liệu

- Mặc dù tên tham số không xuất hiện tại điểm sử dụng của hàm hoặc phương thức, nhưng chúng đóng một vai trò giải thích quan trọng.

Chọn những tên này để dễ đọc tài liệu. Ví dụ: những tên này làm cho tài liệu được đọc một cách tự nhiên:

##### ✅ Ưu tiên:

```swift
/// Return an `Array` containing the elements of `self`
/// that satisfy `predicate`.
func filter(_ predicate: (Element) -> Bool) -> [Generator.Element]

/// Replace the given `subRange` of elements with `newElements`.
mutating func replaceRange(_ subRange: Range, with newElements: [E])
```

Tuy nhiên, những điều này làm cho tài liệu trở nên khó hiểu và không có ngữ điệu:

##### ⛔️ Không được ưa thích:

```swift
/// Return an `Array` containing the elements of `self`
/// that satisfy `includedInResult`.
func filter(_ includedInResult: (Element) -> Bool) -> [Generator.Element]

/// Replace the range of elements indicated by `r` with
/// the contents of `with`.
mutating func replaceRange(_ r: Range, with: [E])
```

#### Tận dụng các tham số mặc định khi nó đơn giản hóa các mục đích sử dụng thông thường

- Bất kỳ tham số nào có một giá trị thường được sử dụng đều là ứng cử viên cho giá trị mặc định.

Các đối số mặc định cải thiện khả năng đọc bằng cách ẩn thông tin không liên quan. Ví dụ:

##### ⛔️ Không được ưa thích:

```swift
let order = lastName.compare(
  royalFamilyName, options: [], range: nil, locale: nil)
```

Có thể trở nên đơn giản hơn nhiều:

##### ✅ Ưu tiên:

```swift
let order = lastName.compare(royalFamilyName)
```

Các đối số mặc định thường được ưu tiên hơn khi sử dụng các họ phương thức, vì chúng đặt ra gánh nặng nhận thức thấp hơn cho bất kỳ ai đang cố gắng hiểu API.

##### ✅ Ưu tiên:

```swift
extension String {
  /// ...description...
  public func compare(
     _ other: String, options: CompareOptions = [],
     range: Range? = nil, locale: Locale? = nil
  ) -> Ordering
}
```

Những điều trên có thể không đơn giản, nhưng nó đơn giản hơn nhiều so với:

##### ⛔️ Không được ưa thích:

```swift
extension String {
  /// ...description 1...
  public func compare(_ other: String) -> Ordering
  /// ...description 2...
  public func compare(_ other: String, options: CompareOptions) -> Ordering
  /// ...description 3...
  public func compare(
     _ other: String, options: CompareOptions, range: Range) -> Ordering
  /// ...description 4...
  public func compare(
     _ other: String, options: StringCompareOptions,
     range: Range, locale: Locale) -> Ordering
}
```

#### Ưu tiên định vị các tham số với giá trị mặc định ở cuối danh sách tham số

- Các tham số không có giá trị mặc định thường thiết yếu hơn đối với ngữ nghĩa của một phương thức và cung cấp một mô hình sử dụng ban đầu ổn định khi các phương thức được gọi.

### h. Nhãn đối số

```swift
func move(from start: Point, to end: Point)

x.move(from: x, to: y)
```

#### Bỏ qua tất cả các nhãn khi các đối số không thể được phân biệt hữu ích

```swift
min(number1, number2)
zip(sequence1, sequence2)
```

#### Trong các trình khởi tạo thực hiện chuyển đổi kiểu bảo toàn giá trị, hãy bỏ qua nhãn đối số đầu tiên

```swift
Int64(someUInt32)
```

Đối số đầu tiên phải luôn là nguồn chuyển đổi.

```swift
extension String {
  // Convert `x` into its textual representation in the given radix
  init(_ x: BigInt, radix: Int = 10) // ← Note the initial underscore
}

text = "The value is: "
text += String(veryLargeNumber)
text += " and in hexadecimal, it's"
text += String(veryLargeNumber, radix: 16)
```

Tuy nhiên, trong các chuyển đổi loại "narrowing", bạn nên sử dụng nhãn mô tả việc narrowing.

```swift
extension UInt32 {
  /// Creates an instance having the specified `value`.
  init(_ value: Int16) // ← Widening, so no label
  /// Creates an instance having the lowest 32 bits of `source`.
  init(truncating source: UInt64)
  /// Creates an instance having the nearest representable
  /// approximation of `valueToApproximate`.
  init(saturating valueToApproximate: UInt64)
}
```

_**Lưu ý**_: Chuyển đổi kiểu bảo toàn giá trị là một phép đơn hình, tức là mọi sự khác biệt về giá trị của nguồn dẫn đến sự khác biệt về giá trị của kết quả. Khả năng truy xuất giá trị ban đầu không liên quan đến việc liệu một chuyển đổi có bảo toàn giá trị hay không.

#### Khi đối số đầu tiên tạo thành một phần của cụm giới từ, hãy đặt cho nó một nhãn đối số

-  Nhãn đối số thường phải bắt đầu bằng giới từ.

```swift
x.removeBoxes(havingLength: 12)
```

Một ngoại lệ phát sinh khi hai đối số đầu tiên đại diện cho các phần của một phần trừu tượng.

##### ⛔️ Không được ưa thích:

```swift
a.move(toX: b, y: c)
a.fade(fromRed: b, green: c, blue: d)
```

Trong những trường hợp như vậy, hãy bắt đầu nhãn đối số **sau** giới từ để giữ cho phần trừu tượng rõ ràng.

##### ✅ Ưu tiên:

```swift
a.moveTo(x: b, y: c)
a.fadeFrom(red: b, green: c, blue: d)
```

#### Ngược lại, nếu đối số đầu tiên tạo thành một phần của cụm từ ngữ pháp, hãy bỏ qua nhãn của nó

- Nối bất kỳ từ nào đứng trước vào tên cơ sở.

```swift
x.addSubview(y)
```

Hướng dẫn này ngụ ý rằng nếu đối số đầu tiên không tạo thành một phần của cụm từ ngữ pháp, thì đối số này phải có nhãn.

##### ✅ Ưu tiên:

```swift
view.dismiss(animated: false)
let text = words.split(maxSplits: 12)
let studentsByName = students.sorted(isOrderedBefore: Student.namePrecedes)
```

Lưu ý rằng điều quan trọng là cụm từ phải truyền đạt ý nghĩa chính xác. Những điều sau đây sẽ đúng ngữ pháp nhưng sẽ diễn đạt điều sai:

##### ⛔️ Không được ưa thích:

```swift
view.dismiss(false) // Don't dismiss? Dismiss a Bool?
words.split(12) // Split the number 12?
```

Cũng lưu ý rằng các đối số có giá trị mặc định có thể bị bỏ qua và trong trường hợp đó, đối số không tạo thành một phần của cụm từ ngữ pháp, vì vậy chúng phải luôn có nhãn.

#### Gắn nhãn tất cả các đối số khác

### i. Hướng dẫn đặc biệt

### k. Prose

### l. Tiền tố lớp

### m. Delegates

### n. Sử dụng loại Inferred Context

### o. Generics

### p. Ngôn ngữ

## 4 - Tổ chức mã

### a. Tuân thủ giao thức

### b. Mã không sử dụng

### c. Minimal Imports

## 5 - Khoảng cách

## 6 - Bình luận

### a. Sử dụng phương ngữ Markdown

### b. Bắt đầu bằng một bản tóm tắt

### c. Theo tuỳ chọn

## 7 - Classes and Structures

### a. Sử dụng cái nào?

### b. Định nghĩa mẫu

### c. Sử dụng Self

### d. Thuộc tính chỉ đọc

### e. Final

## 8 - Khai báo hàm

## 9 - Lệnh gọi hàm

## 10 - Biểu thức Closure

## 11 - Types

### a. Constants

### b. Phương thức tĩnh và thuộc tính kiểu biến

### c. Optionals

### d. Khởi tạo Lazy

### e. Kiểu suy luận

### f. Syntactic Sugar

## 12 - Functions vs Methods

## 13 - Quản lý bộ nhớ

### a. Kéo dài thời gian tồn tại của đối tượng

## 14 - Kiểm soát truy cập

## 15 - Luồng điều khiển

### a. Toán tử bậc ba

## 16 - Con đường vàng

### a. Failing Guards

## 17 - Dấu chấm phẩy

## 18 - Dấu ngoặc đơn

## 19 - Chữ viết chuỗi nhiều dòng

## 20 - Không có biểu tượng cảm xúc

## 21 - Không #imageLiteral hoặc #colorLiteral
