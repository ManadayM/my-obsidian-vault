---
template: note
parent: [[Java]]
tags: 
aliases: []
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1543039717-b4d407223b4c?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4NzYyMTYw&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-25) | (time:: 20:45) | (weather:: Vadodara: 🌦   +27°C ↑18km/h)

# Java Arrays
In [[Java]], an array is a collection of variables of the same type. Check [[Arrays]] to learn it from the Data Structure perspective.

## Creating an array
```java
DVD[] dvdCollection = new DVD[15];

public class DVD {
	
	public String name;
	public int releaseYear;
	public String director;
	
	public DVD(String name, int releaseYear, String director) {
		this.name = name;
		this.releaseYear = releaseYear;
		this.director = director;
	}

	public String toString() {
		return (
			this.name + 
			", directed by " + 
			this.director + 
			", released in year " + 
			this.releaseYear
		);
	}
}
```

> [!NOTE] Default values
> Java always initializes empty Array slots to `null` if the Array contains objects, or to default values if it contains primitive types.

## Writing to an array
Let's put a DVD for The Avengers into the 8th place of the Array we created above.

```java
DVD avengersDVD = new DVD("The Avengers", 2012, "Joss Whedon");

dvdCollection[7] = avengersDVD;
```

Let's add a few more DVDs.

```java
DVD incrediblesDVD = new DVD("The Incredibles", 2004, "Brad Bird");
DVD findginDoryDVD = new DVD("Finding Dory", 2016, "Andrew Stanton");
DVD lionKingDVD = new DVD("The Lion King", 2019, "Jon Favreau");

dvdCollection[3] = incrediblesDVD;
dvdCollection[9] = findginDoryDVD;
dvdCollection[2] = lionKingDVD;
```

## Reading from an array
```java
System.out.println(dvdCollection[7]);
System.out.println(dvdCollection[10]);
System.out.println(dvdCollection[3]);

// Will print:
// The Avengers, directed by Joss Whedon, released in 2012
// null
// The Incredibles by Brad Bird, released in 2004
```

---
#### Internal Links
[[2022-07-25]], [[Java]], [[Java Types]]