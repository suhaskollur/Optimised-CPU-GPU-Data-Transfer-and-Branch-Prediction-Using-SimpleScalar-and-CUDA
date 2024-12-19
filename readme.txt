Needs to be implemented in a Linux-based Environment: Ubuntu (preferred)

necessary files:
all the simplescalar files
code changes in:
bpred.h -> defined necessary structures for predictors
bpred.c -> predictor logic, lookup and update.
sim-outorder.c -> integration of diff predictors.

commands used for running Branch Prediction with simplescalar:
git clone https://github.com/simplescalar/simplescalar.git
cd final/simplescalar

Alpha:
make clean
make config-alpha
make

Pisa:
make clean
make config-alpha
make

anagram:
alpha Not Taken:
./sim-bpred -bpred nottaken -redir:sim nottakenoutanagram.txt /home/rufusm/final/simplesim/tests-alpha/bin/anagram 
Pisa Not taken:
./sim-bpred -bpred nottaken -redir:sim nottakenoutanagram.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/anagram
alpha Taken:
./sim-bpred -bpred taken -redir:sim nottakenoutanagram.txt /home/rufusm/final/simplesim/tests-alpha/bin/anagram 
Pisa Taken:
./sim-bpred -bpred taken -redir:sim nottakenoutanagram.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/anagram
alpha Bimod:
./sim-bpred -bpred bimod -bpred:btb 256 4 -redir:sim bimodoutanagram.txt /home/rufusm/final/simplesim/tests-alpha/bin/anagram
Pisa Bimod:
./sim-bpred -bpred bimod -bpred:btb 256 4 -redir:sim bimodoutanagram.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/anagram
alpha 2level:
./sim-bpred -bpred:2lev 2048 8192 16 1 -redir:sim 2levoutanagram.txt /home/rufusm/final/simplesim/tests-alpha/bin/anagram
Pisa 2level:
./sim-bpred -bpred:2lev 2048 8192 16 1 -redir:sim 2levoutanagram.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/anagram
Alpha comb:
./sim-bpred -bpred comb -bpred:btb 256 4 -bpred:2lev 2048 8192 16 1 -redir:sim comboutanagram.txt /home/rufusm/final/simplesim/tests-alpha/bin/anagram
Pisa comb:
./sim-bpred -bpred comb -bpred:btb 256 4 -bpred:2lev 2048 8192 16 1 /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/anagram
Alpha percept:
./sim-outorder -bpred percept -redir:sim alphaperceptoutanagram.txt /home/rufusm/final/simplesim/tests-alpha/bin/anagram 
Pisa percept:
./sim-outorder -bpred percept -redir:sim alphaperceptoutanagram.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/anagram
Alpha gehl:
./sim-outorder -bpred gehl -redir:sim alphagehloutanagram.txt /home/rufusm/final/simplesim/tests-alpha/bin/anagram
Pisa gehl:
./sim-outorder -bpred gehl -redir:sim alphagehloutanagram.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/anagram

test-llong:
alpha Not Taken:
./sim-bpred -bpred nottaken -redir:sim nottakenouttestllong.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-llong 
Pisa Not taken:
./sim-bpred -bpred nottaken -redir:sim nottakenouttestllong.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-llong
alpha Taken:
./sim-bpred -bpred taken -redir:sim nottakenouttestllong.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-llong 
Pisa Taken:
./sim-bpred -bpred taken -redir:sim nottakenouttestllong.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-llong
alpha Bimod:
./sim-bpred -bpred bimod -bpred:btb 256 4 -redir:sim bimodtestllong.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-llong
Pisa Bimod:
./sim-bpred -bpred bimod -bpred:btb 256 4 -redir:sim bimodtestllong.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-llong
alpha 2level:
./sim-bpred -bpred:2lev 2048 8192 16 1 -redir:sim 2levouttestllong.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-llong
Pisa 2level:
./sim-bpred -bpred:2lev 2048 8192 16 1 -redir:sim 2levouttestllong.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-llong
Alpha comb:
./sim-bpred -bpred comb -bpred:btb 256 4 -bpred:2lev 2048 8192 16 1 -redir:sim combouttestllong.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-llong
Pisa comb:
./sim-bpred -bpred comb -bpred:btb 256 4 -bpred:2lev 2048 8192 16 1 /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-llong
Alpha percept:
./sim-outorder -bpred percept -redir:sim alphaperceptouttestllong.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-llong 
Pisa percept:
./sim-outorder -bpred percept -redir:sim alphaperceptouttestllong.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-llong
Alpha gehl:
./sim-outorder -bpred gehl -redir:sim alphagehlouttestllong.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-llong
Pisa gehl:
./sim-outorder -bpred gehl -redir:sim alphagehlouttestllong.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-llong

