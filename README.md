Download Link: https://assignmentchef.com/product/solved-solvedp3-jukebox-solution
<br>
A visualization of a playlist(you are not actually creating a Graphical User Interface…yet)ContentsProject OverviewGetting StartedSpecificationTestingSubmitting Your ProjectProject OverviewIn this assignment, you will develop a class to represent a playlist of songs. We will provide a driver class with a menu and some methods for reading Song data from files. You will be reusing the class you write later in the semester.

ObjectivesManage objects in an ArrayList.Create an instantiable class.Design and implement several instance methods.Gain experience in test driven development.Override the toString method from the Object class

Getting StartedCreate a new Eclipse project for this assignment.The easiest way to import all the files into your project is to download and unzip the starter files directly into your project workspace directory (using the command-line or dolphin). The starter files are available here: http://cs.boisestate.edu/~cs121/projects/p3/stubs (You should download p3-stubs.zip)After you unzip the files into your workspace directory outside of Eclipse, go back to Eclipse and refresh your project. It should look something like this.There will be several errors, but these are expected until you finish implementing your Song.java and PlayList.java classes.Modify the existing Song class, implementing it according to the specifications below.

When you have completed your Song class, the errors in SongTest will go away and you can use it to test your Song class. You can still run it if there are errors in other classes. Just ignore the pop-up in Eclipse.

Test often! Run your program after each task so you can find and fix problems early. It is really hard for anyone to track down problems if the code was not tested along the way.

You should finish the entire Song class before moving on to PlayList.When you are done implementing the Song class and all of the tests in SongTest pass, create a new Java class called PlayList and implement it according to the specifications below.

When you have completed enough of your PlayList class, the errors in PlayListTest will go away and you can use it to test your PlayList class.

Test often! Run your program after each task so you can find and fix problems early. It is really hard for anyone to track down problems if the code was not tested along the way.

You should finish the entire PlayList class before moving on to Jukebox.When you think you are done with Song and PlayList, run the Jukebox driver class to make sure everything works as expected.Finally, run the final testing scripts as described in the testing section.This is super important!!This is what we will be using to grade your program. Most of your grade will depend on these tests passing, so make sure you take the time to get everything working. Start early so you have time to get help if you need it.

SpecificationExisting classes that you will use: SongTest.java, PlayListTest.javaExisting classes that you will modify: Song.java, Jukebox.javaClasses that you will create: PlayList.javaTask 1: Add Setters to Song.javaYour Song.java class already has getter (e.g. accessor) methods that were included in project 2. You need to modify the Song class to include setter methods.

Setter MethodsWrite setter (e.g. mutator) methods for the following instance variables.title (String), artist (String), playtime (int), filepath (string)SongTest.javaYou do not need to modify this class. You will just use it to test your Song class.When you think you are done with your Song class. Compile and run SongTest.java to make sure all the tests pass.Task 2: Implement PlayList.javaYou will write another instantiable class called PlayList. Your playlist will use an ArrayList of Songobjects to keep track of a user’s songs.

Instance VariablesThe data for a PlayList should include a name, a reference to the song currently playing, and a songList.

Your PlayList class should include instance variables for all of these.

The name should be a String.The song currently playing should be a Song reference to the song playing at the moment.The songList should be an ArrayList Following good object-oriented practice, your instance variables should be private.ConstructorYou should write one constructor for this class.The constructor must take in a value for and set the name of the playlist, initialize playing to null, and initialize the songList to an empty list.MethodsWrite accessor (getter) methods for your name, playing, and songList instance variables.Write mutator (setter) methods for the name instance variables. Why don’t we have setters for all instance variables?Add and complete these additional methods that will allow us to add/remove/play songs in the playlist.addSong. Takes a song as an argument and returns nothing. Adds it to the songList.removeSong. Takes an integer index as an argument and returns the removed song. Removes the song from the songList. Returns null if the index is out of range.getNumSongs. Returns the number of songs in the playlist.getTotalPlayTime. Returns the total playtime of all songs in the playlist (in seconds).getSong. Takes an integer index as an argument and returns the song at that index, if it exists. Returns null if it does not exist.playSong. Takes an integer index as an argument and plays the corresponding song in the play list. If the index is out of range, do nothing. Don’t forget to set the playing instance variable to the song so we know it is playing.getInfo. Returns a String that will display the following stats.The average play time in seconds.The shortest song.The longest song.The total play time of the playlist.The returned string should have the following format:The average play time is: 129.00 secondsThe shortest song is: An awesome song Coolio Jo sounds/westernBeat.wav 5The longest song is: Eighties Jam Some 80’s band sounds/eightiesJam.wav 201Total play time: 387

