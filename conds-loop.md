# SELECTIVE CONTROL STRUCTURES <h1>
  
  **Control structures**
  
According to the structure theorem, any computer program can be written using the basic control structures. They can be combined in any way necessary to deal with a given problem.

**True or False**

The selection structure tests a condition, then executes one sequence of statements instead of another, depending on whether the condition is true or false. A condition is any variable or expression that returns a Boolean value.

The iteration structure executes a sequence of statements repeatedly as long as a condition holds true. The sequence structure simply executes a sequence of statements in the order in which they occur.

The basic attribute of a selection control structure is to be able to select between two or more alternate paths. This is described as either two-way selection or multi-way selection. A question using Boolean concepts usually controls which path is selected. All of the paths from a selection control structure join back up at the end of the control structure, before moving on to the next lines of code in a program.

**IF**

The simplest form of IF statement associates a condition with a sequence of statements enclosed by the keywords THEN and END IF (not ENDIF), as follows:

IF condition THEN
   sequence_of_statements
END IF;

The sequence of statements is executed only if the condition is true. If the condition is false or null, the IF statement does nothing. In either case, control passes to the next statement. An example follows:

IF sales > quota THEN
   compute_bonus(empid);
   UPDATE payroll SET pay = pay + bonus WHERE empno = emp_id;
END IF;

You might want to place brief IF statements on a single line, as in

IF x > y THEN high := x; END IF;

**IF ELSE**


The second form of IF statement adds the keyword ELSE followed by an alternative sequence of statements, as follows:

IF condition THEN
   sequence_of_statements1
ELSE
   sequence_of_statements2
END IF;

The sequence of statements in the ELSE clause is executed only if the condition is false or null. Thus, the ELSE clause ensures that a sequence of statements is executed. In the following example, the first UPDATE statement is executed when the condition is true, but the second UPDATE statement is executed when the condition is false or null:

IF trans_type = 'CR' THEN
   UPDATE accounts SET balance = balance + credit WHERE ...
ELSE
   UPDATE accounts SET balance = balance - debit WHERE ...
END IF;

The THEN and ELSE clauses can include IF statements. That is, IF statements can be nested, as the following example shows:

IF trans_type = 'CR' THEN
   UPDATE accounts SET balance = balance + credit WHERE ...
ELSE
   IF new_balance >= minimum_balance THEN
      UPDATE accounts SET balance = balance - debit WHERE ...
   ELSE
      RAISE insufficient_funds;
   END IF;
END IF;

**WHILE**

A while loop in C programming repeatedly executes a target statement as long as a given condition is true.
statement(s) may be a single statement or a block of statements. The condition may be any expression, and true is any nonzero value. The loop iterates while the condition is true.

When the condition becomes false, the program control passes to the line immediately following the loop.
Here, the key point to note is that a while loop might not execute at all. When the condition is tested and the result is false, the loop body will be skipped and the first statement after the while loop will be executed.

**FOR**

Whereas the number of iterations through a WHILE loop is unknown until the loop completes, the number of iterations through a FOR loop is known before the loop is entered. FOR loops iterate over a specified range of integers. The range is part of an iteration scheme, which is enclosed by the keywords FOR and LOOP. A double dot (..) serves as the range operator. 

**BREAk**

It means stopping the execution of a loop and leaving it.
continue: Used to stop the current iteration and return to the beginning of the loop to perform another iteration, if applicable.
Break
A loop is stopped using the word break. Stopping a loop means exiting it and leaving everything as is to continue the program flow immediately after the loop.

for (i = 0; i <10; i ++) {
   document.write (i)
   type = prompt ("tell me if I keep asking ...", "yes")
   if (type == "no")
      break
}
This example writes the numbers from 0 to 9 and in each iteration of the loop asks the user if they want to continue. If the user says anything, it continues, except when he says "no", a situation in which he exits the loop and leaves the account where he left off.

Continue
It is used to return to the beginning of the loop at any time, without executing the lines below the word continue.

var i = 0
while (i <7) {
   increase = prompt ("The account is at" + i + ", tell me if I increase", "if")
   if (increment == "no")
      continue
   i ++
}
This example would normally count from i = 0 to i = 7, but each time the loop is executed it asks the user if he wants to increase the variable or not. If you enter "no", the continue statement is executed, which returns to the beginning of the loop without increasing the variable i by 1, since the statements below the continue would be ignored.



