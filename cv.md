# Curriculum Vitae

1. Name: Anastasia Kondratyuk
2. Contact: *anastasiakondratyuk98@gmail.com*
3. Induction: Hello World
4. Skills: HTML, CSS, JS, C, Python
5. Code example: 

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <script>
      function filterRangeInPlace(arr, a, b) {
        arr.forEach((item, index) =>
          item <= b && item >= a ? item : arr.splice(index, 1)
        );
        return arr;
      }
      let arr = [5, 3, 8, 1];
      console.log(filterRangeInPlace(arr, 1, 4));
    </script>
  </body>
</html>
```
```
#include <cs50.h>
#include <stdio.h>
#include <string.h>

// Max number of candidates
#define MAX 9

// Candidates have name and vote count
typedef struct
{
    string name;
    int votes;
}
candidate;

// Array of candidates
candidate candidates[MAX];

// Number of candidates
int candidate_count;
int winner = 0;

// Function prototypes
bool vote(string name);
void print_winner(void);

int main(int argc, string argv[])
{
    // Check for invalid usage
    if (argc < 2)
    {
        printf("Usage: plurality [candidate ...]\n");
        return 1;
    }

    // Populate array of candidates
    candidate_count = argc - 1;
    if (candidate_count > MAX)
    {
        printf("Maximum number of candidates is %i\n", MAX);
        return 2;
    }
    for (int i = 0; i < candidate_count; i++)
    {
        candidates[i].name = argv[i + 1];
        candidates[i].votes = 0;
    }

    int voter_count = get_int("Number of voters: ");

    // Loop over all voters
    for (int i = 0; i < voter_count; i++)
    {
        string name = get_string("Vote: ");

        // Check for invalid vote
        if (!vote(name))
        {
            printf("Invalid vote.\n");
        }
    }

    // Display winner of election
    print_winner();
}

// Update vote totals given a new vote
bool vote(string name)
{
    // linear search to check if the name is in the list
    for (int j = 0; j < candidate_count; j++)
    {
        if (strcmp(candidates[j].name, name) == 0)
            {
            candidates[j].votes++;
            return true;
            }
    }
    return false;
}

// Print the winner (or winners) of the election
void print_winner(void)
{
    // print a winner
    for (int k = 0; k < candidate_count; k++)
    {
        if (candidates[k].votes > winner)
        {
            winner = candidates[k].votes;
        }
    }
    for (int p = 0; p < candidate_count; p++)
    {
        if (candidates[p].votes == winner)
        {
            printf("%s\n", candidates[p].name);
        }
    }

    return;
}

```

6. Working experience: Financial Analyst, 3 years
7. Education: Belarusian National Technical University, project-manager
8. English level: B2
