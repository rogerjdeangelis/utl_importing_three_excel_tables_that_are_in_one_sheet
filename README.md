# utl_importing_three_excel_tables_that_are_in_one_sheet
Importing three excel tables that are in one sheet.  Keywords: sas sql join merge big data analytics macros oracle teradata mysql sas communities stackoverflow statistics artificial inteligence AI Python R Java Javascript WPS Matlab SPSS Scala Perl C C# Excel MS Access JSON graphics maps NLP natural language processing machine learning igraph DOSUBL DOW loop stackoverflow SAS community.
    Importing three excel tables that are in one sheet

    github
    https://tinyurl.com/y82mwj6z
    https://github.com/rogerjdeangelis/utl_importing_three_excel_tables_that_are_in_one_sheet

    see
    https://tinyurl.com/y7a4yxh4
    https://communities.sas.com/t5/General-SAS-Programming/Need-to-import-tabular-type-report-in-SAS/m-p/485154

    INPUT
    =====

      d:/xls/utl_threetables.xlsx

      Download the excel file and highlight each 'table' rectangle and
      name the rectangles

       BOXA3J8     -> Table 1 Box starts at A3 and ends at J8
       BOXA10J15   -> Table 2 Box starts at A10 and ends at J15
       BOXL2O30    -> Table 3 Box starts at L2 and ends at O30


       This what proc contents tells us
       libname xel "d:/xls/utl_threetables.xlsx";

       proc contents data=xel._all_;
       run;quit;
                                      DBMS
                  Member              Member
       Name       Type   Vars  Label  Type

       BOXA3J8    DATA    10          TABLE
       BOXA10J15  DATA    10          TABLE
       BOXL2O30   DATA     4          TABLE


    PROCESS
    =======

       libname xel "d:/xls/utl_threetables.xlsx";

       data table_1;
         set xel.BOXA3J8;
       run;quit;

       data table_2;
         set xel.BOXA10J15;
       run;quit;

       data table_3;
         set xel.BOXL2O30;
       run;quit;


    OUTPUT
    ======

    WORK.TABLE_1 total obs=5
    ------------------------

                     PRODUCT_
      PRODUCT_ID     STR_           METRIC     __6_15    __13_15    __20_15    __27_15     __3_15    __10_15    __17_15

      GRP54181578    PEN ML          TRX      0.00000    0.00000    10.0000    6.00000    6.75000    5.59006    6.00000
      GRP79861172    2 PEN ML        TRX      8.28185    8.61818     8.2383    8.06937    6.19086    6.50368    5.10458
      GRP54181569    SYR DV ML       TRX      0.00000    0.00000     9.5000    0.00000    0.00000    0.00000    8.00000
      GRP79861237    2 SYR DV ML     TRX      0.00000    7.33333     6.9091    7.33333    6.14915    6.14124    5.57143
                     Total           TRX      9.06757    8.49180     8.1000    7.83726    6.20217    6.41738    5.24045


    WORK.TABLE_2 total obs=5
    ------------------------

                      PRODUCT_
       PRODUCT_ID     STR_           METRIC     __6_15    __13_15    __20_15    __27_15     __3_15    __10_15    __17_15

      GRP054085785    PEN ML          NRX      11.0000    0.00000    10.0000    6.00000    6.75000    5.59006    6.00000
      GRP079080672    2 PEN ML        NRX       8.2819    8.61818     8.2383    8.16122    6.21521    6.57131    5.30769
      GRP054085694    SYR DV ML       NRX       0.0000    0.00000     9.5000    0.00000    0.00000    0.00000    8.00000
      GRP079080623    2 SYR DV ML     NRX       0.0000    7.33333     6.9091    7.50000    6.14915    6.14124    5.57143
                      Total           NRX       8.4631    8.49180     8.1000    7.93152    6.22369    6.47042    5.42069

    WORK.TABLE_3 total obs=28
    -------------------------
                             PRODUCT_       WEEKLY_
       METRIC     METRIC1    STR_           FACTORS

      20154.00      TRX      PEN ML          0.0000
      20161.00      TRX      PEN ML          0.0000
      20168.00      TRX      PEN ML         10.0000
      20175.00      TRX      PEN ML          6.0000
      20182.00      TRX      PEN ML          6.7500
      20189.00      TRX      PEN ML          5.5901
      20196.00      TRX      PEN ML          6.0000
      20154.00      TRX      2 PEN ML        8.2819

    *                _               _       _
     _ __ ___   __ _| | _____     __| | __ _| |_ __ _
    | '_ ` _ \ / _` | |/ / _ \   / _` |/ _` | __/ _` |
    | | | | | | (_| |   <  __/  | (_| | (_| | || (_| |
    |_| |_| |_|\__,_|_|\_\___|   \__,_|\__,_|\__\__,_|

    ;


      d:/xls/utl_threetables.xlsx

      Download the excel file and highlight each 'table' rectangle and
      name the rectangles

       BOXA3J8     -> Table 1 Box starts at A3 and ends at J8
       BOXA10J15   -> Table 2 Box starts at A10 and ends at J15
       BOXL2O30    -> Table 3 Box starts at L2 and ends at O30

    *          _       _   _
     ___  ___ | |_   _| |_(_) ___  _ __
    / __|/ _ \| | | | | __| |/ _ \| '_ \
    \__ \ (_) | | |_| | |_| | (_) | | | |
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|

    ;
    see process

