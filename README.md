# pacmanAI
pacman Homework
## Bài 1
      Với bài này, một tuple để lưu vị trí và 1 danh sách các hành động của pacman để đến được đi đến đó
      Và tất nhiến sẽ có 1 stack để lưu tất cả chúng
      Sau đó em tạo một dict() để lưu trạng thái đã thăm điểm đó hay chưa
      Bước sau là tạo một vòng lặp while để kiểm soát các điểm nằm trong stack
      Với mỗi điểm đã được thăm thì vòng lặp sẽ lập tức bỏ qua còn nếu không thì nó tìm những điểm có thể đi qua để đẩy vào trong stack 
      Tất cả hành động của pacman đề đã được ghi lại qua biến State do đó co thể trực tiếp trả ra các bước ngay khi tìm được đến đích
      Nếu không tìm được đích thì sẽ trả ra list action rỗng do không tìm 
## Bài 2
      Tương tự bài 1 nhưng mang đặc điểm đặc thù của thuật toán BFS nên sẽ thay Stack bằng Queue và tốc dộ nhanh chậm tùy trường hợp
## Bài 3
      Bài hơi khác một chút khi ta đẩy state trạng thái vào Qrority Queue với giá trị ưu tiên chính là chi phí để đến được đó
## Bài 4 
      Với đặc tính của A* ta sử dụng hàm f(x) = g(x) + h(x) trong đó f(x) là hàm ưu tiên để sắp xếp trạng thái của state, g(x) là unicostsearch 
      và h(x) là hàm ta tự định nghĩa 
      Trong bài này ngoài việc gọi lại giá trị chi phí thực hiện quãng đường và hàm heuristic thì nó tương tự bài 3
## Bài 5
      Để giải bài này với mỗi trạng thái state ta thêm một thuộc tính bao gồm một tuple chứa boolean của 4 điểm góc xem đã thăm nó chưa
      Đã thăm thì tick true và ngược lại
      Và để về địch thì tất nhiên cần 4 điểm đều được tick true
      Còn về hàm getSuccessors thì ta thêm việc mỗi lần đi qua một góc thì nó sẽ được state chưa hành động đó ghi lại và duyệt đủ khi thăm đủ 4 điểm
## Bài 6 
      Khi viết hàm này cho A* thì ý tưởng của em là trong quá trình duyệt đường đi thì ta sẽ trả ra giá trị lớn nhất khoảng cách của vị trí hiện tại 
      với 1 trong 4 điểm nhưng vậy những điểm càng xa thì sẽ có thứ tự ưu tiên thấp hơn còn những điểm ở gần sẽ được đẩy về phía chúng 
      Khi đã thăm xong một điểm thì nó sẽ tự bị đẩy ra ngoài việc so sánh ưu tiên tới các điểm khác
## Bài 7 
      Giống như bài 6 nhưng lại thay bốn góc bằng các điểm chứa food ta cũng trả về giá trị max 
## Bài 8
      Khi dùng A* không phải lúc nào cũng tối ưu thì ta dùng tham lam đối với bài toán này
      Với hàm định tự định nghĩa em dùng khoảng cách manhattanDistance từ điểm hiện tại đến các điểm cần đến để khi pop ra ta
      lấy được điểm có khoảng cách manhatan bé nhất.
      
