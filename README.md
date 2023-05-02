Download Link: https://assignmentchef.com/product/solved-coa-lab-1-implement-a-32-bit-alu
<br>
The goal of this LAB is to implement a 32-bit ALU (Arithmetic Logic Unit) with 32 1-bit ALUs. ALU is the basic computing component of a CPU. Its operations include AND, OR, addition, subtraction, etc. This series of LABs will help you understand the CPU architecture.

2.       HW Requirement

<ul>

 <li>Please use Icarus Verilog and GTKWave as your HDL simulator.</li>

 <li>Please attach your name and student ID as comment at the top of each file.</li>

 <li>Please use the Testbench we provide you, and DO NOT modify it.</li>

 <li>The names of top module and IO ports must be named as follows:</li>

</ul>

Top module: alu.v

ALU starts to work when the signal rst_n is 1, and then catches the data from src1 and src2.

In order to have a good coding style, please obey the rules below:

One module is written in one file.

Module name and file name must be the same.

For example: The file “alu.v” only contains the module “alu”.

<ul>

 <li>Basic instruction set (60%)</li>

</ul>

<table width="518">

 <tbody>

  <tr>

   <td width="173"><strong>ALU action</strong></td>

   <td width="173"><strong>Description</strong></td>

   <td width="173"><strong>ALU control input</strong></td>

  </tr>

  <tr>

   <td width="173">AND</td>

   <td width="173">Bitwise and</td>

   <td width="173">0000</td>

  </tr>

  <tr>

   <td width="173">OR</td>

   <td width="173">Bitwise or</td>

   <td width="173">0001</td>

  </tr>

  <tr>

   <td width="173">ADD</td>

   <td width="173">Addition (with overflow)</td>

   <td width="173">0010</td>

  </tr>

  <tr>

   <td width="173">SUB</td>

   <td width="173">Subtract</td>

   <td width="173">0110</td>

  </tr>

  <tr>

   <td width="173">NOR</td>

   <td width="173">Bitwise nor</td>

   <td width="173">1100</td>

  </tr>

  <tr>

   <td width="173">NAND</td>

   <td width="173">Bitwise nand</td>

   <td width="173">1101</td>

  </tr>

  <tr>

   <td width="173">SLT</td>

   <td width="173">Set less than (signed)</td>

   <td width="173">0111</td>

  </tr>

 </tbody>

</table>







<ul>

 <li>ZCV three flags: zero, carry out, and overflow (30%)</li>

</ul>

<table width="380">

 <tbody>

  <tr>

   <td width="79"><strong>Flag name</strong></td>

   <td width="301"><strong>Operation</strong></td>

  </tr>

  <tr>

   <td width="79">Zero</td>

   <td width="301">Output 1 when the output of ALU is 0Otherwise, output 0</td>

  </tr>

  <tr>

   <td width="79">Cout</td>

   <td width="301">Output 1 when the carry-out is 1 (for ADD SUB)Otherwise, output 0</td>

  </tr>

  <tr>

   <td width="79">Overflow</td>

   <td width="301">Output 1 when signed overflow happens (for ADD SUB)Otherwise, output 0</td>

  </tr>

 </tbody>

</table>

<h1></h1>

<h1>4.       Bonus: Extra instruction set</h1>

<table width="418">

 <tbody>

  <tr>

   <td width="120"><strong>ALU action</strong></td>

   <td width="172"><strong>Description</strong></td>

   <td width="126"><strong>ALU control input</strong></td>

  </tr>

  <tr>

   <td width="120">SLT</td>

   <td width="172">Set less than</td>

   <td width="126">0111_000</td>

  </tr>

  <tr>

   <td width="120">SGT</td>

   <td width="172">Set greater than</td>

   <td width="126">0111_001</td>

  </tr>

  <tr>

   <td width="120">SLE</td>

   <td width="172">Set less equal</td>

   <td width="126">0111_010</td>

  </tr>

  <tr>

   <td width="120">SGE</td>

   <td width="172">Set greater equal</td>

   <td width="126">0111_011</td>

  </tr>

  <tr>

   <td width="120">SEQ</td>

   <td width="172">Set equal</td>

   <td width="126">0111_110</td>

  </tr>

  <tr>

   <td width="120">SNE</td>

   <td width="172">Set not equal</td>

   <td width="126">0111_100</td>

  </tr>

 </tbody>

</table>

Hint: Add a module named “Compare” in 1-bit ALU!

<h1></h1>