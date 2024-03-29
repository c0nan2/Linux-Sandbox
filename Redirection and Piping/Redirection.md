# Redirection 

Normally, a command is run in the command line and its result is outputted to the terminal. However, there are ways we can *redirect* this output to somewhere else, such as another file, program, device, or even another command. This allows us to **chain** commands together in a **pipline**.   

There are three types of communication streams between a computer program and its enviroment 

* `Standard Input` (`stdin`): this is information inputted into the terminal by using a keyboard or another input device 
* `Standard Output` (`stdout`): this is information outputted once a command has been run
* `Standard Error` (`stderr`): this is an error message which is outputted when a falied process or incorrect command is run 

---

# Standard Out

If the below commmand was run:

```console
echo "Hello World!!"
```
Here, `Hello World!!` is entered as the standard input and `Hello World!!` is then outputted to the terminal as standard out. However, we can redirect the output to a file instead of directing it to the terminal. To do this, we would use the `>` command followed by the filename of where we want to send the output. 

```console
echo "Hello World!!" > greeting.txt
```
In the above example, `Hello World!!` would be redirected to the `greeting.txt` file instead of outputting it onto the terminal. We can check that the redirection has worked b using the `cat` command followed by the name of the file we sent the direct to, for example, 

![image](https://user-images.githubusercontent.com/107522496/197761925-2ce542de-981e-4402-93fe-64c46ee7b838.png)


---

# `>`
The `>` command takes the takes the standard output of the command to its left, and redirects it to the file to its right. 

> Important: `>` overwrites the contents of a file. Too know how to append data onto the end of a file, see the next section. 

![image](https://user-images.githubusercontent.com/107522496/197763872-d8559b55-63a5-476f-b007-817aef207df4.png)

In the above example, we are taking the contents of the `cities.txt` file and sending it (redirecting it) to the `namesofcities.txt` file. Because we have redirected the output to a file, we won't see the output on the terminal.

We can confirm that indeed this redirect has been successful by using the `cat`command on the new file:

![image](https://user-images.githubusercontent.com/107522496/197764218-9795681f-5dd4-4f9b-8b40-10abf4f32077.png)

---

# `>>`

The `>>` allows to add text to a file without losing the original text.

![image](https://user-images.githubusercontent.com/107522496/197770528-570fe7d1-6efc-4e12-960e-a090cb67f7d2.png)


Here, the contents of `animals.txt` have been sent to the end of the contents of `greeting.txt`. The orginal text of `greeting.txt` remains. 








