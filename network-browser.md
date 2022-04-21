1. Network, browser, caching, security.
	  - Thao tác cơ bản với network
		+ ipconfig | ipconfig/all => show thông tin địa chỉ mạng.
		+ ping + ip  || domain  => check kết nối của ip đó.
		+ tracert + ip || domain => kiểm tra đường đi của ip domain đấy
	- Browser: 
		+  Browser architechture: 
			+ User Interface: Tầng cao nhất ( address bar, button reload,.. )
			+ Browser Engine: Tầng giữa và là cầu nối giữa UI và Rendering Engine
			+ Rendering Engine ( Layout Engine ): Vai trò xủ lý HTML, CSS, JS,...
			
		+ Network - Javascript interpreter - Display UI Backend.
			+ Networking: Gọi các giao thức về mạng. ( ví dụ HTTP, WS )
			+ UI Backend: xử lý và hiển thị các UI components phổ biến như boxes, text-box...
			+ Javascript interpreter: Thực thi các đoạn mã Javascript để hiển thị lên trang web.
		+ Data persistence: Có chức năng lưu trữ thong tin và dữ liệu trên máy local, Những dữ liệu này có thể là cache, cookies, local storage, indexedDb, Web SQL,....
	- Flow of rendering engine:
		- B1: Parsing ( HTML to DOM and CSS to CSSOM ), parsing từ trên xuống dưới và sẽ dừng lại nếu gặp thẻ internal/ external, đó là lý do vì sao đưa các thẻ script xuống dưới cùng.
				- Với tag script có 2 thuộc tính ( async, defer ).
					- async: load độc lập và có thể ngăn chặn  parsing blocking.
					- defer thì nó bắt buộc phải load xong content thì mới load nó.
		- B2: Render tree ( combime DOM and CSSOM together )
				- Render tree chỉ chứa những thành phần sẽ được hiển thị trên web. Những element có thuộc tính là display:none hay không hiển thị sẽ được đưa vào render tree
						 + Display none: xem như không hiển thị và không ảnh hưởng tới hiệu năng.
						 + visibility: hidden, trình duyệt sẽ phải xử lý để ẩn element này đi và ảnh hưởng tới hiệu năng của trang web.
		- B3: Layout of the render tree.
		- B4: Painting the render tree. 
	
