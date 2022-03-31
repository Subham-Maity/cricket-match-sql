```sql

Match Tables:

create table Match_18 (
 MatchID varchar(20),
 Team1 varchar(20),
Team2 varchar(20),
Ground varchar(20),
mdate DATE,
Winner varchar(20),
primary key (MatchID));
SQL> desc match_18;
 Name                                      Null?    Type
 ----------------------------------------- -------- ----------------------------
 MATCHID                                   NOT NULL VARCHAR2(20)
 TEAM1                                              VARCHAR2(20)
 TEAM2                                              VARCHAR2(20)
 GROUND                                             VARCHAR2(20)
 MDATE                                              DATE
 WINNER                                             VARCHAR2(20)




create table Player_18 (
 PlayerID varchar(20),
LName varchar(20),
FName varchar(20),
Country varchar(20),
YBorn number,
BPlace varchar(20),
FTest number,
primary key (PlayerID));
SQL> desc Player_18;
 Name                                      Null?    Type
 ----------------------------------------- -------- ----------------------------
 PLAYERID                                  NOT NULL VARCHAR2(20)
 LNAME                                              VARCHAR2(20)
 FNAME                                              VARCHAR2(20)
 COUNTRY                                            VARCHAR2(20)
 YBORN                                              NUMBER
 BPLACE                                             VARCHAR2(20)
 FTEST                                              NUMBER

SQL>






create table Batting_18(
MatchID varchar(20),
 PlayerID varchar(20),
BOrder number ,
HOut varchar(20),
FOW varchar(20),
NRuns number ,
Mts number,
Nballs number,
Fours number,
Six number,
FOREIGN KEY (MatchID) REFERENCES Match_18(MatchID),
FOREIGN KEY ( PlayerID) REFERENCES Player_18(PlayerID));
SQL> desc batting_18;
 Name                                      Null?    Type
 ----------------------------------------- -------- ----------------------------
 MATCHID                                            VARCHAR2(20)
 PLAYERID                                           VARCHAR2(20)
 BORDER                                             NUMBER
 HOUT                                               VARCHAR2(20)
 FOW                                                VARCHAR2(20)
 NRUNS                                              NUMBER
 MTS                                                NUMBER
 NBALLS                                             NUMBER
 FOURS                                              NUMBER
 SIX                                                NUMBER





create table Bowling_18(
MatchID varchar(20),
 PlayerID varchar(20),
NOvers number,
Maidens number,
NRuns number ,
NWickets number,
FOREIGN KEY (MatchID) REFERENCES Match_18(MatchID),
FOREIGN KEY ( PlayerID) REFERENCES Player_18(PlayerID));
SQL> desc bowling_18;
 Name                                      Null?    Type
 ----------------------------------------- -------- ----------------------------
 MATCHID                                            VARCHAR2(20)
 PLAYERID                                           VARCHAR2(20)
 NOVERS                                             NUMBER
 MAIDENS                                            NUMBER
 NRUNS                                              NUMBER
 NWICKETS                                           NUMBER



value Insert in match_18:

insert into Match_18 values ('2324','Pakistan','India','Peshawar','06-feb-2006','Team1');
insert into Match_18 values ('2327','Pakistan','India','Rawalpindi','11-feb-2006','Team2');
insert into Match_18 values ('2357','India','England','Delhi','28-mar-2006','Team1');
insert into Match_18 values ('2377','west Indies','India','Kingston','18-may-2006','Team2');
insert into Match_18 values ('2404a','Srilanka','India','Colombo','16-aug-2006','abandoned');
insert into Match_18 values ('2440','India','Australia','Mohali','29-oct-2006','Team2');
insert into Match_18 values ('2449','South Africa','India','Cape Town','26-nov-2006','Team1');
insert into Match_18 values ('2480','India','west indies','Nagpur','21-jan-2007','Team1');
insert into Match_18 values ('2493','India','west indies','vadodam','31-jan-2007','Team1');
insert into Match_18 values ('2520','India','srilanka','Rajkot','11-feb-2007','Team2');
insert into Match_18 values ('2611','England','India','southampior','21-aug-2007','Team1');
insert into Match_18 values ('2632','India','Australia','Mumbai','17-oct-2007','Team1');
insert into Match_18 values ('2643','India','Pakistan','Gowahati','3-nov-2007','Team1');
insert into Match_18 values ('2675','Australia','India','Melbourne','10-feb-2008','Team2');
insert into Match_18 values ('2681','India','Sri lanka','Adelade','19-feb-2008','Team1');
insert into Match_18 values ('2688','Australia','India','Sydney','2-mar-2008','Team2');
insert into Match_18 values ('2689','Australia','India','Brisbane','4-mar-2008','Team2');
insert into Match_18 values ('2717','pakistan','India','Karachi','26-feb-2008','Team2');
insert into Match_18 values ('2750','Srilanka','India','Colombo','24-aug-2008','Team2');
insert into Match_18 values ('2755','Srilanka','India','Colombo','27-aug-2008','Team2');








SQL> SELECT * FROM Match_18
  2
SQL>
SQL> SELECT * FROM Match_18;

MATCHID              TEAM1                TEAM2
-------------------- -------------------- --------------------
GROUND               MDATE     WINNER
-------------------- --------- --------------------
2324                 Pakistan             India
Peshawar             06-FEB-06 Team1

2327                 Pakistan             India
Rawalpindi           11-FEB-06 Team2

2357                 India                England
Delhi                28-MAR-06 Team1


MATCHID              TEAM1                TEAM2
-------------------- -------------------- --------------------
GROUND               MDATE     WINNER
-------------------- --------- --------------------
2377                 west Indies          India
Kingston             18-MAY-06 Team2

2404a                Srilanka             India
Colombo              16-AUG-06 abandoned

2440                 India                Australia
Mohali               29-OCT-06 Team2


MATCHID              TEAM1                TEAM2
-------------------- -------------------- --------------------
GROUND               MDATE     WINNER
-------------------- --------- --------------------
2449                 South Africa         India
Cape Town            26-NOV-06 Team1

2480                 India                west indies
Nagpur               21-JAN-07 Team1

2493                 India                west indies
vadodam              31-JAN-07 Team1


MATCHID              TEAM1                TEAM2
-------------------- -------------------- --------------------
GROUND               MDATE     WINNER
-------------------- --------- --------------------
2520                 India                srilanka
Rajkot               11-FEB-07 Team2

2611                 England              India
southampior          21-AUG-07 Team1

2632                 India                Australia
Mumbai               17-OCT-07 Team1


MATCHID              TEAM1                TEAM2
-------------------- -------------------- --------------------
GROUND               MDATE     WINNER
-------------------- --------- --------------------
2643                 India                Pakistan
Gowahati             03-NOV-07 Team1

2675                 Australia            India
Melbourne            10-FEB-08 Team2

2681                 India                Sri lanka
Adelade              19-FEB-08 Team1


MATCHID              TEAM1                TEAM2
-------------------- -------------------- --------------------
GROUND               MDATE     WINNER
-------------------- --------- --------------------
2688                 Australia            India
Sydney               02-MAR-08 Team2

2689                 Australia            India
Brisbane             04-MAR-08 Team2

2717                 pakistan             India
Karachi              26-FEB-08 Team2


MATCHID              TEAM1                TEAM2
-------------------- -------------------- --------------------
GROUND               MDATE     WINNER
-------------------- --------- --------------------
2750                 Srilanka             India
Colombo              24-AUG-08 Team2

2755                 Srilanka             India
Colombo              27-AUG-08 Team2








                                                              value insert in Player_18 table:

insert into Player_18 values ('89001','Tendulkar','Sachin','India',1973,'Mumbai',1989);
insert into Player_18 values ('90001','Lara','Brian','West Indies',1969,'Santa cruz',1990);
insert into Player_18 values ('95001','Ponting','Ricky','Australia',1974,'launeeston',1995);
insert into Player_18 values ('96001','Dravid','Rahul','India',1973,'Indore',1996);
insert into Player_18 values ('96002','gibbs','herschelle','south africa',1974,'cape town',1996);
insert into Player_18 values ('92001','warne','shane','Australia',1969,'melbourne',1992);
insert into Player_18 values ('95002','pollock','shaun','south africa',1973,'port elizabeth',1995);
insert into Player_18 values ('99003','vaughan','michael','England',1974,'Manchester',1999);
insert into Player_18 values ('92003','Ut Huq','Inzaman','pakistan',1970,'Multan',1992);
insert into Player_18 values ('94004','Fleming','Stephen','New Zealand',1973,'christcharch',1994);
insert into Player_18 values ('93002','streak','Health','Zimbabwe',1974,'Bulawayo',1993);
insert into Player_18 values ('90002','Kumble','Anil','India',1970,'Bangalore',1990);
insert into Player_18 values ('93003','Kristen','Gary','south africa',1967,'cape town',1993);
insert into Player_18 values ('95003','Kallis','jacques','south africa',1975,'cape town',1995);
insert into Player_18 values ('94002','Vass','Chamunda','sri lanka',1974,'Maltumagala',1994);
insert into Player_18 values ('92002','muralitharan','muthiah','sri lanka',1972,'kandy',1992);
insert into Player_18 values ('97004','vetori','Daniel','New zealand',1979,'auckland',1997);
insert into Player_18 values ('25001','Dhoni','MS','India',1981,'Ranchi',2005);
insert into Player_18 values ('23001','singh','yuvraj','India',1981,'chandigarh',2003);
insert into Player_18 values ('96003','ganguly','sourav','India',1972,'calcutta',1996);
insert into Player_18 values ('99002','gilchrist','adam','australia',1971,'bellirgen',1999);
insert into Player_18 values ('24001','sumonds','andrew','australia',1975,'Brimingham',2004);
insert into Player_18 values ('99001','Lee','Brett','australia',1976,'wallongong',1999);
insert into Player_18 values ('91001','jayasuriya','sanath','srilanka',1969,'matara',1991);
insert into Player_18 values ('21001','sehwag','virender','india',1978,'delhi',2001);
insert into Player_18 values ('98001','afridi','shahid','pakistan',1980,'khyber agency',1998);
insert into Player_18 values ('98002','singh','harbhajan','india',1980,'jalandhar',1998);
insert into Player_18 values ('27001','kumar','praveen','india',1986,'meerut',Null);
insert into Player_18 values ('27002','sharma','ishant','india',1988,'delhi',2007);






SQL> SELECT * FROM Player_18;

PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
89001                Tendulkar            Sachin
India                      1973 Mumbai                     1989

90001                Lara                 Brian
West Indies                1969 Santa cruz                 1990

95001                Ponting              Ricky
Australia                  1974 launeeston                 1995


PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
96001                Dravid               Rahul
India                      1973 Indore                     1996

96002                gibbs                herschelle
south africa               1974 cape town                  1996

92001                warne                shane
Australia                  1969 melbourne                  1992


PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
95002                pollock              shaun
south africa               1973 port elizabeth             1995

99003                vaughan              michael
England                    1974 Manchester                 1999

92003                Ut Huq               Inzaman
pakistan                   1970 Multan                     1992


PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
94004                Fleming              Stephen
New Zealand                1973 christcharch               1994

93002                streak               Health
Zimbabwe                   1974 Bulawayo                   1993

90002                Kumble               Anil
India                      1970 Bangalore                  1990


PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
93003                Kristen              Gary
south africa               1967 cape town                  1993

95003                Kallis               jacques
south africa               1975 cape town                  1995

94002                Vass                 Chamunda
sri lanka                  1974 Maltumagala                1994


PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
92002                muralitharan         muthiah
sri lanka                  1972 kandy                      1992

97004                vetori               Daniel
New zealand                1979 auckland                   1997

25001                Dhoni                MS
India                      1981 Ranchi                     2005


PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
23001                singh                yuvraj
India                      1981 chandigarh                 2003

96003                ganguly              sourav
India                      1972 calcutta                   1996

99002                gilchrist            adam
australia                  1971 bellirgen                  1999


PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
24001                sumonds              andrew
australia                  1975 Brimingham                 2004

99001                Lee                  Brett
australia                  1976 wallongong                 1999

91001                jayasuriya           sanath
srilanka                   1969 matara                     1991


PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
21001                sehwag               virender
india                      1978 delhi                      2001

98001                afridi               shahid
pakistan                   1980 khyber agency              1998

98002                singh                harbhajan
india                      1980 jalandhar                  1998


PLAYERID             LNAME                FNAME
-------------------- -------------------- --------------------
COUNTRY                   YBORN BPLACE                    FTEST
-------------------- ---------- -------------------- ----------
27001                kumar                praveen
india                      1986 meerut

27002                sharma               ishant
india                      1988 delhi                      2007



                                                values in batting_18 tables:

insert into Batting_18 values ('2755','23001',3,'C','51',0,12,6,0,0);
insert into Batting_18 values ('2755','25001',5,'C','232',71,104,80,4,0);
insert into Batting_18 values ('2755','91001',1,'C','74',60,85,52,8,2);
insert into Batting_18 values ('2755','94002',7,'LBW','157',17,23,29,1,0);
insert into Batting_18 values ('2755','92002',11,'no','no',11,11,7,0,0);
insert into Batting_18 values ('2689','89001',2,'c','205',91,176,121,7,0);
insert into Batting_18 values ('2689','23001',4,'c','175',38,27,38,2,2);
insert into Batting_18 values ('2689','25001',5,'c','240',36,52,37,2,1);
insert into Batting_18 values ('2689','99002',1,'c','2',2,3,3,0,0);
insert into Batting_18 values ('2689','95001',3,'c','8',4,9,7,0,0);
insert into Batting_18 values ('2689','24001',5,'c','123',42,81,56,2,1);
insert into Batting_18 values ('2689','99001',8,'b','228',7,20,12,0,0);
insert into Batting_18 values ('2689','27001',9,'c','255',7,7,7,1,0);
insert into Batting_18 values ('2755','27001',9,'b','257',2,7,6,0,0);
insert into Batting_18 values ('2689','98002',8,'LBW','249',3,7,3,0,0);
insert into Batting_18 values ('2755','98002',8,'RO','253',2,7,4,0,0);





SQL> SELECT * FROM Batting_18;

MATCHID              PLAYERID                 BORDER HOUT
-------------------- -------------------- ---------- --------------------
FOW                       NRUNS        MTS     NBALLS      FOURS        SIX
-------------------- ---------- ---------- ---------- ---------- ----------
2755                 23001                         3 C
51                            0         12          6          0          0

2755                 25001                         5 C
232                          71        104         80          4          0

2755                 91001                         1 C
74                           60         85         52          8          2


MATCHID              PLAYERID                 BORDER HOUT
-------------------- -------------------- ---------- --------------------
FOW                       NRUNS        MTS     NBALLS      FOURS        SIX
-------------------- ---------- ---------- ---------- ---------- ----------
2755                 94002                         7 LBW
157                          17         23         29          1          0

2755                 92002                        11 no
no                           11         11          7          0          0

2689                 89001                         2 c
205                          91        176        121          7          0


MATCHID              PLAYERID                 BORDER HOUT
-------------------- -------------------- ---------- --------------------
FOW                       NRUNS        MTS     NBALLS      FOURS        SIX
-------------------- ---------- ---------- ---------- ---------- ----------
2689                 23001                         4 c
175                          38         27         38          2          2

2689                 25001                         5 c
240                          36         52         37          2          1

2689                 99002                         1 c
2                             2          3          3          0          0


MATCHID              PLAYERID                 BORDER HOUT
-------------------- -------------------- ---------- --------------------
FOW                       NRUNS        MTS     NBALLS      FOURS        SIX
-------------------- ---------- ---------- ---------- ---------- ----------
2689                 95001                         3 c
8                             4          9          7          0          0

2689                 24001                         5 c
123                          42         81         56          2          1

2689                 99001                         8 b
228                           7         20         12          0          0


MATCHID              PLAYERID                 BORDER HOUT
-------------------- -------------------- ---------- --------------------
FOW                       NRUNS        MTS     NBALLS      FOURS        SIX
-------------------- ---------- ---------- ---------- ---------- ----------
2689                 27001                         9 c
255                           7          7          7          1          0

2755                 27001                         9 b
257                           2          7          6          0          0

2689                 98002                         8 LBW
249                           3          7          3          0          0


MATCHID              PLAYERID                 BORDER HOUT
-------------------- -------------------- ---------- --------------------
FOW                       NRUNS        MTS     NBALLS      FOURS        SIX
-------------------- ---------- ---------- ---------- ---------- ----------
2755                 98002                         8 RO
253



   insert values bowling_18:
insert into Bowling_18 values('2689','99001',10,0,58,1);
insert into Bowling_18 values('2689','24001',3,0,27,1);
insert into Bowling_18 values('2689','23001',3,0,15,0);
insert into Bowling_18 values('2755','94002',9,1,40,1);
insert into Bowling_18 values('2755','92002',10,0,56,1);
insert into Bowling_18 values('2755','91001',4,0,29,0);
insert into Bowling_18 values('2755','23001',10,0,53,2);
insert into Bowling_18 values('2755','98002',10,0,40,3);
insert into Bowling_18 values('2689','98002',10,0,41,1);






SQL> SELECT * FROM bowling_18;

MATCHID              PLAYERID                 NOVERS    MAIDENS      NRUNS
-------------------- -------------------- ---------- ---------- ----------
  NWICKETS
----------
2689                 24001                         3          0         27
         1

2689                 23001                         3          0         15
         0

2755                 94002                         9          1         40
         1


MATCHID              PLAYERID                 NOVERS    MAIDENS      NRUNS
-------------------- -------------------- ---------- ---------- ----------
  NWICKETS
----------
2755                 92002                        10          0         56
         1

2755                 91001                         4          0         29
         0

2755                 23001                        10          0         53
         2


MATCHID              PLAYERID                 NOVERS    MAIDENS      NRUNS
-------------------- -------------------- ---------- ---------- ----------
  NWICKETS
----------
2755                 98002                        10          0         40
         3

2689                 98002                        10          0         41
         1

```