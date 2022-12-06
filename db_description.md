Table:- `candidate`
attributes:-  `CandidateID`, `abc`, `Position`, `Party`, `FirstName`, `LastName`, `MiddleName`, `Gender`, `Year`, `Photo`
pk:- `CandidateID`


INSERT INTO `candidate` (`CandidateID`, `abc`, `Position`, `Party`, `FirstName`, `LastName`, `MiddleName`, `Gender`, `Year`, `Photo`) VALUES
(101, 'c', '1st Year Representative', 'Pig Party', 'Raphael Victor', 'Combate', 'Romarate', 'Male', '1st year', 'upload/photo0317.jpg'),
(102, 'c', '1st Year Representative', 'Horse Party', 'Mary Ver', 'Pamposa', 'Libo-on', 'FeMale', '1st year', 'upload/photo0900.jpg');





Table:- `history`
attributes:- `history_id`, `data`, `action`, `date`, `user`
pk:- `history_id`

INSERT INTO `history` (`history_id`, `data`, `action`, `date`, `user`) VALUES
(568, 'john kevin lorayna', 'Login', '2012-11-08 09:46:23', 'admin'),
(567, 'john kevin lorayna', 'Logout', '2012-11-08 09:45:59', 'admin'),





Table:- `users`
attributes:-`User_id`, `FirstName`, `LastName`, `UserName`, `Password`, `User_Type`
pk:- `User_id`
fk:- `CandidateID`


INSERT INTO `users` (`User_id`, `FirstName`, `LastName`, `UserName`, `Password`, `User_Type`) VALUES
(2, 'john kevin', 'lorayna', 'admin', 'admin', 'admin'),
(5, 'john kevin', 'lorayna', 'jkev', 'jkev', 'Admin');



Table:- `voters`
attributes:- `VoterID`, `FirstName`, `LastName`, `MiddleName`, `Username`, `Password`, `Year`, `Status`
pk:- `VoterID`

INSERT INTO `voters` (`VoterID`, `FirstName`, `LastName`, `MiddleName`, `Username`, `Password`, `Year`, `Status`) VALUES
(24, 'Maricon', 'Itona', 'M.', '20100333', 'concon', '1st year', 'Voted'),
(23, 'Raphael Victor', 'Combate', 'R.', '20100222', 'raprap', '1st year', 'Unvoted');


Table:-`votes`
attributes:- `ID`, `CandidateID`, `votes`
pk:- `ID`



INSERT INTO `votes` (`ID`, `CandidateID`, `votes`) VALUES
(205, 0, 0),
(204, 0, 0);
