# utl-avoid-klingon-code-create-macro-variable-from-string-with-mismatched-quotes-and-many-commas
Avoid klingon code create macro variable from string with mismatched quotes and many commas
    %let pgm=utl-avoid-klingon-code-create-macro-variable-from-string-with-mismatched-quotes-and-many-commas;

    %stop_submission;

    Avoid klingon code create macro variable from string with mismatched quotes and many commas

    SOAPBOX ON
      I Since you were not able to create the macro result, I supect
      the string existes outside of the macro compiler
    SOAPBOX OFF


    https://communities.sas.com/t5/SAS-Programming/Macro-variable-value-with-single-quote/m-p/765596#M242519

    INPUT

    'CLOSING RUN' INSURANCE','INSURANCE','SECONDARY CLOSING RUN INSURANCE','BUSINESS INSURANCE','RI_BCT'
                 ----------
                unmatched quote

    PROCESS
    =======

    %symdel rep_run / nowarn;

    %let rep_run=%qupcase("'closing run' insurance','insurance','secondary closing run insurance','business insurance','RI_BCT'");

    %put  %qsysfunc(dequote(&rep_run));

    OUTPUT
    ======

    'CLOSING RUN' INSURANCE','INSURANCE','SECONDARY CLOSING RUN INSURANCE','BUSINESS INSURANCE','RI_BCT'

    RELATED REPOS

    https://tinyurl.com/4u8vc4hv
    https://github.com/rogerjdeangelis/utl-creating-the-quoted-sql-like-clause-with-resolved-embedde-macro-variable-reduce-macro-trigger

    Be skeptical (not sure I always deleted persistent macro variables.
    https://github.com/rogerjdeangelis/utl-avoiding-klingon-macro-triggers-at-macro-execution-time
    https://github.com/rogerjdeangelis/utl-macro-klingon-solution-or-simple-dosubl-you-decide
    https://github.com/rogerjdeangelis/utl-using-dosubl-to-avoid-klingon-obsucated-macro-coding
    https://github.com/rogerjdeangelis/utl_using_dosubl_to_avoid_klingon_macro_quoting_functions

    /*              _
      ___ _ __   __| |
     / _ \ `_ \ / _` |
    |  __/ | | | (_| |
     \___|_| |_|\__,_|

    */
