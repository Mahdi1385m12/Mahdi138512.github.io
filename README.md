
<!DOCTYPE html>
<html lang="fa">
    <head>
        <link href="./assets/css/bootstrap.min.css" rel="stylesheet" />
        <link href="./assets/css/bootstrap-rtl.min.css" rel="stylesheet" />
        <link href="./assets/css/vazir.css" rel="stylesheet" />
        <link href="./assets/css/style.css?v1.1.2" rel="stylesheet" />
        <title>IRCF | کانفیگ رایگان</title>
        <meta name="description" content="آی پی سالم و تمیز برای کلودفلر (کلادفلر) جهت دسترسی به اینترنت آزاد" />
        <meta name="keywords" content="کلودفلر, کلادفلر, cloudflare, cf, آی پی تمیز, آی پی سالم, اسکن آی پی" />
        <meta name="robots" content="index,follow,noodp" />
        <meta name="googlebot" content="index,follow" />
        <meta name="theme-color" content="#ff7900" />
        <script src="./assets/js/jquery.min.js"></script>
        <script src="./assets/js/bootstrap.min.js"></script>
        <script src="./assets/js/slick-carousel_1.6.0.js"></script>
        <script src="./assets/js/script.js?v1.1.2"></script>
        <meta http-equiv="Content-Security-Policy" content="upgrade-insecure-requests" />
        <meta charset="UTF-8" />
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <link rel="icon" type="image/x-icon" href="./assets/favicon.ico?v1.1" />
    </head>
    <body>
        <nav class="navbar navbar-inverse">
            <div class="container">
                <div class="col-lg-6 col-md-8 col-sm-12 col-xs-12 col-centered">
                    <a href=".">
                        <img src="./assets/img/cflogo.png?v1.1" alt="logo" />
                        <h1>اینترنت برای همه؛ یا هیچ‌کس!</h1>
                    </a>
                </div>
            </div>
        </nav>
        <div class="clearfix"></div>
        <div class="container">
            <div class="col-lg-6 col-md-8 col-sm-12 col-xs-12 col-centered">
                <ul class="nav nav-tabs">
                    <li>
                        <a href="https://ircf.space">معرفی</a>
                    </li>
                    <li>
                        <a href="https://ircf.space/list.php">IP تمیز</a>
                    </li>
                    <li class="dropdown active">
                        <a class="dropdown-toggle" data-toggle="dropdown" href="#">ابزارها <span class="caret"></span></a>
                        <ul class="dropdown-menu">
                            <li><a href="https://ircf.space/scanner.php">معرفی اسکنرها</a></li>
                            <li><a href="https://ircf.space/export.php" target="_blank">خروجی نتایج اسکن</a></li>
                            <li class="divider"></li>
                            <li class="active"><a href="./index.html">کانفیگ رایگان</a></li>
                        </ul>
                    </li>
                    <li class="pull-left">
                        <a href="https://ircf.space/contacts.php">تماس‌باما</a>
                    </li>
                </ul>
                <div class="clearfix"></div>
                <div class="alert alert-info" id="defAlert">
                    <p>توسط این‌ابزار می‌تونین به کانفیگ‌های رایگان گردآوری‌شده از طریق <a href="https://github.com/yebekhe/ConfigCollector" target="_blank">configCollector</a> دسترسی داشته باشین. این‌کانفیگ‌ها به‌صورت خودکار و منظم، بدون دخل‌وتصرف از یه‌سری <a href="https://github.com/yebekhe/ConfigCollector/blob/main/modules/config.php" target="_blank">کانال تلگرامی</a> جمع‌آوری میشن و برای رعایت مسائل امنیتی توصیه میشه تنها برای مصارف عادی ازشون استفاده کنین.</p>
                </div>
                <div class="form-group">
                    <select class="form-control" id="type">
                        <option value="mix">همه‌نوع کانفیگ</option>
                        <option value="reality">کانفیگ REALITY</option>
                        <option value="vless">کانفیگ VLESS</option>
                        <option value="vmess">کانفیگ VMESS</option>
                        <option value="ss">کانفیگ SHADOWSOCKS</option>
                        <option value="trojan">کانفیگ TROJAN</option>
                    </select>
                    <select class="form-control" id="total">
                        <option value="10">حداکثر ۱۰ مورد</option>
                        <option value="25" selected>حداکثر ۲۵ مورد</option>
                        <option value="50">حداکثر ۵۰ مورد</option>
                        <option value="all">همه موارد</option>
                    </select>
                </div>
                <div class="betaVersion rangeSelector">
                    <input type="radio" name="export" id="normal" value="1" checked />
                    <label for="normal">به‌صورت عادی</label>
                    <div class="clearfix"></div>
                    <input type="radio" name="export" id="sub" value="1" />
                    <label for="sub">لینک ساب</label>
                </div>
                <div class="clearfix"></div>
                <div class="btn btn-block btn-default" id="get">دریافت کانفیگ</div>
                <div class="clearfix"></div>
                <div class="fullBox none" id="result">
                    <textarea class="form-control dirLeft"></textarea>
                    <div class="clearfix"></div>
                    <div class="btn btn-link btn-xs" id="copy">کپی کانفیگ</div>
                    <div class="clearfix"></div>
                    <div class="alert alert-warning customers" id="customers">
                        <small class="label label-warning">تامین‌کنندگان</small>
                        <div class="clearfix"></div>
                        <div class="customer-logos slider" id="slider"></div>
                    </div>
                </div>
                <br>
                <div id="donate" class="modal fade" role="dialog">
                    <div class="modal-dialog modal-sm">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h4 class="modal-title">دونیت</h4>
                            </div>
                            <div class="modal-body modalBodyOverflow">
                                <p>درصورت تمایل برای دونیت می‌تونین از یکی‌از روش‌های زیر استفاده کنین:</p>
                                <div class="dirLeft">
                                    <small>Buy me a coffee:</small>
                                    <br>
                                    <a href="https://buymeacoffee.com/ircf" class="btn btn-default btn-block" target="_blank">buymeacoffee.com/ircf</a>
                                    <br>
                                    <small>Tether (TRC20):</small>
                                    <br>
                                    <input type="text" class="form-control text-center" value="TF5cT8fQMuajHGGH141U9JbTygFojkrFdB" />
                                    <br>
                                    <small>Bitcoin:</small>
                                    <br>
                                    <input type="text" class="form-control text-center" value="bc1qyhx0qn9722vdvlz4s64g4sxq3yne0f5ryz3jyd" />
                                    <br>
                                    <small>Tron (TRX):</small>
                                    <br>
                                    <input type="text" class="form-control text-center" value="TF5cT8fQMuajHGGH141U9JbTygFojkrFdB" />
                                    <br>
                                    <small>Ethereum:</small>
                                    <br>
                                    <input type="text" class="form-control text-center" value="0x2A72777912A15A6387a1116f9bDDFe1Cb9474BF1" />
									<br>
                                    <small>Litecoin:</small>
                                    <br>
                                    <input type="text" class="form-control text-center" value="ltc1q5d4u366xef336pjvccn7akn02upavmk45fhtdw" />
                                    <br>
									<small>TON (ERC20):</small>
									<br>
									<input type="text" class="form-control text-center" value="0x2A72777912A15A6387a1116f9bDDFe1Cb9474BF1" />
                                </div>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-default" data-dismiss="modal">حله</button>
                            </div>
                        </div>
                    </div>
                </div>
                <footer>
                    <p class="text-center">
                        © توسط
                        <a href="https://github.com/ircfspace/tconfig" target="_blank">IRCF</a>،
                        به کمک
                        <a href="https://github.com/yebekhe/ConfigCollector" target="_blank">YeBeKhe</a>
                    </p>
                    <div class="text-center">
                        <a href="#" class="btn btn-link btn-normal btn-lg btn-outline donateLink" data-toggle="modal" data-target="#donate">☕</a>
                    </div>
                </footer>
            </div>
        </div>
    </body>
</html>
