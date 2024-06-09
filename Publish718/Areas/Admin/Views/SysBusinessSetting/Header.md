 <!--Attendance Reports-->
        <li class="nav-item has-treeview">
            @if ((bool)ViewBag.Role_SystemAdmin || (bool)ViewBag.Role_Admin || (bool)ViewBag.Role_MainComOprerator)
            {
                <a href="#" class="nav-link">
                    <i class="fab fa-wpforms nav-icon "></i>
                    <p>
                        工作考勤
                        <i class="fa fa-angle-left right"></i>
                    </p>
                </a>
                <ul class="nav nav-treeview">
                    <li class="nav-item">
                        <a href="@Url.Action("ShiftBrief","AttendanceReports",new { Language =ViewBag.Language,area ="Admin"})" class="nav-link">
                            <i class="fa fa-address-book-o nav-icon "></i>
                            <p> 遲到早退</p>
                        </a>
                    </li> 
                    <li class="nav-item">
                        <a href="@Url.Action("DayStatistics","AttendanceReports",new { Language =ViewBag.Language,area ="Admin"})" class="nav-link">
                            <i class="fas fa-sun nav-icon"></i>
                            <p> 每日統計</p>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="@Url.Action("MonthlyStatistics","AttendanceReports",new { Language =ViewBag.Language,area ="Admin"})" class="nav-link">
                            <i class="fa fa-address-book nav-icon"></i>
                            <p> 每月統計</p>
                        </a>
                    </li>
                </ul>
            }
        </li> 


<!-- Info boxes -->
        <div class="row">
            <div class="col-12 col-sm-6 col-md-3">
                <div class="info-box bg-secondary">
                    @{
                        if (ViewBag.ShiftBusinessMode != 2)
                        {
                            @:<span class="info-box-icon bg-warning-gradient elevation-1 text-white"><i class="fas fa-sun"></i></span>
                            ViewBag.ActionName1 = "ShiftSetting";
                            ViewBag.ActionNameLabel1 = Lang.Shift_DayShiftLabel;
                        }
                        else
                        {
                            @:<span class="info-box-icon bg-dark elevation-1"><i class="fas fa-moon-o"></i></span>
                            ViewBag.ActionName1 = "ShiftSettingNight";
                            ViewBag.ActionNameLabel1 = Lang.Shift_NightSettingLabel;
                        }
                    }
                    <div class="info-box-content">
                        <a href="@Url.Action(ViewBag.ActionName1, "SysBusinessSetting", new { Language = LangUtilities.LanguageCode, area = "Admin",shiftid = ViewBag.ShiftId})" class="info-box-text">@ViewBag.ActionNameLabel1</a>
                        <span class="info-box-number"><small>Main</small></span>
                    </div>
                    <!-- /.info-box-content -->
                </div>
                <!-- /.info-box -->
            </div>
            <!-- /.col -->
            <div class="col-12 col-sm-6 col-md-3">
                <div class="info-box mb-3">
                    <span class="info-box-icon bg-primary elevation-1"><i class="fa fa-coffee"></i></span>

                    <div class="info-box-content">
                        <a href="@Url.Action("ShiftSettingLunch", "SysBusinessSetting", new { Language = LangUtilities.LanguageCode, area = "Admin",shiftid = ViewBag.ShiftId})" class="info-box-text">@Lang.Shift_LunchTimeLabel</a>
                        <span class="info-box-number"><small>Extend Fun 1</small></span>
                    </div>
                    <!-- /.info-box-content -->
                </div>
                <!-- /.info-box -->
            </div>
            <!-- /.col -->
            <!-- fix for small devices only -->
            <div class="clearfix hidden-md-up"></div>

            <div class="col-12 col-sm-6 col-md-3">
                <div class="info-box mb-3">
                    <span class="info-box-icon bg-success elevation-1"><i class="fas fa-fast-forward"></i></span>  <!--fa fa-stack-overflow-->
                    <div class="info-box-content">
                        <a href="@Url.Action("ShiftSettingOverTime", "SysBusinessSetting", new { Language = LangUtilities.LanguageCode, area = "Admin",shiftid = ViewBag.ShiftId})" class="info-box-text">@Lang.Shift_OverTimeLabel</a>
                        <span class="info-box-number"><small>Extend Fun 2</small></span>
                    </div>
                    <!-- /.info-box-content -->
                </div>
                <!-- /.info-box -->
            </div>
            <!-- /.col -->
            <div class="col-12 col-sm-6 col-md-3 ">
                <div class="info-box mb-3">
                    <span class="info-box-icon bg-info-gradient elevation-1"><i class="fa fa-crosshairs"></i></span>

                    <div class="info-box-content">
                        <a href="@Url.Action("ShiftSettingWeekDay", "SysBusinessSetting", new { Language = LangUtilities.LanguageCode, area = "Admin",shiftid = ViewBag.ShiftId})" class="info-box-text">@Lang.Shift_WeekDaySettingLabel</a>
                        <span class="info-box-number"><small>Extend Fun 3</small></span>
                    </div>
                    <!-- /.info-box-content -->
                </div>
                <!-- /.info-box -->
            </div>
            <!-- /.col -->
        </div>









 







