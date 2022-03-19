# Tic-Tac-Toe

Ví dụ mô phỏng giải thuật Minimax cho trò chơi Tic-Tac-toe
MAX đại diện quân đi O.
MIN đại diện quân đi X.
Trạng thái kết thúc là trạng thái có 3 ô liên tiếp ngang, dọc, chéo có cùng một quân cờ X hoặc O, nếu là X tức MIN thắng còn O tức MAX thắng còn nếu tất cả các ô cờ đều được đi và trạng thái chưa kết thúc thì bàn cờ hòa. Điểm thắng của X là -1, của O là 1, và bàn cờ hòa là 0.

Áp dụng giải thuật Minimax:

Từ trạng thái bàn cờ hiện tại ta dự đoán nước đi của trạng thái tiếp theo nếu trạng thái tiếp theo ta tiến hành lượng giá cây trò chơi bằng cách ta tiến hành quét cạn tất cả các trạng thái tiếp theo cho đến lúc gặp trạng thái chiến thắng (Node lá) tính điểm cho Node lá bằng cách:

Nếu ở trạng thái mà ta gặp chiến thắng nếu đó là lượt đi của quân X  thì đánh giá điểm trạng thái đó là -1.
Nếu ở trạng thái ta gặp chiến thắng nếu đó là lượt đi của  quân O thì đánh giá điểm trạng thái đó là 1.
Nếu là hòa thì điểm trạng thái đó là 0.
Sau đó tính ngược lại cây trò chơi theo quy tắc:

Nút thuộc lớp MAX thì gán cho nó giá trị lớn nhất của các Node con của Node đó.
Nút thuộc lớp MAX thì gán cho nó giá trị nhỏ nhất của các Node con của Node đó.
Sau khi lượng giá hết cây trò chơi ta tiến hành chọn bước đi tiếp theo nguyên tắc:

Nếu lớp tiếp theo là MAX ta chọn Node con có giá trị lớn nhất.
Nếu lớp tiếp theo là MIN ta chọn Node con có giá trị nhỏ nhất.
