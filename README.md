# cs341-lab2-memory-exploration-solved
**TO GET THIS SOLUTION VISIT:** [CS341 Lab2-Memory Exploration Solved](https://www.ankitcodinghub.com/product/cs341-lab2-memory-exploration-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;68046&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS341 Lab2-Memory Exploration Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
The goal in this lab will be to explore the Harvard architecture and its memory spaces. The starter code can be found on GitHub under Lab 2. The code is mostly written for you already, you should uncomment it bit by bit and observe what happens.

<h1>Part 1</h1>
The processor used in the Arduino UNO (the ATMEGA328) is built along the lines of the Harvard architecture.&nbsp; In this architecture, the processor stores program code and program data/stack in separate memory spaces.

&nbsp;

There are three memory spaces in the Arduino UNO processor architecture.&nbsp; See the Figure above. Note that addresses for each of the three memory spaces start with 0x0000 and go to a symbolic constant as the end address – FLASHEND, RAMEND, or E2END. These constants are defined in the IDE compiler and you will determine their hex values below.

&nbsp;

The Flash (program code) and EEPROM (configuration data) are non-volatile meaning that their contents are preserved across power cycles.&nbsp; The RAM is volatile so its contents are lost when the power is turned off.&nbsp; The contents of RAM are initialized during the power on sequence in the program code.

Note that the 32 general purpose registers and the I/O device registers are

“memory mapped” into the data memory address space from 0x0000 to 0x00ff.&nbsp; The program memory is organized as 16 bit words while the data memory and EEPROM are organized as bytes.

&nbsp;

<ol>
<li>Setup an Arduino in the simulator (no components necessary)</li>
<li>Find the section in the <a href="https://github.com/jack17davis/cs341/blob/master/Lab%202/Lab%202%20Starter.ino">code</a> labeled “Part 1” and uncomment it</li>
<li>Click run, and open the serial monitor</li>
<li><strong>Record the 3 constants in the results section of your lab report </strong></li>
</ol>
<strong>&nbsp;</strong>

<h1>Part 2</h1>
Now that we know the size of our memory spaces, lets create some arrays and see where they end up.

<ol>
<li>I have already created 6 arrays, 3 as global variables and 3 in setup</li>
<li>Take a careful look at the arrays, and how they are initialized</li>
<li>Uncomment the section in the code labeled “Part 2”</li>
<li>Clear the serial monitor, and click run</li>
<li>Look at the locations of the arrays and try to piece together how the compiler allocates memory. Where does the heap, stack, and initialized data end up?</li>
</ol>
&nbsp;

<h1>Part 3</h1>
After seeing where our arrays ended up, we’re going to print out sections of the RAM to confirm our guesses at the end of part 2. Tinkercad limits the buffer size of the serial monitor, so this means that we cannot look at the entire RAM at one time easily.

&nbsp;

<ol>
<li>I have already created the functions displayRAM and displayAllRAM to help you out. Call them like this:</li>
</ol>
displayRAM((char *) 0x100, (char *) 0x200, false); displayAllRAM(2000, false); //displays memory in 0x100 blocks with delays&nbsp; The output will look something like this.

&nbsp;

The first row corresponds to memory addresses 0x200 through 0x20F. Thus, the memory address 0x2A0 is currently storing the integer 4.

<ol start="2">
<li><strong>In your lab report answer the following question: </strong></li>
</ol>
<strong>What memory addresses were used by the stack, heap, and initialized data? </strong>Give rough estimates such as “the stack starts around 0x300 and extends towards 0x00.”
