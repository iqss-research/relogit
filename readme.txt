
                                 RELOGIT
                     Rare Event Logistic Regression
                     Version 1.1.1, October 28, 1999

                               Michael Tomz
                         Department of Government
                            Harvard University
                           tomz@fas.harvard.edu

                Gary King                     Langche Zeng
         Department of Government                 CBRSS
            Harvard University             Harvard University
             king@harvard.edu        langche@everest.fas.harvard.edu



 1. What is RELOGIT?

    RELOGIT is a suite of programs for estimating and interpreting
    logit results when the sample is unbalanced (one outcome is rarer
    than the other) or has been selected by a rule correlated with the
    dependent variable.  RELOGIT estimates the same logit model as the
    -logit- command, but with an estimator that give lower mean square
    error in the presence of rare events data for coefficients,
    probabilities, and other quantities of interest. The program,
    designed for use with the Stata statistics package, offers a
    convenient way to implement the procedures suggested in

       Gary King and Langche Zeng. 1999a. "Logistic Regression in Rare
       Events Data," Department of Government, Harvard University,
       available from http://GKing.Harvard.Edu.

       and

       Gary King and Langche Zeng. 1999b. "Estimating Absolute, Relative,
       and Attributable Risks in Case-Control Studies," Department of
       Government, Harvard University, available from
       http://GKing.Harvard.Edu.


 2. Software requirements

    RELOGIT works in conjunction with "Stata Statistical Software: Release
    6.0," produced by Stata Corporation.  You must have Stata 6.0 to run
    RELOGIT.  To obtain a copy of Stata or learn more about the software,
    visit http://www.stata.com or send email to stata@stata.com


 3. Files included in RELOGIT
                      
    The RELOGIT package contains seveh main files.  Please verify that you
    have all seven before installing the software.  The files are:
  
       relogit.ado   
       relogit.hlp   
       setx.ado      
       setx.hlp      
       setxHL.ado
       relogitq.ado     
       relogitq.hlp


 4. How to install RELOGIT

    To install RELOGIT, launch Stata and then type

          sysdir

    at the command prompt.  If you are running Stata for Windows, you
    should see a message that looks something like this:

           STATA:  C:\STATA\
         UPDATES:  C:\STATA\ado\updates\
            BASE:  C:\STATA\ado\base\
            SITE:  C:\STATA\ado\site\
         STBPLUS:  c:\ado\stbplus\
        PERSONAL:  c:\ado\personal\
        OLDPLACE:  c:\ado\

    Users of Stata for UNIX will see a message that looks something like
    this:

           STATA:  /usr/local/stata/
         UPDATES:  /usr/local/stata/ado/updates/
            BASE:  /usr/local/stata/ado/base/
            SITE:  /usr/local/ado/
         STBPLUS:  ~/ado/stbplus/
        PERSONAL:  ~/ado/personal/
        OLDPLACE:  ~/ado/            

    If RELOGIT is strictly for your own use, copy all files to the STBPLUS
    directory listed on your screen.  In this example, the directory is
    c:\ado\stbplus under Windows and ~/ado/stbplus/ under UNIX.  If, on the
    other hand, you are a site administrator who wants to share RELOGIT with
    other users on your network, copy all files to the SITE directory.  In
    some cases the STBPLUS and SITE directories may not yet exist on your
    computer.  For those cases, please use your operating system to create
    the directory  that will hold the files.


 5. How to use RELOGIT

    The three main commands in RELOGIT are

       relogit   (estimates logit coefficients and corrects for
                  rare events and selection on the dependent variable)
       setx      (sets values of Xs before calculating quantities of
                  interest)
       relogitq  (improved methods of computing quantities of interest,
                  such as probabilities, first differences and relative
                  risks)

    In general, the commands should be run in the order given,
    although it is often useful to call setx and relogitq many times
    after running relogit.

    Each command comes with an on-line help file.  To read the on-line
    help for relogit, click "Help" in the Stata menu bar and select
    "Stata Command," which causes the Stata command dialog box to appear.
    Type the name of the RELOGIT command (such as relogit) in the blank
    and then click the "OK" button.  An on-line help file will appear on
    the screen.  Alternatively, type "help relogit" at the command line.


 6. How to cite this software

    If you use this software, please cite

       Michael Tomz, Gary King, and Langche Zeng. 1999.  RELOGIT:
       Rare Events Logistic Regression, Version 1.1  Cambridge,
       MA: Harvard University, October 1, http://gking.harvard.edu/

    and the following two papers

       Gary King and Langche Zeng. 1999a. "Logistic Regression in Rare
       Events Data," Department of Government, Harvard University,
       https://gking.harvard.edu/files/abs/0s-abs.shtml.

       Gary King and Langche Zeng. 1999b. "Estimating Absolute, Relative,
       and Attributable Risks in Case-Control Studies," Department of
       Government, Harvard University, available from
       https://gking.harvard.edu/files/abs/1s-abs.shtml.


 7. Where to obtain updates

    The current version of RELOGIT is available on this github and at SSC.

 8. Sharing this program with others

    RELOGIT is (C) Copyright, 1999, Michael Tomz, Gary King and Langche
    Zeng, All Rights Reserved.  You may copy and distribute this program
    provided no charge is made and the copy is identical to the original.
    To request an exception, please contact Michael Tomz.

    We recommend that you distribute the most recent version of RELOGIT.


 9. Questions and comments

    Questions and comments about RELOGIT should be directed to Michael
    Tomz, Department of Government, Harvard University, Littauer Center
    North Yard, Cambridge, MA 02138.  email : tomz@fas.harvard.edu


10. Acknowledgements

    Parts of this program are borrowed from "CLARIFY: Software for
    Interpreting and Presenting Statistical Results," (C) Michael Tomz,
    Jason Wittenberg and Gary King.  The -relogitq- command uses an
    updated version of a parsing procedure that was developed by Jeroen
    Weesie, "Parsing Options with Embedded Parentheses," Stata Technical
    Bulletin 40 (Nov 1997), insert ip22.
