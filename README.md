# Smart_gold
My business landing page 
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>كراسة مواصفات ونظام فوترة شركة سمارت جولد لينك</title>
    <style>
        :root {
            --gold: #d4af37;
            --dark-gold: #8c7623;
            --bg-light: #fcfbfa;
            --dark-charcoal: #2b2b2b;
            --gray-input: #fafafa;
            --border-color: #dcd7cc;
            --whatsapp-green: #25d366;
            --pdf-red: #e4405f;
            --primary-blue: #007bff;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-light);
            color: var(--dark-charcoal);
            line-height: 1.6;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: #ffffff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        /* 1. رأس الصفحة والهوية البصرية */
        .header-container {
            border-bottom: 3px solid var(--gold);
            padding-bottom: 20px;
            margin-bottom: 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
        }

        .title-area {
            flex: 1;
            min-width: 300px;
        }

        .title-area h1 {
            color: var(--dark-gold);
            font-size: 26px;
            margin-bottom: 5px;
        }

        .title-area p {
            font-size: 14px;
            color: #666;
            margin-bottom: 15px;
        }

        .jordan-flag-area {
            text-align: left;
            font-size: 12px;
            line-height: 1.4;
        }

        .flag-box {
            display: inline-block;
            width: 60px;
            height: 33px;
            background: linear-gradient(to bottom, #000 33.3%, #fff 33.3%, #fff 66.6%, #007a3d 66.6%);
            position: relative;
            border: 1px solid #ccc;
            margin-bottom: 5px;
        }

        .flag-box::before {
            content: "";
            position: absolute;
            top: 0;
            right: 0;
            width: 0;
            height: 0;
            border-top: 16.5px solid transparent;
            border-bottom: 16.5px solid transparent;
            border-right: 24px solid #ce1126;
        }

        /* العناوين والأقسام الرئيسيّة */
        .section-title {
            color: var(--dark-gold);
            font-size: 18px;
            border-bottom: 2px solid #e0dbd3;
            padding-bottom: 5px;
            margin: 35px 0 15px 0;
            font-weight: bold;
        }

        .info-block {
            background-color: #f7f5f0;
            padding: 15px;
            border-radius: 6px;
            border-right: 5px solid var(--gold);
            margin-bottom: 20px;
        }

        .info-block p {
            margin: 5px 0;
        }

        /* 3. شريط الماركات المدعومة (Infinite-like Slider CSS) */
        .brand-slider {
            background: #fff;
            border: 1px solid var(--border-color);
            padding: 15px;
            overflow-x: auto;
            white-space: nowrap;
            border-radius: 6px;
            text-align: center;
        }

        .brand-item {
            display: inline-block;
            margin: 0 12px;
            color: var(--dark-gold);
            background: #f0ede6;
            padding: 6px 18px;
            border-radius: 20px;
            font-weight: bold;
            font-size: 14px;
        }

        /* 4 & 5. نظام النماذج الذكية للأجهزة والمحافظات */
        .form-mockup {
            border: 1px solid var(--border-color);
            background-color: #fff;
            padding: 25px;
            border-radius: 8px;
            margin-top: 20px;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.01);
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-bottom: 20px;
        }

        @media (max-width: 768px) {
            .form-grid { grid-template-columns: 1fr; }
            .form-group.full-width { grid-column: span 1 !important; }
            .summary-box { width: 100% !important; }
            .header-container { text-align: center; justify-content: center; }
            .jordan-flag-area { text-align: center; }
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group.full-width {
            grid-column: span 2;
        }

        label {
            font-weight: bold;
            margin-bottom: 6px;
            color: #444;
            font-size: 14px;
        }

        input, select, textarea {
            padding: 10px;
            background-color: var(--gray-input);
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 14px;
            width: 100%;
            outline: none;
        }

        input:focus, select:focus, textarea:focus {
            border-color: var(--gold);
        }

        /* 7. جداول الفوترة الديناميكية */
        .dynamic-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            font-size: 14px;
        }

        .dynamic-table th, .dynamic-table td {
            border: 1px solid var(--border-color);
            padding: 12px;
            text-align: right;
        }

        .dynamic-table th {
            background-color: var(--dark-gold);
            color: white;
        }

        /* صندوق الإجماليات والملخص المالي */
        .summary-box {
            width: 40%;
            margin-right: auto;
            background: #faf9f6;
            padding: 20px;
            border-radius: 6px;
            border: 1px solid var(--border-color);
        }

        .summary-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            font-size: 14px;
        }

        .summary-row.total {
            border-top: 2px solid var(--gold);
            padding-top: 10px;
            font-weight: bold;
            font-size: 16px;
            color: var(--dark-gold);
        }

        /* 7-ز. نظام التنبيهات الذكي للـ UX */
        .alert {
            padding: 12px 15px;
            border-radius: 4px;
            margin-bottom: 15px;
            font-size: 13px;
            font-weight: bold;
        }
        .alert-danger {
            background-color: #f8d7da;
            color: #721c24;
            border-right: 5px solid #dc3545;
        }
        .alert-warning {
            background-color: #fff3cd;
            color: #856404;
            border-right: 5px solid #ffc107;
        }

        /* أزرار الإجراء والتحكم */
        .btn-container {
            margin-top: 25px;
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
            font-size: 14px;
            color: white;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            transition: opacity 0.2s;
        }

        .btn:hover { opacity: 0.9; }
        .btn-whatsapp { background-color: var(--whatsapp-green); }
        .btn-pdf { background-color: var(--pdf-red); }
        .btn-save { background-color: #6c757d; }
        .btn-primary { background-color: var(--primary-blue); }
        .btn-cancel { background-color: #dc3545; }
        .btn-action { background-color: var(--dark-gold); color: #fff; }
        .btn-small-del { background-color: #dc3545; padding: 4px 8px; font-size: 12px; border-radius: 3px; }

        /* معرض الأعمال الدائري المتفاعل */
        .gallery-mockup {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .gallery-item {
            background: #f0ede6;
            border: 1px solid var(--border-color);
            height: 120px;
            border-radius: 6px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            font-size: 13px;
            font-weight: bold;
            color: #555;
            cursor: pointer;
            transition: transform 0.2s, background-color 0.2s;
        }

        .gallery-item:hover {
            transform: scale(1.03);
            background-color: #e6e1d6;
        }

        .footer {
            text-align: center;
            font-size: 12px;
            color: #777;
            margin-top: 50px;
            border-top: 1px solid var(--border-color);
            padding-top: 20px;
        }
    </style>
</head>
<body>

    <div class="container">
        
        <!-- 1. رأس الصفحة والهوية البصرية -->
        <header class="header-container">
            <div class="title-area">
                <h1>شركة سمارت جولد لينك (Smart Gold Link)</h1>
                <p>راحتك تبدأ بلمسة ذكية – خدمات التكييف والصيانة المنزلية الفورية في الأردن</p>
                <div class="btn-container" style="margin-top: 10px;">
                    <a href="tel:0790252605" class="btn btn-primary">اتصال فوري بـ سمارت جولد لينك 📞</a>
                    <a href="https://wa.me/962790252605" target="_blank" class="btn btn-whatsapp">مراسلة واتساب فورية 💬</a>
                </div>
            </div>
            <div class="jordan-flag-area">
                <div class="flag-box"></div>
                <div><strong>المملكة الأردنية الهاشمية</strong></div>
                <div>The Hashemite Kingdom of Jordan</div>
            </div>
        </header>

        <!-- 2. من نحن وعراقة الشركة -->
        <section>
            <div class="section-title">2. من نحن؟ (العراقة والموثوقية القانونية)</div>
            <div class="info-block">
                <p><strong>مسيرة التميز:</strong> تأسست الشركة رسمياً في <strong>7 سبتمبر 2008 (7/9/2008)</strong> لتقديم أرقى خدمات الصيانة.</p>
                <p><strong>الوضع القانوني:</strong> شركة مرخصة ومسجلة رسمياً بالكامل لدى <strong>وزارة الصناعة والتجارة الأردنية</strong>.</p>
                <p><strong>الإدارة العامة:</strong> تُدار وتعمل بكافة طواقمها تحت إشراف وتوجيهات المدير العام السيد <strong>فهد السعودي</strong>.</p>
            </div>
        </section>

        <!-- 3. شريط الماركات المدعومة -->
        <section>
            <div class="section-title">3. شريط الماركات العالمية المدعومة (Brand Partners Slider)</div>
            <div class="brand-slider">
                <div class="brand-item">LG</div>
                <div class="brand-item">National</div>
                <div class="brand-item">Samsung</div>
                <div class="brand-item">Beko</div>
                <div class="brand-item">Vestel</div>
                <div class="brand-item">Hyundai</div>
                <div class="brand-item">Hitachi</div>
                <div class="brand-item">Gree</div>
                <div class="brand-item">Green Aux</div>
                <div class="brand-item">Midea</div>
            </div>
        </section>

        <!-- 4 & 5. نماذج الصيانة وتحديد الجغرافيا والمحافظات الـ 12 -->
        <section>
            <div class="section-title">4 & 5. طلب خدمة صيانة وتحديد الموقع (المحافظات الـ 12)</div>
            <div class="form-mockup">
                <form onsubmit="event.preventDefault();">
                    <div class="form-grid">
                        <div class="form-group">
                            <label>نوع الجهاز الكهربائي المطلوب صيانته:</label>
                            <select>
                                <option>مكيفات وأنظمة تبريد</option>
                                <option>غسالات</option>
                                <option>ثلاجات وفريزرات</option>
                                <option>جلايات صحون</option>
                                <option>شاشات وتلفزيونات</option>
                                <option>حماصات وأجهزة صغيرة</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>الماركة / نوع المصنع:</label>
                            <input type="text" placeholder="مثال: Samsung, LG, Beko...">
                        </div>
                        <div class="form-group full-width">
                            <label>وصف العطل بالتفصيل:</label>
                            <textarea placeholder="يرجى كتابة تفاصيل المشكلة أو الرموز الظاهرة على الشاشة..."></textarea>
                        </div>
                        
                        <!-- التغطية الجغرافية -->
                        <div class="form-group">
                            <label>المحافظة (تغطية شاملة لـ 12 محافظة):</label>
                            <select>
                                <option>العاصمة عمان</option>
                                <option>إربد</option>
                                <option>الزرقاء</option>
                                <option>المفرق</option>
                                <option>جرش</option>
                                <option>عجلون</option>
                                <option>البلقاء</option>
                                <option>مأدبا</option>
                                <option>الكرك</option>
                                <option>الطفيلة</option>
                                <option>معان</option>
                                <option>العقبة</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>الحي / المنطقة الدقيقة:</label>
                            <input type="text" placeholder="مثال: العبدلي، تلاع العلي...">
                        </div>
                        <div class="form-group">
                            <label>الشارع / اسم العمارة:</label>
                            <input type="text" placeholder="اسم الشارع ورقم العمارة">
                        </div>
                        <div class="form-group">
                            <label>رقم الشقة / الطابق:</label>
                            <input type="text" placeholder="مثال: طابق 3 - شقة 12">
                        </div>
                        <div class="form-group">
                            <label>رقم الهاتف الأساسي للعميل:</label>
                            <input type="tel" placeholder="07XXXXXXXX">
                        </div>
                        <div class="form-group">
                            <label>رقم الهاتف الاحتياطي البديل:</label>
                            <input type="tel" placeholder="رقم اتصال بديل آخر">
                        </div>
                    </div>
                    
                    <div style="background: #fdfaf4; padding: 12px; border-radius: 4px; margin-bottom: 15px; font-size: 13px;">
                        <strong>💵 طرق الدفع المتوفرة والمقبولة بالكامل:</strong> كليك (CliQ) • المحافظ الإلكترونية (زين كاش، أمنية) • تحويل بنكي مباشر • نقداً (كاش) عند الاستلام والمعاينة.
                    </div>

                    <button type="submit" class="btn btn-whatsapp" style="width: 100%;">إرسال الطلب والموقع عبر الواتساب 🚀</button>
                </form>
            </div>
        </section>

        <!-- 7. نظام فورم الفوترة الذكي والاحترافي -->
        <section>
            <div class="section-title">7. قالب الفوترة الاحترافي والقانوني المعتمد (Invoicing Module)</div>
            
            <!-- 7-ز. نظام التنبيهات المدمج للـ UI/UX -->
            <div class="alert alert-warning">⚠️ تنبيه مستخدم (UX): التاريخ المدخل قديم جداً أو خارج النطاق الحالي، يرجى مراجعته.</div>
            <div class="alert alert-danger">🛑 خطأ مالي قانوني: تم ترك الحقل الضريبي فارغاً! يرجى تحديده لمنع وقوع مخالفات مالية مع الدائرة.</div>

            <div class="form-mockup" style="border: 2px solid var(--gold);">
                <!-- ترويسة الفاتورة الثابتة والمطبوعة آلياً -->
                <div style="display: flex; justify-content: space-between; border-bottom: 2px dashed var(--gold); padding-bottom: 15px; margin-bottom: 20px; font-size: 13px;">
                    <div>
                        <h3 style="color: var(--dark-gold); font-size: 18px; margin-bottom: 5px;">شركة سمارت جولد لينك للصيانة والتكييف</h3>
                        <p><strong>العنوان:</strong> الأردن - العاصمة عمان - منطقة العبدلي</p>
                        <p><strong>صندوق بريد:</strong> 68 | <strong>الرمز البريدي:</strong> 11190</p>
                        <p><strong>هاتف وواتساب التنسيق:</strong> 0790252605</p>
                    </div>
                    <div style="text-align: left;">
                        <p style="font-size: 15px; font-weight: bold; color: var(--dark-gold);">رقم ضريبة المبيعات الثابت:</p>
                        <p style="font-size: 18px; font-weight: bold; letter-spacing: 2px; color: #000;">014294923</p>
                    </div>
                </div>

                <form>
                    <!-- بيانات الفاتورة والعميل الأساسية -->
                    <div class="form-grid">
                        <div class="form-group">
                            <label>رقم الفاتورة (تسلسلي تلقائي):</label>
                            <input type="text" value="#SGL-2026-1024" readonly style="font-weight: bold; color: var(--dark-gold); background: #eee;">
                        </div>
                        <div class="form-group">
                            <label>العملة المعتمدة:</label>
                            <input type="text" value="الدينار الأردني (JOD)" readonly style="background: #eee;">
                        </div>
                        <div class="form-group">
                            <label>تاريخ إصدار الفاتورة المعتمد:</label>
                            <input type="date" value="2026-07-11">
                        </div>
                        <div class="form-group">
                            <label>تاريخ استحقاق الفاتورة المالي:</label>
                            <input type="date" value="2026-07-26">
                        </div>
                        <div class="form-group">
                            <label>التاريخ الفعلي لاستلام الخدمة:</label>
                            <input type="date">
                        </div>
                        <div class="form-group">
                            <label>رقم هاتف الفني المشرف على العمل:</label>
                            <input type="text" placeholder="رقم هاتف فني الصيانة المسؤول">
                        </div>
                    </div>

                    <h4 style="margin: 15px 0 10px 0; color: var(--dark-gold); border-bottom: 1px solid #eee; padding-bottom: 3px;">بيانات العميل المستهدف</h4>
                    <div class="form-grid">
                        <div class="form-group">
                            <label>اسم العميل / الشركة المستلمة:</label>
                            <input type="text" placeholder="اكتب الاسم بالكامل">
                            <label style="margin-top: 6px; font-weight: normal; font-size: 12px; display: flex; align-items: center; gap: 5px;">
                                <input type="checkbox" style="width: auto;"> حفظ بيانات العميل في السجلات لتقليل وقت الإدخال مستقبلاً
                            </label>
                        </div>
                        <div class="form-group">
                            <label>رقم التعريف المالي للعميل (الهاتف / الرقم الضريبي):</label>
                            <input type="text" placeholder="رقم الاتصال أو الرقم الضريبي للشركات">
                        </div>
                    </div>

                    <!-- جدول بنود الخدمات الديناميكي -->
                    <h4 style="margin: 20px 0 10px 0; color: var(--dark-gold);">جدول تفاصيل البنود والخدمات المستحقة</h4>
                    <table class="dynamic-table">
                        <thead>
                            <tr>
                                <th>وصف الخدمة / الأجزاء المستبدلة</th>
                                <th style="width: 10%;">الكمية</th>
                                <th style="width: 15%;">سعر الوحدة</th>
                                <th style="width: 12%;">الضريبة (%)</th>
                                <th style="width: 20%;">الإجمالي الفرعي</th>
                                <th style="width: 8%;">إجراء</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><input type="text" value="صيانة مكيف سبليت وتنظيف الفلاتر مع تعبئة غاز"></td>
                                <td><input type="number" value="1"></td>
                                <td><input type="number" value="35.00"></td>
                                <td><input type="number" value="16"></td>
                                <td><input type="number" value="40.60" readonly style="font-weight: bold; background: #f0f0f0;"></td>
                                <td style="text-align: center;"><button class="btn btn-small-del">× حذف</button></td>
                            </tr>
                        </tbody>
                    </table>
                    <button type="button" class="btn btn-action" style="font-size: 12px; padding: 5px 12px;">+ إضافة بند جديد</button>

                    <!-- شروط الملاحظات والملخص المالي النهائي -->
                    <div style="display: flex; justify-content: space-between; margin-top: 30px; flex-wrap: wrap; gap: 20px;">
                        <div style="flex: 1; min-width: 300px;">
                            <label>شروط وأحكام الفاتورة الثابتة:</label>
                            <input type="text" value="شروط الدفع مباشرة، يرجى السداد خلال مدة لا تتجاوز 15 يوماً من تاريخ استلام الخدمة" readonly style="font-size: 12px; background: #eee; margin-bottom: 15px;">
                            
                            <label>صندوق الملاحظات الحرة للفني (الكفالة والتفاصيل):</label>
                            <textarea placeholder="اكتب هنا تفاصيل كفالة القطع المستبدلة أو أي توصيات أخرى للعميل..."></textarea>
                        </div>
                        
                        <div class="summary-box">
                            <div class="summary-row">
                                <span>إجمالي المبالغ الفرعية قبل الضريبة:</span>
                                <strong>35.00 د.أ</strong>
                            </div>
                            <div class="summary-row">
                                <span>إجمالي قيمة الضريبة المضافة:</span>
                                <strong>5.60 د.أ</strong>
                            </div>
                            <div class="summary-row" style="align-items: center;">
                                <span>قيمة الخصم الممنوح (إن وجد):</span>
                                <input type="number" value="0.00" style="width: 90px; padding: 4px; text-align: center;">
                            </div>
                            <div class="summary-row total">
                                <span>صافي المبلغ المستحق النهائي:</span>
                                <span>40.60 د.أ</span>
                            </div>
                        </div>
                    </div>

                    <!-- أزرار التحكم والعمليات المتاحة بالفاتورة -->
                    <div class="btn-container" style="justify-content: center; border-top: 1px solid #eee; padding-top: 25px; margin-top: 25px;">
                        <button type="button" class="btn btn-save">حفظ كمسودة 💾</button>
                        <button type="button" class="btn btn-action">معاينة الفاتورة 👁️</button>
                        <button type="button" class="btn btn-primary">إصدار فاتورة 🚀</button>
                        <button type="button" class="btn btn-whatsapp">إرسال للعميل عبر واتساب 💬</button>
                        <button type="button" class="btn btn-pdf">تحميل الفاتورة PDF 📄</button>
                        <button type="button" class="btn btn-cancel">إلغاء العملية بالكامل ❌</button>
                    </div>
                </form>
            </div>
        </section>

        <!-- 8. معرض أعمالنا الميداني والتفاعلي -->
        <section>
            <div class="section-title">8. معرض أعمالنا الحي والميداني من مواقع الصيانة الفورية</div>
            <div class="gallery-mockup">
                <div class="gallery-item">صيانة مكيفات هواء ❄️</div>
                <div class="gallery-item">إصلاح غسالات ملابس 🧺</div>
                <div class="gallery-item">صيانة ثلاجات وأنظمة تبريد ❄️</div>
                <div class="gallery-item">صيانة جلايات صحون 🍽️</div>
                <div class="gallery-item">فحص شاشات ذكية 📺</div>
                <div class="gallery-item">صيانة حماصات وأجهزة مطبخ 🍞</div>
            </div>
        </section>

        <!-- 9. صندوق الشكاوى المباشر للإدارة -->
        <section>
            <div class="section-title">9. صندوق الشكاوى والمقترحات المباشر الموجه للإدارة العامة</div>
            <div class="form-mockup" style="border-right: 5px solid var(--pdf-red);">
                <p style="font-size: 13px; color: #555; margin-bottom: 15px;">يسعى المدير العام فهد السعودي وكافة أفراد إدارة <strong>"سمارت جولد لينك"</strong> لتقديم خدمة خالية من الأخطاء. في حال وجود أي ملاحظة، تواصل معنا مباشرة:</p>
                <form onsubmit="event.preventDefault();">
                    <div class="form-grid">
                        <div class="form-group">
                            <label>اسم العميل الثلاثي:</label>
                            <input type="text" placeholder="أدخل اسمك بالكامل">
                        </div>
                        <div class="form-group">
                            <label>رقم هاتف مقدم الشكوى المباشر:</label>
                            <input type="tel" placeholder="07XXXXXXXX">
                        </div>
                        <div class="form-group full-width">
                            <label>اسم فني الصيانة المسؤول عن زيارتكم إن وُجد:</label>
                            <input type="text" placeholder="اسم الفني أو المشرف الميداني">
                        </div>
                        <div class="form-group full-width">
                            <label>تفاصيل الشكوى أو المقترح بدقة:</label>
                            <textarea placeholder="اكتب هنا ما واجهك بالتفصيل لنتمكن من معالجته فوراً..."></textarea>
                        </div>
                    </div>
                    <button type="submit" class="btn btn-cancel" style="width: 100%; background-color: #c82333;">إرسال الشكوى مباشرة عبر الواتساب للإدارة 🚨</button>
                </form>
            </div>
        </section>

        <!-- 10. منصات التواصل وتذييل الصفحة المعتمد -->
        <footer style="margin-top: 40px;">
            <div class="section-title">10. تابعونا وتواصلوا معنا عبر منصاتنا المعتمدة (Social Media)</div>
            <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin-bottom: 20px;">
                <a href="#" style="color: #3b5998; font-weight: bold; text-decoration: none;">🔹 فيسبوك (سمارت جولد لينك)</a>
                <a href="https://www.instagram.com/fahed_ayel_slman?igsh=MWF2Mm83aG1rODZhdQ==" target="_blank" style="color: var(--pdf-red); font-weight: bold; text-decoration: none;">📸 انستغرام الإدارة العامة</a>
                <a href="https://www.youtube.com/@fahdhatmalalsudi" target="_blank" style="color: #cd201f; font-weight: bold; text-decoration: none;">🎥 يوتيوب الإدارة العامة</a>
            </div>
            
            <div class="footer">
                جميع الحقوق محفوظة © <strong>شركة سمارت جولد لينك لصيانة الأجهزة والتكييف</strong><br>
                بإشراف وتوجيهات المدير العام: السيد فهد السعودي<br>
                المقر الرئيسي واللوجستي للشركة: الأردن - العاصمة عمان - منطقة العبدلي
            </div>
        </footer>

    </div>

</body>
</html>