Write a toString method for the PlayList class. The toString method is inherited from the Object class. In order to have it do something appropriate to the PlayList class, you need to override it. The signature of the toString method ispublic String toString()It can access the instance variables. This method should return a String containing the name, number of songs, and all the songs in the playlist in the following format——————Sample Playlist (3 songs)——————(0) Classical A Classical Artist sounds/classical.wav 181(1) Eighties Jam Some 80’s band sounds/eightiesJam.wav 201(2) New Age Javya sounds/newAgeRhythm.wav 132——————

Don’t re-write the code to generate strings for each song. Just use the String returned by the toString method in Song.java.PlayListTest.javaYou do not need to modify this class. You will just use it to test your PlayList class.When you think you are done with your PlayList class. Compile and run PlayListTest.java to make sure all the tests pass.Task 3: Complete Jukebox.javaIt is the driver class, meaning, it will contain the main method.

This class is mostly done for you. You must

Add an info option to the Jukebox menu that will display statistics about the playlist. The menu option should be displayed as(i) infoUse the getInfo method from your PlayList class to display the info when the option is selected.Complete the readSong method defined in Jukebox.java. We have provided a “stub” of the method for you. Look for and complete the TODO comments.

The method should read a Song from the keyboard and return a Song. The data for each instance variable will be entered on a separate line.There are four lines of input for each song.

A sample input is shown below.This is My SongSinging Artiste03:21sounds/hitchcock.wav

TestingOnce you have completed your program in Eclipse, copy all your .java and README files into a directory on the onyx server, with no other files (if you did the project on your computer).

Navigate to your project directory on the command-line and run the autograder using the following command.

./autograde.sh

When you pass all of the requirements, your output will look something like the output below. Most of your grade will depend on these tests passing, so make sure you take the time to get everything working. Start early so you have time to get help if you need it.

[<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="50293f25103f3e2928">[email protected]</a> P3]$ ./autograde.sh——————-Testing Song.java——————-PASSED: getTitlePASSED: getArtistPASSED: getPlayTimePASSED: getFilePathPASSED: getPlayCountPASSED: setTitlePASSED: setArtistPASSED: setPlayTimePASSED: setFilePathPASSED: playPASSED: toString———————-Testing PlayList.java———————-PASSED: getNamePASSED: setNamePASSED: getPlaying – nothing playingPASSED: addSongPASSED: getSongPASSED: removeSongPASSED: getNumSongs – empty listPASSED: getNumSongsPASSED: getTotalPlayTime – empty listPASSED: getTotalPlayTimePASSED: playSongPASSED: getPlaying – after playSongPASSED: getInfo – empty listPASSED: getInfo – with songsPASSED: toString – empty listPASSED: toString – with songs——————-Testing Jukebox.java (output below)——————-===========================Welcome to the super jukebox!===========================You must create a playlist to get started.—————————(f) load playlist from file(n) create new playlist—————————Choose an option: Playlist added.——————Sample Playlist (3 songs)——————(0) Classical A Classical Artist sounds/classical.wav 181(1) Eighties Jam Some 80’s band sounds/eightiesJam.wav 201(2) New Age Javya sounds/newAgeRhythm.wav 132——————

What do you want to do (type ‘m’ to show menu)? Enter title: Enter artist: Enter play time: Enter file: Added song: An awesome songWhat do you want to do (type ‘m’ to show menu)? ——————Sample Playlist (4 songs)——————(0) Classical A Classical Artist sounds/classical.wav 181(1) Eighties Jam Some 80’s band sounds/eightiesJam.wav 201(2) New Age Javya sounds/newAgeRhythm.wav 132(3) An awesome song Coolio Jo sounds/westernBeat.wav 5——————

Choose a valid song id: Removed song.What do you want to do (type ‘m’ to show menu)? ——————Sample Playlist (3 songs)——————(0) Classical A Classical Artist sounds/classical.wav 181(1) Eighties Jam Some 80’s band sounds/eightiesJam.wav 201(2) An awesome song Coolio Jo sounds/westernBeat.wav 5——————

Choose a valid song id: Playing song: Eighties Jam Some 80’s band sounds/eightiesJam.wav 201What do you want to do (type ‘m’ to show menu)?——————Sample Playlist (3 songs)——————(0) Classical A Classical Artist sounds/classical.wav 181(1) Eighties Jam Some 80’s band sounds/eightiesJam.wav 201(2) An awesome song Coolio Jo sounds/westernBeat.wav 5——————

