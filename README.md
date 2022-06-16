# Hướng dẫn phong cách Swift (Swift Style Guide)

- Mục tiêu bao trùm của chúng ta là rõ ràng, nhất quán và ngắn gọn, theo thứ tự, hợp lý hoá luồng nội dung.
- Đảm bảo rằng loại bỏ nhiều gánh nặng cho người đọc.

## Mục lục

* [1 - Tính đúng đắn](#1---tính-đúng-đắn)
* [2 - Sử dụng SwiftLint](#2---sử-dụng-swiftlint)
    * [a. Cài đặt](#a-cài-đặt)
    * [b. Tham chiếu quy tắc](#b-tham-chiếu-quy-tắc)
* [3 - Quy tắc đặt tên](#3---quy-tắc-đặt-tên)
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
    * [n. Sử dụng loại ngữ cảnh suy luận](#n-sử-dụng-loại-ngữ-cảnh-suy-luận)
    * [o. Generics](#o-generics)
    * [p. Ngôn ngữ](#p-ngôn-ngữ)
* [4 - Tổ chức mã](#4---tổ-chức-mã)
    * [a. Tuân thủ giao thức](#a-tuân-thủ-giao-thức)
    * [b. Mã không sử dụng](#b-mã-không-sử-dụng)
    * [c. Minimal Imports](#c-minimal-imports)
* [5 - Khoảng cách](#5---khoảng-cách)
* [6 - Bình luận](#6---bình-luận)
    * [a. Sử dụng phương ngữ Markdown](#a-sử-dụng-phương-ngữ-markdown)
    * [b. Bắt đầu bằng một bản tóm tắt](#b-bắt-đầu-bằng-một-bản-tóm-tắt)
    * [c. Theo tuỳ chọn](#c-theo-tuỳ-chọn)
* [7 - Classes and Structures](#7---classes-and-structures)
* [8 - Khai báo hàm](#8---khai-báo-hàm)
* [9 - Lệnh gọi hàm](#9---lệnh-gọi-hàm)
* [10 - Biểu thức Closure](#10---biểu-thức-closure)
* [11 - Types](#11---types)
    * [a. Constants](#a-constants)
    * [b. Phương thức tĩnh và thuộc tính kiểu biến](#b-phương-thức-tĩnh-và-thuộc-tính-kiểu-biến)
    * [c. Optionals](#c-optionals)
    * [d. Khởi tạo Lazy](#d-khởi-tạo-lazy)
    * [e. Kiểu suy luận](#e-kiểu-suy-luận)
    * [f. Cú pháp](#f-cú-pháp)
* [12 - Functions vs Methods](#12---functions-vs-methods)
* [13 - Quản lý bộ nhớ](#13---quản-lý-bộ-nhớ)
    * [a. Kéo dài thời gian tồn tại của đối tượng](#a-kéo-dài-thời-gian-tồn-tại-của-đối-tượng)
* [14 - Kiểm soát truy cập](#14---kiểm-soát-truy-cập)
* [15 - Luồng điều khiển](#15---luồng-điều-khiển)
    * [a. Toán tử bậc ba](#a-toán-tử-bậc-ba)
* [16 - Con đường vàng](#16---con-đường-vàng)
* [17 - Dấu chấm phẩy](#17---dấu-chấm-phẩy)
* [18 - Dấu ngoặc đơn](#18---dấu-ngoặc-đơn)
* [19 - Chữ viết chuỗi nhiều dòng](#19---chữ-viết-chuỗi-nhiều-dòng)
* [20 - Không có biểu tượng cảm xúc](#20---không-có-biểu-tượng-cảm-xúc)
* [21 - Không #imageLiteral hoặc #colorLiteral](#21---không-imageliteral-hoặc-colorliteral)

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

- Đặt tên cho các cặp phương thức đột biến / không thay đổi một cách nhất quán. Một phương thức thay đổi thường sẽ có một biến thể không thay đổi với ngữ nghĩa tương tự, nhưng nó trả về một giá trị mới thay vì cập nhật một thể hiện tại chỗ.

##### Khi thao tác được mô tả một cách tự nhiên bởi một động từ

Hãy sử dụng mệnh lệnh của động từ đó cho phương thức biến âm và áp dụng hậu tố “ed” hoặc “ing” để đặt tên cho đối từ không biến âm của nó.

| Đột biến    | Nonmutating         |
|-------------|---------------------|
| x.sort()    | z = x.sorted()      |
| x.append(y) | z = x.appending(y)  |

_Ưu tiên đặt tên cho biến thể không bổ ngữ bằng cách sử dụng phân từ quá khứ của động từ (thường thêm “ed”)._

```swift
/// Reverses `self` in-place.
mutating func reverse()

/// Returns a reversed copy of `self`.
func reversed() -> Self
...
x.reverse()
let y = x.reversed()
```

_Khi động từ có tân ngữ trực tiếp, thêm “ed” là không đúng ngữ pháp, hãy đặt tên cho biến thể không bổ ngữ bằng cách sử dụng phân từ hiện tại của động từ, bằng cách thêm “ing”._

```swift
/// Strips all the newlines from `self`
mutating func stripNewlines()

/// Returns a copy of `self` with all the newlines stripped.
func strippingNewlines() -> String
...
s.stripNewlines()
let oneLine = t.strippingNewlines()
```

##### Khi thao tác được mô tả một cách tự nhiên bởi một danh từ

Hãy sử dụng danh từ cho phương thức không thay đổi và áp dụng tiền tố “form” để đặt tên cho phương thức biến đổi của nó.

| Nonmutating         | Đột biến            |
|---------------------|---------------------|
| x = y.union(z)      | y.formUnion(z)      |
| j = c.successor(i)  | c.formSuccessor(&i) |

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
    - Tốt hơn là đặt tên `Array` cho một cấu trúc dữ liệu liền kề hơn là sử dụng một thuật ngữ đơn giản hóa, chẳng hạn như `List`, mặc dù người mới bắt đầu có thể hiểu ý nghĩa của `List` dễ dàng hơn. `Array` là yếu tố cơ bản trong máy tính hiện đại, vì vậy mọi lập trình viên đều biết — hoặc sẽ sớm biết — array là gì. Sử dụng một thuật ngữ mà hầu hết các lập trình viên đều quen thuộc và các tìm kiếm và câu hỏi trên web của họ sẽ được thưởng.
    - Trong một lĩnh vực lập trình cụ thể, chẳng hạn như toán học, một thuật ngữ chưa từng được biết đến rộng rãi như `sin(x)` được ưu tiên hơn một cụm từ giải thích chẳng hạn như `verticalPositionOnUnitCircleAtOriginOfEndOfRadiusWithAngle(x)`. Lưu ý rằng trong trường hợp này, tiền lệ vượt trội hơn hướng dẫn tránh viết tắt: mặc dù từ đầy đủ là sine, “sin(x)” đã được sử dụng phổ biến trong các lập trình viên trong nhiều thập kỷ và các nhà toán học trong nhiều thế kỷ.

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

#### Gắn nhãn các thành viên tuple và các tham số đóng tên

- Những tên này có sức mạnh giải thích, có thể được tham chiếu từ các nhận xét tài liệu và cung cấp quyền truy cập rõ ràng cho các thành viên tuple.

```swift
/// Ensure that we hold uniquely-referenced storage for at least
/// `requestedCapacity` elements.
///
/// If more storage is needed, `allocate` is called with
/// `byteCount` equal to the number of maximally-aligned
/// bytes to allocate.
///
/// - Returns:
///   - reallocated: `true` iff a new block of memory
///     was allocated.
///   - capacityChanged: `true` iff `capacity` was updated.
mutating func ensureUniqueStorage(
  minimumCapacity requestedCapacity: Int, 
  allocate: (_ byteCount: Int) -> UnsafePointer<Void>
) -> (reallocated: Bool, capacityChanged: Bool)
```

Tên được sử dụng cho các tham số đóng nên được chọn giống như tên tham số cho các hàm cấp cao nhất. Nhãn cho các đối số closure xuất hiện tại điểm gọi không được hỗ trợ.

#### Hãy cẩn thận hơn với tính đa hình không bị giới hạn để tránh sự mơ hồ trong các overload sets.

Ví dụ: Any và AnyObject các tham số chung không bị giới hạn

##### ⛔️ Không được ưa thích:

```swift
struct Array {
  /// Inserts `newElement` at `self.endIndex`.
  public mutating func append(_ newElement: Element)

  /// Inserts the contents of `newElements`, in order, at
  /// `self.endIndex`.
  public mutating func append(_ newElements: S)
    where S.Generator.Element == Element
}
```

Các phương thức này tạo thành một tập ngữ nghĩa và các kiểu đối số thoạt đầu có vẻ khác biệt rõ ràng. Tuy nhiên, khi Element là Any, một phần tử có thể có cùng kiểu với một dãy các phần tử.

##### ⛔️ Không được ưa thích:

```swift
var values: [Any] = [1, "a"]
values.append([2, 3, 4]) // [1, "a", [2, 3, 4]] or [1, "a", 2, 3, 4]?
```

Để loại bỏ sự mơ hồ, hãy đặt tên cho overload thứ hai rõ ràng hơn.

##### ✅ Ưu tiên:

```swift
struct Array {
  /// Inserts `newElement` at `self.endIndex`.
  public mutating func append(_ newElement: Element)

  /// Inserts the contents of `newElements`, in order, at
  /// `self.endIndex`.
  public mutating func append(contentsOf newElements: S)
    where S.Generator.Element == Element
}
```

### k. Prose

- Khi đề cập đến các phương pháp trong prose, rõ ràng là rất quan trọng. Để tham chiếu đến tên phương thức, hãy sử dụng biểu mẫu đơn giản nhất có thể.
  - Viết tên phương thức không có tham số. Ví dụ: Tiếp theo, bạn cần gọi `addTarget`.
  - Viết tên phương thức với các nhãn đối số. Ví dụ: Tiếp theo, bạn cần gọi `addTarget(_:action:)`.
  - Viết tên đầy đủ của phương thức với các nhãn và kiểu đối số. Ví dụ: Tiếp theo, bạn cần gọi `addTarget(_: Any?, action: Selector?)`.

### l. Tiền tố lớp

- Các kiểu Swift được mô-đun chứa chúng tự động đặt tên cho các kiểu và bạn không nên thêm tiền tố lớp chẳng hạn như RW. Nếu hai tên từ các mô-đun khác nhau xung đột, bạn có thể phân biệt bằng cách thêm tên loại vào trước tên mô-đun. Tuy nhiên, chỉ xác định tên mô-đun khi có thể xảy ra nhầm lẫn, điều này hiếm khi xảy ra.

```swift
import SomeModule

let myClass = MyModule.UsefulClass()
```

### m. Delegates

- Khi tạo các phương thức đại biểu tùy chỉnh, tham số đầu tiên không được đặt tên phải là nguồn đại biểu. (UIKit chứa nhiều ví dụ về điều này.)

##### ✅ Ưu tiên:

```swift
func namePickerView(_ namePickerView: NamePickerView, didSelectName name: String)
func namePickerViewShouldReload(_ namePickerView: NamePickerView) -> Bool
```

##### ⛔️ Không được ưa thích:

```swift
func didSelectName(namePicker: NamePickerViewController, name: String)
func namePickerShouldReload() -> Bool
```

### n. Sử dụng loại ngữ cảnh suy luận

- Sử dụng ngữ cảnh suy luận của trình biên dịch để viết mã ngắn hơn, rõ ràng.

##### ✅ Ưu tiên:

```swift
let selector = #selector(viewDidLoad)
view.backgroundColor = .red
let toView = context.view(forKey: .to)
let view = UIView(frame: .zero)
```

##### ⛔️ Không được ưa thích:

```swift
let selector = #selector(ViewController.viewDidLoad)
view.backgroundColor = UIColor.red
let toView = context.view(forKey: UITransitionContextViewKey.to)
let view = UIView(frame: CGRect.zero)
```

### o. Generics

- Các thông số loại chung phải là tên mô tả, upper camel case. Khi tên loại không có mối quan hệ hoặc vai trò có ý nghĩa, hãy sử dụng một chữ cái in hoa truyền thống như `T`, `U` hoặc `V`.

##### ✅ Ưu tiên:

```swift
struct Stack<Element> { ... }
func write<Target: OutputStream>(to target: inout Target)
func swap<T>(_ a: inout T, _ b: inout T)
```

##### ⛔️ Không được ưa thích:

```swift
struct Stack<T> { ... }
func write<target: OutputStream>(to target: inout target)
func swap<Thing>(_ a: inout Thing, _ b: inout Thing)
```

### p. Ngôn ngữ

- Sử dụng chính tả tiếng Anh Mỹ để khớp với API của Apple.

##### ✅ Ưu tiên:

```swift
let color = "red"
```

##### ⛔️ Không được ưa thích:

```swift
let colour = "red"
```

## 4 - Tổ chức mã

- Sử dụng các phần mở rộng để tổ chức mã của bạn thành các khối chức năng hợp lý. Mỗi tiện ích mở rộng nên được thiết lập bằng một `// MARK: -` nhận xét để giữ mọi thứ được sắp xếp tốt.

### a. Tuân thủ giao thức

- Đặc biệt, khi thêm sự tuân thủ giao thức vào một mô hình, hãy ưu tiên thêm một phần mở rộng riêng cho các phương thức giao thức. Điều này giữ cho các phương thức liên quan được nhóm cùng với giao thức và có thể đơn giản hóa các hướng dẫn để thêm giao thức vào một lớp với các phương thức liên quan của nó.

##### ✅ Ưu tiên:

```swift
class MyViewController: UIViewController {
  // class stuff here
}

// MARK: - UITableViewDataSource
extension MyViewController: UITableViewDataSource {
  // table view data source methods
}

// MARK: - UIScrollViewDelegate
extension MyViewController: UIScrollViewDelegate {
  // scroll view delegate methods
}
```

##### ⛔️ Không được ưa thích:

```swift
class MyViewController: UIViewController, UITableViewDataSource, UIScrollViewDelegate {
  // all methods
}
```

- Vì trình biên dịch không cho phép bạn khai báo lại sự tuân thủ giao thức trong một lớp dẫn xuất, nên không phải lúc nào cũng cần phải sao chép các nhóm mở rộng của lớp cơ sở. Điều này đặc biệt đúng nếu lớp dẫn xuất là một lớp đầu cuối và một số lượng nhỏ các phương thức đang bị ghi đè. Khi nào thì bảo tồn các nhóm mở rộng là tùy theo quyết định của bạn.
- Đối với bộ điều khiển chế độ xem UIKit, hãy xem xét nhóm lifecycle, custom accessors và IBAction trong các phần mở rộng lớp riêng biệt.

### b. Mã không sử dụng

- Mã không được sử dụng (đã chết), bao gồm mã mẫu Xcode và nhận xét của trình giữ chỗ nên được xóa.
- Một ngoại lệ là khi hướng dẫn hoặc sách của bạn hướng dẫn người dùng sử dụng mã đã nhận xét.
- Các phương thức nguyện vọng không được liên kết trực tiếp với hướng dẫn mà việc triển khai chỉ đơn giản là gọi lớp cha cũng nên bị loại bỏ. Điều này bao gồm mọi phương thức UIApplicationDelegate trống / không sử dụng.

##### ✅ Ưu tiên:

```swift
override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
  return Database.contacts.count
}
```

##### ⛔️ Không được ưa thích:

```swift
override func didReceiveMemoryWarning() {
  super.didReceiveMemoryWarning()
  // Dispose of any resources that can be recreated.
}

override func numberOfSections(in tableView: UITableView) -> Int {
  // #warning Incomplete implementation, return the number of sections
  return 1
}

override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
  // #warning Incomplete implementation, return the number of rows
  return Database.contacts.count
}
```

### c. Minimal Imports

- Chỉ import các mô-đun mà tệp nguồn yêu cầu.

##### ✅ Ưu tiên:

```swift
import UIKit
var view: UIView
var deviceModels: [String]
```

##### ✅ Ưu tiên:

```swift
import Foundation
var deviceModels: [String]
```

##### ⛔️ Không được ưa thích:

```swift
import UIKit
import Foundation
var view: UIView
var deviceModels: [String]
```

##### ⛔️ Không được ưa thích:

```swift
import UIKit
var deviceModels: [String]
```

## 5 - Khoảng cách

- Thụt lề bằng cách sử dụng 2 dấu cách thay vì tab để tiết kiệm không gian và giúp ngăn chặn dòng. Đảm bảo đặt tùy chọn này trong Xcode và trong cài đặt Dự án.
- Các dấu ngoặc nhọn và các dấu ngoặc nhọn khác ( `if` / `else` / `switch` / `while`...) luôn mở trên cùng một dòng với câu lệnh nhưng đóng trên một dòng mới.

##### ✅ Ưu tiên:

```swift
if user.isHappy {
  // Do something
} else {
  // Do something else
}
```

##### ⛔️ Không được ưa thích:

```swift
if user.isHappy
{
  // Do something
}
else {
  // Do something else
}
```

- Nên có một dòng trống giữa các phương thức và tối đa một dòng trống giữa các khai báo kiểu để hỗ trợ việc tổ chức và rõ ràng trực quan. Khoảng trắng bên trong các phương thức sẽ phân tách chức năng, nhưng có quá nhiều phần trong một phương thức thường có nghĩa là bạn nên cấu trúc lại thành một số phương thức.
- Không được có dòng trống sau dấu ngoặc mở hoặc trước dấu ngoặc nhọn.
- Dấu ngoặc đơn không được xuất hiện trên một dòng.

##### ✅ Ưu tiên:

```swift
let user = try await getUser(
  for: userID,
  on: connection)
```

##### ⛔️ Không được ưa thích:

```swift
let user = try await getUser(
  for: userID,
  on: connection
)
```

- Dấu hai chấm luôn không có khoảng trắng ở bên trái và một khoảng trắng ở bên phải. Các ngoại lệ là toán tử bậc ba `? :`, từ điển trống `[:]` và `#selector` cú pháp `addTarget(_:action:)`.

##### ✅ Ưu tiên:

```swift
class TestDatabase: Database {
  var data: [String: CGFloat] = ["A": 1.2, "B": 3.2]
}
```

##### ⛔️ Không được ưa thích:

```swift
class TestDatabase : Database {
  var data :[String:CGFloat] = ["A" : 1.2, "B":3.2]
}
```

- Các dòng dài nên được bao quanh khoảng 70 ký tự. Một giới hạn cứng được cố ý không chỉ định. Không được quá 120 ký tự trên mỗi dòng.
- Tránh các khoảng trắng ở cuối dòng.
- Thêm một ký tự dòng mới vào cuối mỗi tệp.

## 6 - Bình luận

- Viết bình luận tài liệu cho mọi khai báo. Những hiểu biết sâu sắc có được bằng cách viết tài liệu có thể có tác động sâu sắc đến thiết kế của bạn, vì vậy đừng bỏ qua nó.
- Khi chúng cần thiết, hãy sử dụng các nhận xét để giải thích tại sao một đoạn mã cụ thể lại làm được điều gì đó. Nhận xét phải được cập nhật hoặc xóa.
- Tránh chặn các nhận xét cùng dòng với mã, vì mã phải tự tài liệu hóa càng tốt. Ngoại lệ: Điều này không áp dụng cho những nhận xét được sử dụng để tạo tài liệu.
- Tránh sử dụng các chú thích kiểu C `/* ... */`. Ưu tiên sử dụng dấu gạch chéo kép `//` hoặc dấu gạch chéo ba `///`.
- _**Lưu ý**_: Nếu bạn gặp sự cố khi mô tả chức năng API của mình bằng các thuật ngữ đơn giản, có thể bạn đã thiết kế sai.

### a. [Sử dụng phương ngữ Markdown](https://developer.apple.com/library/archive/documentation/Xcode/Reference/xcode_markup_formatting_ref)

### b. Bắt đầu bằng một bản tóm tắt

- Mô tả thực thể đang được khai báo. Thông thường, một API có thể được hiểu hoàn toàn từ phần khai báo và phần tóm tắt của nó.

```swift
/// Returns a "view" of `self` containing the same elements in
/// reverse order.
func reversed() -> ReverseCollection
```

#### Tập trung vào phần tóm tắt

- Đó là phần quan trọng nhất. Nhiều nhận xét về tài liệu xuất sắc chỉ bao gồm một bản tóm tắt tuyệt vời.

#### Sử dụng một đoạn câu đơn

- Nếu có thể, kết thúc bằng dấu chấm. Không sử dụng một câu hoàn chỉnh.

#### Mô tả những gì một hàm hoặc phương thức thực hiện và những gì nó trả về

- Bỏ qua các hiệu ứng `nil` và `Void` trả về:

```swift
/// Inserts `newHead` at the beginning of `self`.
mutating func prepend(_ newHead: Int)

/// Returns a `List` containing `head` followed by the elements
/// of `self`.
func prepending(_ head: Element) -> List

/// Removes and returns the first element of `self` if non-empty;
/// returns `nil` otherwise.
mutating func popFirst() -> Element?
```

- _**Lưu ý**_: Trong một số trường hợp hiếm hoi như **popFirst** trên, phần tóm tắt được tạo thành từ nhiều đoạn câu được phân tách bằng dấu chấm phẩy.

#### Mô tả những gì một chỉ số phụ truy cập

```swift
/// Accesses the `index`th element.
subscript(index: Int) -> Element { get set }
```

#### Mô tả những gì một trình khởi tạo tạo ra

```swift
/// Creates an instance containing `n` repetitions of `x`.
init(count n: Int, repeatedElement x: Element)
```

#### Mô tả thực thể được khai báo

```swift
/// A collection that supports equally efficient insertion/removal
/// at any position.
struct List {

  /// The element at the beginning of `self`, or `nil` if self is
  /// empty.
  var first: Element?
  ...
```

### c. Theo tuỳ chọn

-  Dùng một hoặc nhiều đoạn văn và mục đầu dòng. Các đoạn văn được phân tách bằng các dòng trống và sử dụng các câu hoàn chỉnh.

```swift
/// Writes the textual representation of each    ← Summary
/// element of `items` to the standard output.
///                                              ← Blank line
/// The textual representation for each item `x` ← Additional discussion
/// is generated by the expression `String(x)`.
///
/// - Parameter separator: text to be printed    ⎫
///   between items.                             ⎟
/// - Parameter terminator: text to be printed   ⎬ Parameters section
///   at the end.                                ⎟
///                                              ⎭
/// - Note: To print without a trailing          ⎫
///   newline, pass `terminator: ""`             ⎟
///                                              ⎬ Symbol commands
/// - SeeAlso: `CustomDebugStringConvertible`,   ⎟
///   `CustomStringConvertible`, `debugPrint`.   ⎭
public func print(
  _ items: Any..., separator: String = " ", terminator: String = "\n")
```

- Biết và sử dụng các mục dấu đầu dòng được công nhận với cú pháp lệnh ký hiệu.

| Attention  |  Author        | Authors       |	Bug         |
|------------|----------------|---------------|-------------|
| Complexity |  Copyright     | Date          |	Experiment  |
| Important  |  Invariant     | Note          |	Parameter   |
| Parameters |  Postcondition | Precondition  |	Remark      |
| Requires   |  Returns       | SeeAlso       |	Since       |
| Throws     |  ToDo          | Version       |	Warning     |

## 7 - Classes and Structures

### a. Sử dụng cái nào?

- Hãy nhớ rằng, cấu trúc có **ngữ nghĩa giá trị**. Sử dụng cấu trúc cho những thứ không có danh tính. Một mảng chứa `[a, b, c]` thực sự giống với một mảng khác chứa `[a, b, c]` và chúng hoàn toàn có thể hoán đổi cho nhau. Không quan trọng bạn sử dụng mảng đầu tiên hay mảng thứ hai, vì chúng đại diện cho cùng một thứ. Đó là lý do tại sao mảng là cấu trúc.
- Các lớp có **ngữ nghĩa tham chiếu**. Sử dụng các lớp cho những thứ có danh tính hoặc một vòng đời cụ thể. Bạn sẽ lập mô hình một người như một lớp vì hai đối tượng người là hai thứ khác nhau. Chỉ vì hai người có cùng tên và ngày sinh, không có nghĩa là họ là cùng một người. Nhưng ngày sinh của người đó sẽ là một cấu trúc vì ngày 3 tháng 3 năm 1950 giống với bất kỳ đối tượng ngày nào khác cho ngày 3 tháng 3 năm 1950. Bản thân ngày đó không có danh tính.

### b. Định nghĩa mẫu

- Dưới đây là một ví dụ về định nghĩa lớp được tạo kiểu tốt:

```swift
class Circle: Shape {
  var x: Int, y: Int
  var radius: Double
  var diameter: Double {
    get {
      return radius * 2
    }
    set {
      radius = newValue / 2
    }
  }

  init(x: Int, y: Int, radius: Double) {
    self.x = x
    self.y = y
    self.radius = radius
  }

  convenience init(x: Int, y: Int, diameter: Double) {
    self.init(x: x, y: y, radius: diameter / 2)
  }

  override func area() -> Double {
    return Double.pi * radius * radius
  }
}

extension Circle: CustomStringConvertible {
  var description: String {
    return "center = \(centerString) area = \(area())"
  }
  private var centerString: String {
    return "(\(x),\(y))"
  }
}
```

Ví dụ trên minh họa các nguyên tắc kiểu sau:

- Chỉ định kiểu cho các thuộc tính, biến, hằng số, khai báo đối số và các câu lệnh khác có dấu cách sau dấu hai chấm nhưng không có trước dấu hai chấm. Ví dụ x: Int, và Circle: Shape.
- Xác định nhiều biến và cấu trúc trên một dòng nếu chúng có chung mục đích / ngữ cảnh.
- Thụt lề các định nghĩa getter và setter và các trình quan sát thuộc tính.
- Không thêm các công cụ sửa đổi, chẳng hạn như `internal` khi chúng đã là mặc định. Tương tự, không lặp lại công cụ sửa đổi truy cập khi ghi đè một phương thức.
- Ẩn các chi tiết triển khai, không được chia sẻ, chẳng hạn như `centerString` bên trong tiện ích mở rộng bằng cách sử dụng `private` kiểm soát truy cập.

### c. Sử dụng Self

- Để ngắn gọn, hãy tránh sử dụng `self` vì Swift không yêu cầu nó truy cập thuộc tính của một đối tượng hoặc gọi các phương thức của nó.
- Chỉ sử dụng `self` khi trình biên dịch yêu cầu (trong các @escaping closure hoặc trong các trình khởi tạo để phân biệt các thuộc tính khỏi các đối số). Nói cách khác, nếu nó biên dịch mà không có `self` thì hãy bỏ qua nó.

### d. Thuộc tính chỉ đọc

- Để ngắn gọn, nếu một thuộc tính được tính là chỉ đọc, hãy bỏ qua mệnh đề get. Mệnh đề get chỉ được yêu cầu khi một mệnh đề đã đặt được cung cấp.

##### ✅ Ưu tiên:

```swift
var diameter: Double {
  return radius * 2
}
```

##### ⛔️ Không được ưa thích:

```swift
var diameter: Double {
  get {
    return radius * 2
  }
}
```

### e. Final

- Việc sử dụng `final` đôi khi có thể làm rõ ý định của bạn và đáng giá.

Trong ví dụ dưới đây, `Box` có một mục đích cụ thể và tùy chỉnh trong một lớp dẫn xuất không có mục đích. Đánh dấu nó `final` làm cho điều đó rõ ràng.

```swift
// Turn any generic type into a reference type using this Box class.
final class Box<T> {
  let value: T
  init(_ value: T) {
    self.value = value
  }
}
```

## 8 - Khai báo hàm

- Giữ các khai báo hàm ngắn trên một dòng bao gồm cả dấu ngoặc nhọn mở:

```swift
func reticulateSplines(spline: [Double]) -> Bool {
  // reticulate code goes here
}
```

- Đối với các hàm có chữ ký dài, hãy đặt mỗi tham số trên một dòng mới và thêm một thụt lề phụ trên các dòng tiếp theo:

```swift
func reticulateSplines(
  spline: [Double], 
  adjustmentFactor: Double,
  translateConstant: Int, 
  comment: String
) -> Bool {
  // reticulate code goes here
}
```

- Không sử dụng `(Void)` để thể hiện việc thiếu đầu vào; đơn giản là sử dụng `()`. Ngược lại, sử dụng `Void` thay vì `()` cho kết quả closure và hàm.

##### ✅ Ưu tiên:

```swift
func updateConstraints() -> Void {
  // magic happens here
}

typealias CompletionHandler = (result) -> Void
```

##### ⛔️ Không được ưa thích:

```swift
func updateConstraints() -> () {
  // magic happens here
}

typealias CompletionHandler = (result) -> ()
```

## 9 - Lệnh gọi hàm

- Phản ánh kiểu khai báo hàm tại các điểm gọi. Các cuộc gọi phù hợp trên một dòng phải được viết như vậy:

```swift
let success = reticulateSplines(splines)
```

- Nếu điểm gọi phải được bao bọc, hãy đặt mỗi tham số trên một dòng mới, thụt lề một cấp bổ sung:

```swift
let success = reticulateSplines(
  spline: splines,
  adjustmentFactor: 1.3,
  translateConstant: 2,
  comment: "normalize the display")
```

## 10 - Biểu thức Closure

- Chỉ sử dụng cú pháp bao đóng theo sau nếu có một tham số biểu thức closure duy nhất ở cuối danh sách đối số. Đặt tên mô tả các tham số closure.

##### ✅ Ưu tiên:

```swift
UIView.animate(withDuration: 1.0) {
  self.myView.alpha = 0
}

UIView.animate(withDuration: 1.0, animations: {
  self.myView.alpha = 0
}, completion: { finished in
  self.myView.removeFromSuperview()
})
```

##### ⛔️ Không được ưa thích:

```swift
UIView.animate(withDuration: 1.0, animations: {
  self.myView.alpha = 0
})

UIView.animate(withDuration: 1.0, animations: {
  self.myView.alpha = 0
}) { f in
  self.myView.removeFromSuperview()
}
```

- Đối với các bao đóng biểu thức đơn trong đó ngữ cảnh rõ ràng, hãy sử dụng các trả về ngầm định:

```swift
attendeeList.sort { a, b in
  a > b
}
```

- Các phương thức chuỗi sử dụng dấu đóng phải rõ ràng và dễ đọc trong ngữ cảnh. Các quyết định về khoảng cách, ngắt dòng và khi nào sử dụng các đối số có tên so với ẩn danh là tùy ý của tác giả. Ví dụ:

```swift
let value = numbers.map { $0 * 2 }.filter { $0 % 3 == 0 }.index(of: 90)

let value = numbers
  .map {$0 * 2}
  .filter {$0 > 50}
  .map {$0 + 10}
```

## 11 - Types

- Luôn sử dụng các kiểu và biểu thức gốc của Swift khi có sẵn.

##### ✅ Ưu tiên:

```swift
let width = 120.0 // Double
let widthString = "\(width)" // String
```

##### ❗️ Ít được ưa thích:

```swift
let width = 120.0 // Double
let widthString = (width as NSNumber).stringValue // String
```

##### ⛔️ Không được ưa thích:

```swift
let width: NSNumber = 120.0 // NSNumber
let widthString: NSString = width.stringValue // NSString
```

- Trong mã vẽ, hãy sử dụng `CGFloat` nếu nó làm cho mã ngắn gọn hơn bằng cách tránh quá nhiều chuyển đổi.

### a. Constants

- Hằng số được xác định bằng cách sử dụng từ khóa `let` và các biến với từ khóa `var`. Luôn sử dụng `let` thay vì `var` nếu giá trị của biến sẽ không thay đổi.

- Mẹo: Một kỹ thuật tốt là xác định mọi thứ bằng cách sử dụng `let` và chỉ thay đổi nó thành `var` nếu trình biên dịch phàn nàn!

Bạn có thể xác định hằng số trên một enum chứ không phải trên một thể hiện của enum đó bằng cách sử dụng thuộc tính enum. Để khai báo một thuộc tính enum như một hằng số, chỉ cần sử dụng `static let`. Các thuộc tính enum được khai báo theo cách này thường được ưu tiên hơn các hằng toàn cục vì chúng dễ phân biệt hơn với các thuộc tính thể hiện. Thí dụ:

##### ✅ Ưu tiên:

```swift
enum Math {
  static let e = 2.718281828459045235360287
  static let root2 = 1.41421356237309504880168872
}

let hypotenuse = side * Math.root2
```

Lưu ý: Ưu điểm của việc sử dụng enum liệt kê không có chữ hoa chữ thường là nó không thể vô tình được khởi tạo và hoạt động như một không gian tên thuần túy.

##### ⛔️ Không được ưa thích:

```swift
let e = 2.718281828459045235360287  // pollutes global namespace
let root2 = 1.41421356237309504880168872

let hypotenuse = side * root2 // what is root2?
```

### b. Phương thức tĩnh và thuộc tính kiểu biến

- Các phương thức tĩnh và thuộc tính kiểu hoạt động tương tự như các hàm toàn cục và biến toàn cục và nên được sử dụng một cách tiết kiệm.

### c. Optionals

- Khai báo các biến và kiểu trả về của hàm là optional với `?`, giá trị `nil` được chấp nhận.
- Chỉ sử dụng các kiểu không được bao bọc hoàn toàn được khai báo `!` với các biến cá thể mà bạn biết sẽ được khởi tạo sau đó trước khi sử dụng.
- Ưu tiên ràng buộc optional hơn optional không được bao bọc trong hầu hết các trường hợp khác.

Khi truy cập một giá trị optional, hãy sử dụng chuỗi optional nếu giá trị chỉ được truy cập một lần hoặc nếu có nhiều optional trong chuỗi:

```swift
textContainer?.textLabel?.setNeedsDisplay()
```

Sử dụng ràng buộc optional khi việc mở một lần và thực hiện nhiều thao tác thuận tiện hơn:

```swift
if let textContainer = textContainer {
  // do many things with textContainer
}
```

Khi đặt tên cho các biến và thuộc tính optional, hãy tránh đặt tên chúng giống như `optionalString` hoặc `maybeView` vì optional của chúng đã có trong khai báo kiểu.

##### ✅ Ưu tiên:

```swift
var subview: UIView?
var volume: Double?

// later on...
if let subview = subview, let volume = volume {
  // do something with unwrapped subview and volume
}

// another example
resource.request().onComplete { [weak self] response in
  guard let self = self else { return }
  let model = self.updateModel(response)
  self.updateUI(model)
}
```

##### ⛔️ Không được ưa thích:

```swift
var optionalSubview: UIView?
var volume: Double?

if let unwrappedSubview = optionalSubview {
  if let realVolume = volume {
    // do something with unwrappedSubview and realVolume
  }
}

// another example
UIView.animate(withDuration: 2.0) { [weak self] in
  guard let strongSelf = self else { return }
  strongSelf.alpha = 1.0
}
```

### d. Khởi tạo Lazy

Cân nhắc sử dụng khởi tạo lazy để kiểm soát chi tiết hơn đối với thời gian tồn tại của đối tượng. Điều này đặc biệt đúng với `UIViewController` tải lượt xem một cách lazy. Bạn có thể sử dụng một closure được gọi ngay lập tức `{ }()` hoặc gọi một phương thức factory riêng tư (private).

```swift
lazy var locationManager = makeLocationManager()

private func makeLocationManager() -> CLLocationManager {
  let manager = CLLocationManager()
  manager.desiredAccuracy = kCLLocationAccuracyBest
  manager.delegate = self
  manager.requestAlwaysAuthorization()
  return manager
}

lazy var contentView: UIView = {
  let view = UIView()
  return view
}()
```

_**Ghi chú**_: `[unowned self]` không bắt buộc ở đây. Một chu kỳ lưu giữ không được tạo.

### e. Kiểu suy luận

- Ưu tiên mã nhỏ gọn và để trình biên dịch suy ra kiểu cho các hằng số hoặc biến của các trường hợp đơn lẻ.
- Kiểu suy luận cũng thích hợp cho các mảng và từ điển nhỏ, không trống.
- Khi được yêu cầu, hãy chỉ định loại cụ thể chẳng hạn như `CGFloat` hoặc `Int16`.

##### ✅ Ưu tiên:

```swift
let message = "Click the button"
let currentBounds = computeViewBounds()
var names = ["Mic", "Sam", "Christine"]
let maximumWidth: CGFloat = 106.5
```

##### ⛔️ Không được ưa thích:

```swift
let message: String = "Click the button"
let currentBounds: CGRect = computeViewBounds()
var names = [String]()
```

Đối với các mảng và từ điển trống, hãy sử dụng chú thích kiểu.

##### ✅ Ưu tiên:

```swift
var names: [String] = []
var lookup: [String: Int] = [:]
```

##### ⛔️ Không được ưa thích:

```swift
var names = [String]()
var lookup = [String: Int]()
```

_**Lưu ý**_: Làm theo hướng dẫn này có nghĩa là việc chọn tên mô tả thậm chí còn quan trọng hơn trước đây.

### f. Cú pháp

- Ưu tiên các phiên bản tắt của khai báo kiểu hơn là cú pháp chung đầy đủ.

##### ✅ Ưu tiên:

```swift
var deviceModels: [String]
var employees: [Int: String]
var faxNumber: Int?
```

##### ⛔️ Không được ưa thích:

```swift
var deviceModels: Array<String>
var employees: Dictionary<Int, String>
var faxNumber: Optional<Int>
```

## 12 - Functions vs Methods

- Các chức năng miễn phí, không gắn liền với một lớp hoặc kiểu, nên được sử dụng một cách tiết kiệm.
- Khi có thể, hãy ưu tiên sử dụng một phương thức thay vì một hàm miễn phí. Điều này hỗ trợ khả năng đọc và khả năng khám phá.
- Các hàm miễn phí thích hợp nhất khi chúng không được liên kết với bất kỳ kiểu hoặc trường hợp cụ thể nào.

##### ✅ Ưu tiên:

```swift
let sorted = items.mergeSorted() // easily discoverable
rocket.launch() // acts on the model
```

##### ⛔️ Không được ưa thích:

```swift
let sorted = mergeSort(items) // hard to discover
launch(&rocket)
```

##### Ngoại lệ:

```swift
let tuples = zip(a, b) // feels natural as a free function (symmetry)
let value = max(x, y, z) // another free function that feels natural
```

## 13 - Quản lý bộ nhớ

- Mã không nên tạo các chu trình tham chiếu.
- Phân tích đồ thị đối tượng của bạn và ngăn chặn các chu kỳ mạnh với `weak` và `unowned` tham chiếu.
- Ngoài ra, hãy sử dụng các kiểu giá trị (struct, enum) để ngăn chặn hoàn toàn các chu kỳ.

### a. Kéo dài thời gian tồn tại của đối tượng

- Kéo dài thời gian tồn tại của đối tượng bằng cách sử dụng `[weak self]` và thành ngữ `guard let self = self else { return }`.

##### ✅ Ưu tiên:

```swift
resource.request().onComplete { [weak self] response in
  guard let self = self else {
    return
  }
  let model = self.updateModel(response)
  self.updateUI(model)
}
```

##### ⛔️ Không được ưa thích:

```swift
// might crash if self is released before response returns
resource.request().onComplete { [unowned self] response in
  let model = self.updateModel(response)
  self.updateUI(model)
}
```

##### ⛔️ Không được ưa thích:

```swift
// deallocate could happen between updating the model and updating UI
resource.request().onComplete { [weak self] response in
  let model = self?.updateModel(response)
  self?.updateUI(model)
}
```

## 14 - Kiểm soát truy cập

- Việc sử dụng `private` và `fileprivate` thích hợp sẽ làm tăng thêm sự rõ ràng và thúc đẩy sự đóng gói.
- Ưu tiên sử dụng `private`; `fileprivate` chỉ sử dụng khi trình biên dịch khẳng định.
- Chỉ sử dụng một cách rõ ràng `open`, `public` và `internal` khi bạn yêu cầu một đặc điểm kỹ thuật kiểm soát truy cập đầy đủ.

##### ✅ Ưu tiên:

```swift
private let message = "Great Scott!"

class TimeMachine {  
  private dynamic lazy var fluxCapacitor = FluxCapacitor()
}
```

##### ⛔️ Không được ưa thích:

```swift
fileprivate let message = "Great Scott!"

class TimeMachine {  
  lazy dynamic private var fluxCapacitor = FluxCapacitor()
}
```

## 15 - Luồng điều khiển

- Ưu tiên `for-in` kiểu vòng lặp `for` hơn kiểu `while-condition-increment`.

##### ✅ Ưu tiên:

```swift
for _ in 0..<3 {
  print("Hello three times")
}

for (index, person) in attendeeList.enumerated() {
  print("\(person) is at position #\(index)")
}

for index in stride(from: 0, to: items.count, by: 2) {
  print(index)
}

for index in (0...3).reversed() {
  print(index)
}
```

##### ⛔️ Không được ưa thích:

```swift
var i = 0
while i < 3 {
  print("Hello three times")
  i += 1
}


var i = 0
while i < attendeeList.count {
  let person = attendeeList[i]
  print("\(person) is at position #\(i)")
  i += 1
}
```

### a. Toán tử bậc ba

- Toán tử bậc ba `? :`chỉ nên được sử dụng khi nó làm tăng độ rõ ràng hoặc tính gọn gàng của mã.
- Một điều kiện duy nhất thường là tất cả những gì cần được đánh giá.
- Cách sử dụng tốt nhất của toán tử bậc ba là trong khi gán một biến và quyết định giá trị nào sẽ sử dụng.

##### ✅ Ưu tiên:

```swift
let value = 5
result = value != 0 ? x : y

let isHorizontal = true
result = isHorizontal ? x : y
```

##### ⛔️ Không được ưa thích:

```swift
result = a > b ? x = c > d ? c : d : y
```

## 16 - Con đường vàng

- Khi viết mã với các điều kiện, lề bên trái của mã phải là đường "vàng" hoặc "hạnh phúc". Đó là, không lồng các câu lệnh `if`. Nhiều câu lệnh trả về là OK. Tuyên bố được xây dựng cho `guard`.

##### ✅ Ưu tiên:

```swift
func computeFFT(context: Context?, inputData: InputData?) throws -> Frequencies {
  guard let context = context else {
    throw FFTError.noContext
  }
  guard let inputData = inputData else {
    throw FFTError.noInputData
  }

  // use context and input to compute the frequencies
  return frequencies
}
```

##### ⛔️ Không được ưa thích:

```swift
func computeFFT(context: Context?, inputData: InputData?) throws -> Frequencies {
  if let context = context {
    if let inputData = inputData {
      // use context and input to compute the frequencies

      return frequencies
    } else {
      throw FFTError.noInputData
    }
  } else {
    throw FFTError.noContext
  }
}
```

- Khi nhiều optional được mở hoặc có `guard` hoặc `if let`, hãy giảm thiểu việc lồng vào nhau bằng cách sử dụng phiên bản ghép khi có thể.
- Trong phiên bản ghép, đặt điều kiện `guard` trên dòng riêng của nó, sau đó thụt lề từng điều kiện trên dòng riêng của nó. Mệnh đề `else` được thụt vào để khớp với `guard` chính nó.

##### ✅ Ưu tiên:

```swift
guard 
  let number1 = number1,
  let number2 = number2,
  let number3 = number3 
else {
  fatalError("impossible")
}
// do something with numbers
```

##### ⛔️ Không được ưa thích:

```swift
if let number1 = number1 {
  if let number2 = number2 {
    if let number3 = number3 {
      // do something with numbers
    } else {
      fatalError("impossible")
    }
  } else {
    fatalError("impossible")
  }
} else {
  fatalError("impossible")
}
```

## 17 - Dấu chấm phẩy

- Swift không yêu cầu dấu chấm phẩy sau mỗi câu lệnh trong mã của bạn. Chúng chỉ được yêu cầu nếu bạn muốn kết hợp nhiều câu lệnh trên một dòng.
- Không viết nhiều câu lệnh trên một dòng được phân tách bằng dấu chấm phẩy.

##### ✅ Ưu tiên:

```swift
let swift = "not a scripting language"
```

##### ⛔️ Không được ưa thích:

```swift
let swift = "not a scripting language";
```

## 18 - Dấu ngoặc đơn

- Dấu ngoặc đơn xung quanh các điều kiện là không bắt buộc và nên được bỏ qua.

##### ✅ Ưu tiên:

```swift
if name == "Hello" {
  print("World")
}
```

##### ⛔️ Không được ưa thích:

```swift
if (name == "Hello") {
  print("World")
}
```

Trong các biểu thức lớn hơn, các dấu ngoặc đơn tùy chọn đôi khi có thể làm cho mã đọc rõ ràng hơn.

##### ✅ Ưu tiên:

```swift
let playerMark = (player == current ? "X" : "O")
```

## 19 - Chữ viết chuỗi nhiều dòng

Khi xây dựng một chuỗi ký tự dài, bạn nên sử dụng cú pháp ký tự chuỗi nhiều dòng. Mở văn bản trên cùng dòng với nhiệm vụ nhưng không bao gồm văn bản trên dòng đó. Thụt lề khối văn bản một cấp độ bổ sung.

##### ✅ Ưu tiên:

```swift
let message = """
  You cannot charge the flux \
  capacitor with a 9V battery.
  You must use a super-charger \
  which costs 10 credits. You currently \
  have \(credits) credits available.
  """
```

##### ⛔️ Không được ưa thích:

```swift
let message = """You cannot charge the flux \
  capacitor with a 9V battery.
  You must use a super-charger \
  which costs 10 credits. You currently \
  have \(credits) credits available.
  """
```

##### ⛔️ Không được ưa thích:

```swift
let message = "You cannot charge the flux " +
  "capacitor with a 9V battery.\n" +
  "You must use a super-charger " +
  "which costs 10 credits. You currently " +
  "have \(credits) credits available."
```

## 20 - Không có biểu tượng cảm xúc

- Không sử dụng biểu tượng cảm xúc trong các dự án của bạn.
- Đối với những độc giả thực sự gõ mã của họ, đó là một nguồn gây xích mích không cần thiết. Mặc dù nó có thể dễ thương, nhưng nó không bổ sung vào việc học và nó làm gián đoạn quá trình viết mã cho những người đọc này.

## 21 - Không #imageLiteral hoặc #colorLiteral

- Không sử dụng khả năng của Xcode để kéo màu hoặc hình ảnh vào một câu lệnh nguồn. Những thứ này lần lượt biến thành #colorLiteral và #imageLiteral và đưa ra những thách thức khó chịu cho người đọc khi cố gắng nhập chúng dựa trên văn bản hướng dẫn. Thay vào đó, hãy sử dụng `UIColor(red:green:blue)` và `UIImage(imageLiteralResourceName:)`.
