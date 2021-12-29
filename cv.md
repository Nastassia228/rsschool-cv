# Curriculum Vitae

**Name:** Anastasia Kondratyuk
********
**Contact:** *anastasiakondratyuk98@gmail.com*
********
**Induction:** Hello World
********
**Skills:** HTML, CSS, JS, C, Python
****
**Code example:**

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
#include <stdint.h>
#include <stdio.h>
#include <stdlib.h>

// Number of bytes in .wav header
const int HEADER_SIZE = 44;

int main(int argc, char *argv[])
{
    // Check command-line arguments
    if (argc != 4)
    {
        printf("Usage: ./volume input.wav output.wav factor\n");
        return 1;
    }

    // Open files and determine scaling factor
    FILE *input = fopen(argv[1], "r");
    if (input == NULL)
    {
        printf("Could not open file.\n");
        return 1;
    }

    FILE *output = fopen(argv[2], "w");
    if (output == NULL)
    {
        printf("Could not open file.\n");
        return 1;
    }

    float factor = atof(argv[3]);

    // TODO: Copy header from input file to output file
    uint8_t header[HEADER_SIZE];
    while (fread(&header, HEADER_SIZE, 1, input))
    {
        fwrite(&header, HEADER_SIZE, 1, output);
    }

    // TODO: Read samples from input file and write updated data to output file
    int16_t buffer;
    while (fread(&buffer, sizeof(int16_t), 1, input))
    {
        buffer *= factor;
        fwrite(&buffer, sizeof(int16_t), 1, output);
    }

    // Close files
    fclose(input);
    fclose(output);
}

```

**Working experience:** Financial Analyst, 3 years
===
**Education:** Belarusian National Technical University, project-manager
===
**English level:** B2
