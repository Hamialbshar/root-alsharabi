<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مدارس المعالي النموذجية - مأرب</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Cairo', sans-serif;
        }
        .sidebar {
            transition: all 0.3s ease;
        }
        .stat-card {
            transition: transform 0.3s ease;
        }
        .stat-card:hover {
            transform: translateY(-5px);
        }
        .data-table {
            border-collapse: separate;
            border-spacing: 0;
        }
        .data-table th {
            position: sticky;
            top: 0;
            background-color: #f8fafc;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">
    <!-- Header -->
    <header class="bg-gradient-to-r from-blue-600 to-blue-800 text-white shadow-lg">
        <div class="container mx-auto px-4 py-6">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="flex items-center space-x-4 space-x-reverse mb-4 md:mb-0">
                    <div class="bg-white p-3 rounded-full">
                        <i class="fas fa-school text-blue-600 text-2xl"></i>
                    </div>
                    <div>
                        <h1 class="text-2xl md:text-3xl font-bold">مدارس المعالي النموذجية - مأرب</h1>
                        <p class="text-blue-100 mt-1">نظام الإدارة المدرسية المتكامل</p>
                    </div>
                </div>
                <div class="flex items-center space-x-4 space-x-reverse">
                    <div class="hidden md:block">
                        <span class="text-blue-100">مرحباً،</span>
                        <span class="font-semibold">مدير النظام</span>
                    </div>
                    <button class="bg-blue-500 hover:bg-blue-400 px-4 py-2 rounded-lg transition">
                        <i class="fas fa-sign-out-alt ml-2"></i>تسجيل الخروج
                    </button>
                </div>
            </div>
        </div>
    </header>

    <div class="flex">
        <!-- Sidebar -->
        <aside class="sidebar w-64 bg-white shadow-lg min-h-screen hidden md:block">
            <nav class="p-6">
                <div class="mb-8">
                    <h2 class="text-lg font-bold text-gray-700 mb-4 border-b pb-2">
                        <i class="fas fa-bars ml-2"></i>القائمة الرئيسية
                    </h2>
                    <ul class="space-y-2">
                        <li>
                            <a href="#" class="nav-item active" data-section="dashboard">
                                <i class="fas fa-home ml-3"></i>لوحة التحكم
                            </a>
                        </li>
                        <li>
                            <a href="#" class="nav-item" data-section="students">
                                <i class="fas fa-users ml-3"></i>الطلاب
                            </a>
                        </li>
                        <li>
                            <a href="#" class="nav-item" data-section="teachers">
                                <i class="fas fa-chalkboard-teacher ml-3"></i>المعلمون
                            </a>
                        </li>
                        <li>
                            <a href="#" class="nav-item" data-section="attendance">
                                <i class="fas fa-calendar-check ml-3"></i>الحضور والغياب
                            </a>
                        </li>
                        <li>
                            <a href="#" class="nav-item" data-section="grades">
                                <i class="fas fa-chart-line ml-3"></i>الدرجات والنتائج
                            </a>
                        </li>
                        <li>
                            <a href="#" class="nav-item" data-section="database">
                                <i class="fas fa-database ml-3"></i>قاعدة البيانات
                            </a>
                        </li>
                        <li>
                            <a href="#" class="nav-item" data-section="reports">
                                <i class="fas fa-file-alt ml-3"></i>التقارير
                            </a>
                        </li>
                        <li>
                            <a href="#" class="nav-item" data-section="settings">
                                <i class="fas fa-cog ml-3"></i>الإعدادات
                            </a>
                        </li>
                    </ul>
                </div>
                
                <div class="mt-8">
                    <h3 class="text-sm font-bold text-gray-500 mb-3">اتصال GitHub</h3>
                    <div class="bg-gray-50 p-4 rounded-lg">
                        <div class="flex items-center mb-3">
                            <i class="fab fa-github text-gray-700 text-xl ml-2"></i>
                            <span class="font-medium">مزامنة قاعدة البيانات</span>
                        </div>
                        <button id="syncBtn" class="w-full bg-gray-800 hover:bg-gray-700 text-white py-2 rounded-lg transition flex items-center justify-center">
                            <i class="fas fa-sync-alt ml-2"></i>مزامنة مع GitHub
                        </button>
                        <div id="syncStatus" class="mt-2 text-sm text-gray-600 text-center hidden">
                            <i class="fas fa-check-circle text-green-500 ml-1"></i>
                            <span>تمت المزامنة بنجاح</span>
                        </div>
                    </div>
                </div>
            </nav>
        </aside>

        <!-- Main Content -->
        <main class="flex-1 p-4 md:p-8">
            <!-- Dashboard Section (Default) -->
            <section id="dashboard" class="section active">
                <div class="mb-8">
                    <h2 class="text-2xl font-bold text-gray-800">لوحة التحكم</h2>
                    <p class="text-gray-600 mt-2">نظرة عامة على إحصائيات مدارس المعالي النموذجية</p>
                </div>

                <!-- Stats Cards -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mb-8">
                    <div class="stat-card bg-white p-6 rounded-xl shadow-md border-l-4 border-blue-500">
                        <div class="flex justify-between items-center">
                            <div>
                                <p class="text-gray-500 text-sm">إجمالي الطلاب</p>
                                <h3 class="text-2xl font-bold mt-2" id="totalStudents">485</h3>
                            </div>
                            <div class="bg-blue-100 p-3 rounded-full">
                                <i class="fas fa-users text-blue-600 text-xl"></i>
                            </div>
                        </div>
                        <div class="mt-4 text-sm text-green-600">
                            <i class="fas fa-arrow-up ml-1"></i> 12% زيادة هذا الشهر
                        </div>
                    </div>

                    <div class="stat-card bg-white p-6 rounded-xl shadow-md border-l-4 border-green-500">
                        <div class="flex justify-between items-center">
                            <div>
                                <p class="text-gray-500 text-sm">إجمالي المعلمين</p>
                                <h3 class="text-2xl font-bold mt-2" id="totalTeachers">42</h3>
                            </div>
                            <div class="bg-green-100 p-3 rounded-full">
                                <i class="fas fa-chalkboard-teacher text-green-600 text-xl"></i>
                            </div>
                        </div>
                        <div class="mt-4 text-sm text-green-600">
                            <i class="fas fa-arrow-up ml-1"></i> 5% زيادة هذا الشهر
                        </div>
                    </div>

                    <div class="stat-card bg-white p-6 rounded-xl shadow-md border-l-4 border-yellow-500">
                        <div class="flex justify-between items-center">
                            <div>
                                <p class="text-gray-500 text-sm">نسبة الحضور</p>
                                <h3 class="text-2xl font-bold mt-2" id="attendanceRate">94%</h3>
                            </div>
                            <div class="bg-yellow-100 p-3 rounded-full">
                                <i class="fas fa-calendar-check text-yellow-600 text-xl"></i>
                            </div>
                        </div>
                        <div class="mt-4 text-sm text-green-600">
                            <i class="fas fa-arrow-up ml-1"></i> 3% زيادة هذا الأسبوع
                        </div>
                    </div>

                    <div class="stat-card bg-white p-6 rounded-xl shadow-md border-l-4 border-purple-500">
                        <div class="flex justify-between items-center">
                            <div>
                                <p class="text-gray-500 text-sm">متوسط النتائج</p>
                                <h3 class="text-2xl font-bold mt-2" id="averageGrades">86.5%</h3>
                            </div>
                            <div class="bg-purple-100 p-3 rounded-full">
                                <i class="fas fa-chart-line text-purple-600 text-xl"></i>
                            </div>
                        </div>
                        <div class="mt-4 text-sm text-green-600">
                            <i class="fas fa-arrow-up ml-1"></i> 2% زيادة هذا الفصل
                        </div>
                    </div>
                </div>

                <!-- Recent Activity -->
                <div class="bg-white rounded-xl shadow-md p-6 mb-8">
                    <h3 class="text-xl font-bold text-gray-800 mb-6">النشاط الأخير</h3>
                    <div class="space-y-4">
                        <div class="flex items-center p-3 bg-blue-50 rounded-lg">
                            <div class="bg-blue-100 p-2 rounded-full ml-3">
                                <i class="fas fa-user-plus text-blue-600"></i>
                            </div>
                            <div class="flex-1">
                                <p class="font-medium">تم تسجيل طالب جديد</p>
                                <p class="text-sm text-gray-500">أحمد محمد - الصف العاشر</p>
                            </div>
                            <span class="text-sm text-gray-500">منذ ساعتين</span>
                        </div>
                        <div class="flex items-center p-3 bg-green-50 rounded-lg">
                            <div class="bg-green-100 p-2 rounded-full ml-3">
                                <i class="fas fa-chalkboard-teacher text-green-600"></i>
                            </div>
                            <div class="flex-1">
                                <p class="font-medium">تم تعيين معلم جديد</p>
                                <p class="text-sm text-gray-500">أ. سعيد عبدالله - مادة الرياضيات</p>
                            </div>
                            <span class="text-sm text-gray-500">منذ 5 ساعات</span>
                        </div>
                        <div class="flex items-center p-3 bg-yellow-50 rounded-lg">
                            <div class="bg-yellow-100 p-2 rounded-full ml-3">
                                <i class="fas fa-sync-alt text-yellow-600"></i>
                            </div>
                            <div class="flex-1">
                                <p class="font-medium">تمت مزامنة قاعدة البيانات</p>
                                <p class="text-sm text-gray-500">مع GitHub بنجاح</p>
                            </div>
                            <span class="text-sm text-gray-500">منذ يوم</span>
                        </div>
                    </div>
                </div>

                <!-- School Info -->
                <div class="bg-gradient-to-r from-blue-50 to-indigo-50 rounded-xl shadow-md p-6">
                    <h3 class="text-xl font-bold text-gray-800 mb-4">معلومات عن مدارس المعالي النموذجية - مأرب</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div>
                            <p class="text-gray-700 mb-4">
                                تأسست مدارس المعالي النموذجية في مدينة مأرب عام 2010 بهدف تقديم تعليم متميز وفق أعلى المعايير التعليمية. تقدم المدرسة التعليم من المرحلة الابتدائية حتى الثانوية.
                            </p>
                            <ul class="space-y-2 text-gray-700">
                                <li><i class="fas fa-check text-green-500 ml-2"></i> معامل علوم وتكنولوجيا متطورة</li>
                                <li><i class="fas fa-check text-green-500 ml-2"></i> أنشطة رياضية وثقافية متنوعة</li>
                                <li><i class="fas fa-check text-green-500 ml-2"></i> كادر تعليمي مؤهل وذو خبرة</li>
                                <li><i class="fas fa-check text-green-500 ml-2"></i> بيئة تعليمية آمنة ومحفزة</li>
                            </ul>
                        </div>
                        <div class="bg-white p-4 rounded-lg">
                            <h4 class="font-bold text-gray-800 mb-3">معلومات الاتصال</h4>
                            <div class="space-y-3">
                                <div class="flex items-center">
                                    <i class="fas fa-map-marker-alt text-blue-600 ml-3"></i>
                                    <span>مدينة مأرب - حي التعليم - شارع المدارس</span>
                                </div>
                                <div class="flex items-center">
                                    <i class="fas fa-phone text-blue-600 ml-3"></i>
                                    <span>+967 123 456 789</span>
                                </div>
                                <div class="flex items-center">
                                    <i class="fas fa-envelope text-blue-600 ml-3"></i>
                                    <span>info@almaali-schools.edu.ye</span>
                                </div>
                                <div class="flex items-center">
                                    <i class="fab fa-github text-blue-600 ml-3"></i>
                                    <span>github.com/almaali-schools</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Students Section -->
            <section id="students" class="section hidden">
                <div class="mb-8">
                    <h2 class="text-2xl font-bold text-gray-800">إدارة الطلاب</h2>
                    <p class="text-gray-600 mt-2">إضافة وتعديل وحذف بيانات الطلاب</p>
                </div>

                <div class="bg-white rounded-xl shadow-md p-6 mb-6">
                    <div class="flex justify-between items-center mb-6">
                        <h3 class="text-xl font-bold text-gray-800">قائمة الطلاب</h3>
                        <button class="bg-blue-600 hover:bg-blue-700 text-white px-4 py-2 rounded-lg flex items-center">
                            <i class="fas fa-plus ml-2"></i>إضافة طالب جديد
                        </button>
                    </div>

                    <div class="overflow-x-auto">
                        <table class="w-full data-table">
                            <thead class="bg-gray-100">
                                <tr>
                                    <th class="py-3 px-4 text-right font-semibold text-gray-700">الرقم التسلسلي</th>
                                    <th class="py-3 px-4 text-right font-semibold text-gray-700">اسم الطالب</th>
                                    <th class="py-3 px-4 text-right font-semibold text-gray-700">الصف</th>
                                    <th class="py-3 px-4 text-right font-semibold text-gray-700">تاريخ التسجيل</th>
                                    <th class="py-3 px-4 text-right font-semibold text-gray-700">الحالة</th>
                                    <th class="py-3 px-4 text-right font-semibold text-gray-700">الإجراءات</th>
                                </tr>
                            </thead>
                            <tbody id="studentsTable">
                                <!-- Students will be loaded here -->
                            </tbody>
                        </table>
                    </div>
                </div>
            </section>

            <!-- Database Section -->
            <section id="database" class="section hidden">
                <div class="mb-8">
                    <h2 class="text-2xl font-bold text-gray-800">قاعدة البيانات</h2>
                    <p class="text-gray-600 mt-2">إدارة ومزامنة قاعدة بيانات المدارس مع GitHub</p>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                    <div class="lg:col-span-2">
                        <div class="bg-white rounded-xl shadow-md p-6 mb-6">
                            <h3 class="text-xl font-bold text-gray-800 mb-6">هيكل قاعدة البيانات</h3>
                            <div class="space-y-4">
                                <div class="border rounded-lg p-4">
                                    <div class="flex items-center justify-between mb-3">
                                        <h4 class="font-bold text-blue-700">
                                            <i class="fas fa-table ml-2"></i>جدول الطلاب (students)
                                        </h4>
                                        <span class="bg-blue-100 text-blue-800 text-xs px-2 py-1 rounded">485 سجل</span>
                                    </div>
                                    <div class="text-sm text-gray-700 space-y-1">
                                        <div class="flex justify-between">
                                            <span>id: INT (Primary Key)</span>
                                            <span class="text-gray-500">معرف فريد</span>
                                        </div>
                                        <div class="flex justify-between">
                                            <span>name: VARCHAR(100)</span>
                                            <span class="text-gray-500">اسم الطالب</span>
                                        </div>
                                        <div class="flex justify-between">
                                            <span>grade: VARCHAR(20)</span>
                                            <span class="text-gray-500">الصف الدراسي</span>
                                        </div>
                                        <div class="flex justify-between">
                                            <span>birth_date: DATE</span>
                                            <span class="text-gray-500">تاريخ الميلاد</span>
                                        </div>
                                    </div>
                                </div>

                                <div class="border rounded-lg p-4">
                                    <div class="flex items-center justify-between mb-3">
                                        <h4 class="font-bold text-green-700">
                                            <i class="fas fa-table ml-2"></i>جدول المعلمين (teachers)
                                        </h4>
                                        <span class="bg-green-100 text-green-80