# git-TT

<?php/* Template Name: payment  */?>
 <?php
    $servername = "localhost";
    $database = "admin";
    $username = "admin";
    $password = "";
    $conn = mysqli_connect($servername, $username, $password, $database);

    if (!$conn) {
        die("Connection failed: " . mysqli_connect_error());
    }
    if(isset($_POST['btn_book_ticker'])&&($_POST['btn_book_ticker'])){
        $ticket = $_POST['ticket'];
        $sl_ticket = $_POST['SL_ticket'];
        $date = $_POST['date'];
        $full_name = $_POST['fullname'];
        $phone = $_POST['phone'];
        $email = $_POST['email'];
        $sql_khachhang = mysqli_query($conn,"INSERT INTO WP_DATVE(DV_LOAIVE,DV_SLVE,DV_DATE,DV_FULLNAME,DV_PHONE,DV_EMAIL) 
        VALUES('$ticket','$sl_ticket','$date','$fullname','$phone','$email')");
        $last_id = mysqli_insert_id($conn);
        echo "succes";
    }
?> 
<?php get_header();?>
    <p class="absolute left-[708px] top-[144px] w-[536px] font-black text-8xl text-white">Thanh toán</p>
    <img src="/TTAP-TN/wp-content/uploads/2021/11/Group-1-2.png" alt="" class="absolute z-10 left-[330px] top-[264.81px]">
    <img src="/TTAP-TN/wp-content/uploads/2021/11/Group-2-1.png" alt="" class="absolute z-10 left-[1257px] top-[264.81px]">
    <img src="/TTAP-TN/wp-content/uploads/2021/11/Group.png" alt="" 
    class="absolute h-96 w-96 mx-4 top-56 md:w-[600px] md:left-20 md:h-[450px] lg:w-auto xl:w-auto lg:left-auto lg:right-auto xl:bg-center 
        2xl:w-[950px] 2xl:h-[642px] 2xl:left-[202px] 2xl:top-[293px] 2xl:bottom-[115px]">

    <img src="/TTAP-TN/wp-content/uploads/2021/11/Vector.png" alt="" 
    class="absolute hidden sm:hidden md:hidden lg:hidden  2xl:block  2xl:left-[1124px] 2xl:top-[293px] 2xl:bottom-[131.19px] 2xl:w-[141.04px] 2xl:h-[639px]">

    <img src="/TTAP-TN/wp-content/uploads/2021/11/Group-1-1.png" alt="" 
    class="absolute mx-4 w-96 top-[650px] h-96  2xl:left-[1181px] 2xl:top-[293px] 2xl:bottom-[115px] 2xl:w-[539px] 2xl:h-[657px]">

    <img src="/TTAP-TN/wp-content/uploads/2021/11/Trini_Arnold_Votay1-2-1.png" alt="" class="absolute z-10 top-[346px]">

    <p class="absolute z-10 font-bold text-xl left-[330px] top-[374px] text-[#23221F]">Số tiền thanh toán</p>

    <input type="text" name="monney" class="ticket-group absolute z-10 left-[330px] top-[412px] w-[233px] h-14 outline-none rounded-2xl px-4 py-5" 
    value="">

    <p class="absolute z-10 font-bold text-xl left-[627px] top-[374px] text-[#23221F]">Số lượng vé</p>

    <input type="text" name="ticket_quantity" class="ticket-group absolute z-10 left-[627px] top-[412px] w-[94px] h-14 rounded-2xl outline-none px-4 py-5"  
    value="">

    <p class="absolute z-10 text-[#23221F] left-[729px] top-[427px] font-medium text-lg">vé</p>

    <p class="absolute z-10 left-[814px] top-[374px] font-bold text-xl text-[#23221F]">Ngày sử dụng</p>

    <input type="text" name="date_time" class="ticket-group absolute z-10 left-[814px] top-[412px] w-[234px] h-14 rounded-2xl outline-none px-4 py-5"  
    value="">

    <p class="absolute z-10 left-[330px] top-[484px] font-bold text-xl text-[#23221F]">Thông tin liên hệ</p>

    <input type="text" name="fname" class="ticket-group absolute z-10 left-[330px] top-[522px] w-[391px] h-14 rounded-2xl outline-none px-4 py-5"  
    value="">

    <p class="absolute z-10 left-[330px] top-[594px] font-bold text-xl text-[#23221F]">Điện thoại</p>

    <input type="text" name="phone_pt" class="ticket-group absolute z-10 left-[330px] top-[632px] w-[233px] h-14 rounded-2xl outline-none px-4 py-5"  
    value="">

    <p class="absolute z-10 left-[330px] top-[704px] font-bold text-xl text-[#23221F]">Email</p>

    <input type="text" name="email_pt" class="ticket-group absolute z-10 left-[330px] top-[742px] w-[391px] h-14 rounded-2xl outline-none px-4 py-5"  
    value="">

    <p class="absolute z-10 left-[1250px] top-[374px] font-bold text-xl text-[#23221F]">Số thẻ</p>

    <input type="text" name="" class="ticket-group absolute z-10 left-[1250px] top-[412px] w-[411px] h-14 rounded-2xl outline-none px-4 py-5"  value="">

    <p class="absolute z-10 left-[1250px] top-[484px] font-bold text-xl text-[#23221F]">Họ tên chủ thẻ</p>

    <input type="text" name="" class="ticket-group absolute z-10 left-[1250px] top-[522px] w-[411px] h-14 rounded-2xl outline-none px-4 py-5"  value="">

    <p class="absolute z-10 left-[1250px] top-[594px] font-bold text-xl text-[#23221F]">Ngày hết hạn</p>

    <input type="text" name="" class="ticket-group absolute z-10 left-[1250px] top-[632px] w-[342px] h-14 rounded-2xl outline-none px-4 py-5"  value="">

    <img src="/TTAP-TN/wp-content/uploads/2021/11/Frame.png" alt="" class="absolute z-10 left-[1603px] top-[632px] w-[53] h-14">

    <p class="absolute z-10 left-[1250px] top-[704px] font-bold text-xl text-[#23221F]">CVV/CVC</p>

    <input type="password" name="" placeholder="***" class="ticket-group absolute z-10 left-[1250px] top-[742px] w-[113px] h-14 rounded-2xl outline-none px-4 py-5"  value="">

    <button type="submit" class="btn-btn absolute w-[368px] h-[68px] left-[1268px] top-[822px] bg-[#FF000A] rounded-xl z-10 text-white font-black text-2xl">Thanh toán</button>
    <button type="submit" class="btn-btn absolute w-[368px] h-[68px] left-[1268px] top-[829px] bg-[#BD000B] rounded-xl z-0"></button>

<?php get_footer();?>
