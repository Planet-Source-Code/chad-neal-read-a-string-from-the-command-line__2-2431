<div align="center">

## Read a string from the command line


</div>

### Description

reads a string from the command line. Should be easy but it wasnt explained well so I wrote this.
 
### More Info
 
text

I am using jdk 1.4 so I am not sure of compat problems ;(


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Chad Neal](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/chad-neal.md)
**Level**          |Beginner
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |Java \(JDK 1\.2\)
**Category**       |[Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/input-output__2-84.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/chad-neal-read-a-string-from-the-command-line__2-2431/archive/master.zip)





### Source Code

```
// hello <string>
import java.io.*;
public class hello
{
	public static void main(String[] args)
	{
		//setup global vars (bad)
		String userName = null;
		//setup input buffer
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		//do my stuff
		System.out.print("\nWhats your name?\n\n");
		//make sure to cath errors (they happen often with this ;( )
		try
		{
			userName = br.readLine();
		}
		catch (IOException ioerror)
		{
			System.out.println("IO error trying to read your name!");
			System.exit(1);
		}
		System.out.print("\n\n\nHello " + userName + "!!!\n\n\n");
	}
}
```