test-lswlr:
alpha Not Taken:
./sim-bpred -bpred nottaken -redir:sim nottakenouttestlswlr.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-lswlr 
Pisa Not taken:
./sim-bpred -bpred nottaken -redir:sim nottakenouttestlswlr.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-lswlr
alpha Taken:
./sim-bpred -bpred taken -redir:sim nottakenouttestlswlr.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-lswlr 
Pisa Taken:
./sim-bpred -bpred taken -redir:sim nottakenouttestlswlr.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-lswlr
alpha Bimod:
./sim-bpred -bpred bimod -bpred:btb 256 4 -redir:sim bimodtestlswlr.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-lswlr
Pisa Bimod:
./sim-bpred -bpred bimod -bpred:btb 256 4 -redir:sim bimodtestlswlr.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-lswlr
alpha 2level:
./sim-bpred -bpred:2lev 2048 8192 16 1 -redir:sim 2levouttestlswlr.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-lswlr
Pisa 2level:
./sim-bpred -bpred:2lev 2048 8192 16 1 -redir:sim 2levouttestlswlr.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-lswlr
Alpha comb:
./sim-bpred -bpred comb -bpred:btb 256 4 -bpred:2lev 2048 8192 16 1 -redir:sim combouttestlswlr.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-lswlr
Pisa comb:
./sim-bpred -bpred comb -bpred:btb 256 4 -bpred:2lev 2048 8192 16 1 /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-lswlr
Alpha percept:
./sim-outorder -bpred percept -redir:sim alphaperceptouttestlswlr.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-lswlr 
Pisa percept:
./sim-outorder -bpred percept -redir:sim alphaperceptouttestlswlr.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-lswlr
Alpha gehl:
./sim-outorder -bpred gehl -redir:sim alphagehlouttestlswlr.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-lswlr
Pisa gehl:
./sim-outorder -bpred gehl -redir:sim alphagehlouttestlswlr.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-lswlr

test-math
test-math:
alpha Not Taken:
./sim-bpred -bpred nottaken -redir:sim nottakenouttestmath.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-math 
Pisa Not taken:
./sim-bpred -bpred nottaken -redir:sim nottakenouttestmath.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-math
alpha Taken:
./sim-bpred -bpred taken -redir:sim nottakenouttestmath.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-math 
Pisa Taken:
./sim-bpred -bpred taken -redir:sim nottakenouttestmath.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-math
alpha Bimod:
./sim-bpred -bpred bimod -bpred:btb 256 4 -redir:sim bimodtestmath.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-math
Pisa Bimod:
./sim-bpred -bpred bimod -bpred:btb 256 4 -redir:sim bimodtestmath.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-math
alpha 2level:
./sim-bpred -bpred:2lev 2048 8192 16 1 -redir:sim 2levouttestmath.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-math
Pisa 2level:
./sim-bpred -bpred:2lev 2048 8192 16 1 -redir:sim 2levouttestmath.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-math
Alpha comb:
./sim-bpred -bpred comb -bpred:btb 256 4 -bpred:2lev 2048 8192 16 1 -redir:sim combouttestmath.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-math
Pisa comb:
./sim-bpred -bpred comb -bpred:btb 256 4 -bpred:2lev 2048 8192 16 1 /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-math
Alpha percept:
./sim-outorder -bpred percept -redir:sim alphaperceptouttestmath.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-math 
Pisa percept:
./sim-outorder -bpred percept -redir:sim alphaperceptouttestmath.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-math
Alpha gehl:
./sim-outorder -bpred gehl -redir:sim alphagehlouttestmath.txt /home/rufusm/final/simplesim/tests-alpha/bin/test-math
Pisa gehl:
./sim-outorder -bpred gehl -redir:sim alphagehlouttestmath.txt /home/rufusm/projects/simplesim-3.0/tests-pisa/bin.little/test-math