What do you want to do (type ‘m’ to show menu)?The average play time is: 129.00 secondsThe shortest song is: An awesome song Coolio Jo sounds/westernBeat.wav 5The longest song is: Eighties Jam Some 80’s band sounds/eightiesJam.wav 201Total play time: 387

What do you want to do (type ‘m’ to show menu)? Goodbye!————————–DONE running Jukebox testVerify that the output is correct. Each song should have played and must have a valid file location.Your final playlist should be——————Sample Playlist (3 songs)——————(0) Classical A Classical Artist sounds/classical.wav 181(1) Eighties Jam Some 80’s band sounds/eightiesJam.wav 201(2) An awesome song Coolio Jo sounds/westernBeat.wav 5——————

Generated javadocs. Run the following command to view your documentation!google-chrome doc/index.html

Make sure that each method has the correct documentation or you will lose pointsWhen you are done, remove the entire doc directory using “rm -rf doc”

README found. Make sure it follows the correct format.

Keep in mind that this doesn’t test EVERYTHING.You should still make sure your indentation is correct and that you are submittingthe correct files, using good coding practices, javadocs, etc.

Extra CreditSearch (10 points)As anyone with a large music collection will tell you, it can be extremely difficult to find the music you want if you must scroll through a long list of songs. To help with this situation, you will implement a search tool for the jukebox.

Task 1: (6 points)Modify PlayList class and add a search() method. This method will take a String as a parameter and will return an ArrayList containing Song objects whose title or artist match the query string. The following signature should be used for the search() method:public ArrayList Add a search option to the Jukebox menu that will prompt the user for a query string and display a list of songs from the playlist that match the search criteria. The menu option should be displayed as(s) searchUse the search() method from your PlayList class to display the results when the option is selected.After displaying the search results, prompt the user for the index of a particular song to play from the search results, or press ‘m’ for main menu. Once the user specifies a song to play, play the song using the Song object’s play() method.This is an sample walk throughWhat do you want to do (type ‘m’ to show menu)? m(p) play song(l) list songs(a) add song(d) delete song(i) info(s) search(q) quitWhat do you want to do (type ‘m’ to show menu)? sEnter search string:AgeSearch results containing: Age(0) New Age Javya sounds/newAgeRhythm.wav 132Choose a song id to play (m for main menu): 0What do you want to do (type ‘m’ to show menu)?

Task 2: (4 points)Add a test case to the PlayListTest class for the search() method. The test case should check for the following conditions: query string matches at least one song, query string matches no songs, query string is empty string “”.

Submitting Your ProjectDocumentationJavadoc CommentsIf you haven’t already, add javadoc comments to your program. They should be located immediately before the class header and before each method. If you forgot how to do this, go look at theDocumenting Your Program section from lab.

Have a class javadoc comment before the class.Your class comment must include the @author tag at the end of the comment. This will list you as the author of your software when you create your documentation.Have javadoc comments before every method that you wrote. Comments must include @paramand @return tags as appropriate.To build and view your comments, run the following commands.javadoc -author -d doc *.javagoogle-chrome doc/index.html

READMEInclude a plain-text file called README that describes your program and how to use it. Expected formatting and content are described in README_TEMPLATE. See README_EXAMPLE for an example.SubmissionYou will follow the same process for submitting each project.

Open a console and navigate to the project directory containing your source files,Remove all the .class files using the command, rm *.class.In the same directory, execute the submit command for your section as shown in the following table.Look for the success message and timestamp. If you don’t see a success message and timestamp, make sure the submit command you used is EXACTLY as shown.

Required Source FilesRequired files (be sure the names match what is here exactly):Song.javaPlayList.javaJukebox.java (main class)SongTest.java (provided class)PlayListTest.java (provided class)playlist.txt (provided test file)autograde.sh (provided test file)READMESectionInstructorSubmit Command1Luke Hindman (TuTh 1:30 – 2:45)submit lhindman cs121-1 p32Greg Andersen (TuTh 9:00 – 10:15)submit gandersen cs121-2 p33Luke Hindman (TuTh 10:30 – 11:45)submit lhindman cs121-3 p34Marissa Schmidt (TuTh 4:30 – 5:45)submit marissa cs121-4 p35Jerry Fails (TuTh 1:30 – 2:45)submit jfails cs121-5 p3After submitting, you may check your submission using the “check” command. In the example below, replace