<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>إعدادات الملف الشخصي | نِحرير</title>
    <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-auth-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-firestore-compat.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Kufi+Arabic:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --dark: #0c2340; --gold: #c5a059; --bg: #f0f2f5; }
        body { font-family: 'Noto Kufi Arabic', sans-serif; background: var(--bg); display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
        .box { background: white; padding: 40px; border-radius: 15px; box-shadow: 0 10px 25px rgba(0,0,0,0.1); text-align: center; width: 380px; border-top: 5px solid var(--gold); }
        
        .profile-pic-container { position: relative; width: 130px; height: 130px; margin: 0 auto 20px; }
        .profile-pic { width: 100%; height: 100%; border-radius: 50%; object-fit: cover; border: 3px solid var(--gold); background: #eee; }
        
        .upload-label { position: absolute; bottom: 5px; right: 5px; background: var(--dark); color: white; width: 35px; height: 35px; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; border: 2px solid white; transition: 0.3s; }
        .upload-label:hover { background: var(--gold); }
        #fileInput { display: none; }

        input[type="text"] { width: 100%; padding: 12px; margin-bottom: 20px; border: 1px solid #ddd; border-radius: 8px; box-sizing: border-box; text-align: center; font-family: inherit; }
        
        .btn-save { background: var(--dark); color: white; border: none; padding: 14px; width: 100%; border-radius: 8px; cursor: pointer; font-weight: bold; font-size: 1rem; transition: 0.3s; }
        .btn-save:hover { background: var(--gold); color: var(--dark); }
        
        .back-link { display: block; margin-top: 20px; color: #888; text-decoration: none; font-size: 0.9rem; }
        .status-msg { margin-top: 10px; font-size: 0.8rem; display: none; }
    </style>
</head>
<body>

<div class="box">
    <div class="profile-pic-container">
        <img id="userImg" src="https://via.placeholder.com/130" class="profile-pic">
        <label for="fileInput" class="upload-label">
            <i class="fas fa-camera"></i>
        </label>
        <input type="file" id="fileInput" accept="image/*" onchange="previewImage(event)">
    </div>

    <h3>تعديل الملف الشخصي</h3>
    <p style="font-size: 0.8rem; color: #666; margin-bottom: 20px;">دكتور، يمكنك تغيير اسمك وصورتك الشخصية هنا</p>
    
    <input type="text" id="newName" placeholder="الاسم الكامل">
    
    <button class="btn-save" onclick="updateProfile()">حفظ التغييرات</button>
    <div id="status" class="status-msg"></div>
    
    <a href="index.html" class="back-link"><i class="fas fa-arrow-right"></i> العودة للرئيسية</a>
</div>

<script>
    const firebaseConfig = {
        apiKey: "AIzaSyAOiRs8QWVxo0FMmFJrv_KTNDNvxrp8TzE",
        authDomain: "nihrir-7527c.firebaseapp.com",
        projectId: "nihrir-7527c",
        storageBucket: "nihrir-7527c.firebasestorage.app",
        messagingSenderId: "912985166127",
        appId: "1:912985166127:web:b841722bdcad5d4ef6d1da"
    };

    firebase.initializeApp(firebaseConfig);
    const db = firebase.firestore();
    const auth = firebase.auth();
    let base64Image = "";

    // جلب البيانات الحالية عند فتح الصفحة
    auth.onAuthStateChanged(user => {
        if (user) {
            db.collection('users').doc(user.uid).get().then(doc => {
                if (doc.exists) {
                    const data = doc.data();
                    document.getElementById('newName').value = data.name || "";
                    if (data.photoURL) {
                        document.getElementById('userImg').src = data.photoURL;
                        base64Image = data.photoURL;
                    }
                }
            });
        } else {
            window.location.href = "login.html";
        }
    });

    // معاينة الصورة عند اختيارها من الجهاز
    function previewImage(event) {
        const file = event.target.files[0];
        if (file) {
            const reader = new FileReader();
            reader.onload = function(e) {
                document.getElementById('userImg').src = e.target.result;
                base64Image = e.target.result; // تخزين الصورة بصيغة نصية
            };
            reader.readAsDataURL(file);
        }
    }

    // حفظ التعديلات في Firebase
    async function updateProfile() {
        const user = auth.currentUser;
        const name = document.getElementById('newName').value;
        const statusDiv = document.getElementById('status');

        if (!name) {
            alert("يرجى إدخال الاسم");
            return;
        }

        try {
            statusDiv.style.display = "block";
            statusDiv.style.color = "blue";
            statusDiv.innerText = "جاري الحفظ...";

            await db.collection('users').doc(user.uid).update({
                name: name,
                photoURL: base64Image
            });

            statusDiv.style.color = "green";
            statusDiv.innerText = "تم تحديث الملف الشخصي بنجاح!";
            
            setTimeout(() => {
                window.location.href = "index.html";
            }, 1500);

        } catch (error) {
            console.error(error);
            statusDiv.style.color = "red";
            statusDiv.innerText = "حدث خطأ أثناء الحفظ.";
        }
    }
</script>
</body>
</html>
