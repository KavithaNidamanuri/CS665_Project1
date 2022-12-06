SELECT * FROM candidate;


SELECT * FROM history;

SELECT * FROM users;

SELECT * FROM voters;

SELECT * FROM votes;






--
-- Dumping data for table `candidate`
--

INSERT INTO `candidate` (`CandidateID`, `abc`, `Position`, `Party`, `FirstName`, `LastName`, `MiddleName`, `Gender`, `Year`, `Photo`) VALUES
(101, 'c', '1st Year Representative', 'Pig Party', 'Raphael Victor', 'Combate', 'Romarate', 'Male', '1st year', 'upload/photo0317.jpg'),
(102, 'c', '1st Year Representative', 'Horse Party', 'Mary Ver', 'Pamposa', 'Libo-on', 'FeMale', '1st year', 'upload/photo0900.jpg'),
(103, 'c', '1st Year Representative', 'Pig Party', 'Rowan Jennele', 'Villamor', 'Totot', 'FeMale', '1st year', 'upload/2012-10-13 16.37.13.jpg'),
(100, 'e', '3rd Year Representative', 'Horse Party', 'Achilles', 'Palma', 'wla', 'Male', '3rd year', 'upload/539324_3623195908310_933066000_n.jpg'),
(137, 'c', '1st Year Representative', 'Horse Party', 'Jeza Marie', 'Telmoso', 'Agbay', 'FeMale', '1st year', 'upload/2012-10-13 16.38.18.jpg'),
(136, 'c', '1st Year Representative', 'Horse Party', 'Ailyn', 'Tanaleon', 'Labos', 'FeMale', '1st year', 'upload/2012-10-13 16.37.36.jpg'),
(158, 'f', '3rd Year Representative', 'Pig Party', 'Michael', 'Jomero', 'Dert', 'Male', '3rd year', 'upload/1.jpg'),
(159, 'e', '3rd Year Representative', 'Pig Party', 'Cristine', 'Yanson', 'Poo', 'FeMale', '3rd year', 'upload/312212_286103561418274_100000558960309_1109905_270256889_n.jpg'),
(186, 'f', '4th Year Representative', 'Pig Party', 'Gerald', 'Anderson', 'Ferrera', 'Male', '4th year', 'upload/black-abstract-windows7-seven-desktop-wallpaper-1600x1200.jpg'),
(190, 'a', 'Governor', 'party2x', 'Sherwin', 'Laylon', 'Deres', 'Male', '3rd year', 'upload/293896_417785301600923_1313159027_n.jpg');

-- --------------------------------------------------------


--
-- Dumping data for table `history`
--

INSERT INTO `history` (`history_id`, `data`, `action`, `date`, `user`) VALUES
(568, 'john kevin lorayna', 'Login', '2012-11-08 09:46:23', 'admin'),
(567, 'john kevin lorayna', 'Logout', '2012-11-08 09:45:59', 'admin'),
(566, 'john kevin lorayna', 'Login', '2012-11-08 09:44:41', 'admin'),
(565, 'john kevin lorayna', 'Login', '2012-11-03 20:24:08', 'admin'),
(564, 'Achilles Palma', 'Deleted Voter', '10/25/2012 11:1:39', 'admin'),
(563, 'john kevin lorayna', 'Login', '2012-10-25 10:48:40', 'admin');

-- --------------------------------------------------------
--
-- Dumping data for table `users`
--

INSERT INTO `users` (`User_id`, `FirstName`, `LastName`, `UserName`, `Password`, `User_Type`) VALUES
(2, 'john kevin', 'lorayna', 'admin', 'admin', 'admin'),
(5, 'john kevin', 'lorayna', 'jkev', 'jkev', 'Admin'),
(4, 'Stephnanie', 'Villanueva', 'teph', 'teph', 'Admin');

-- --------------------------------------------------------



--
-- Dumping data for table `voters`
--

INSERT INTO `voters` (`VoterID`, `FirstName`, `LastName`, `MiddleName`, `Username`, `Password`, `Year`, `Status`) VALUES
(24, 'Maricon', 'Itona', 'M.', '20100333', 'concon', '1st year', 'Voted'),
(23, 'Raphael Victor', 'Combate', 'R.', '20100222', 'raprap', '1st year', 'Unvoted'),
(17, 'May', 'Mendoza', 'Alvijos', '20100323', 'may', '1st year', 'Unvoted'),
(18, 'Golda', 'Nepomuceno', 'Molentin', '20100316', 'golda', '1st year', 'Unvoted'),
(19, 'Shiera Mae', 'Tuting', 'Terer', '20100968', 'shiera', '3rd year', 'Unvoted'),
(20, 'Mary Ver', 'Libo-on', 'M', '20100381', 'mary', '1st year', 'Unvoted'),
(21, 'John Kevin', 'Lorayna', 'Amos', '20100412', 'kevin', '1st year', 'Unvoted'),
(22, 'Denmark', 'Tabiolo', 'R', '20100111', 'denmark', '1st year', 'Unvoted'),
(16, 'Sherwin', 'Laylon', 'Delicana', '20100349', 'zac', '3rd year', 'Unvoted');



--
-- Dumping data for table `votes`
--

INSERT INTO `votes` (`ID`, `CandidateID`, `votes`) VALUES
(205, 0, 0),
(204, 0, 0),
(203, 153, 0),
(202, 129, 0),
(201, 95, 0);


delete from candidate where CandidateID=1;


delete from users where User_id=2;	


delete from voter where voter_name like 'aa%';



delete from votes where id=2;




ALTER TABLE `candidate`
  ADD PRIMARY KEY (`CandidateID`),
  

ALTER TABLE `history`
  ADD PRIMARY KEY (`history_id`);

ALTER TABLE `users`
  ADD PRIMARY KEY (`User_id`);


ALTER TABLE `voters`
  ADD PRIMARY KEY (`VoterID`);


ALTER TABLE `votes`
  ADD PRIMARY KEY (`ID`),
  


ALTER TABLE `candidate`
  MODIFY `CandidateID` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

ALTER TABLE `history`
  MODIFY `history_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=10;

ALTER TABLE `users`
  MODIFY `User_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=20;

ALTER TABLE `voters`
`
  MODIFY `VoterID` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

ALTER TABLE `votes`
  MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=22;


ALTER TABLE `votes`
  ADD CONSTRAINT `ID` FOREIGN KEY (`CandidateID`) REFERENCES `candidate` (`CandidateID`) ON DELETE CASCADE;











