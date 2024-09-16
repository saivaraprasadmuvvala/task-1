# task-1

 #include <stdio.h>

void convertTemperature(float temp, char unit);

int main() { float temp; char unit;

printf("Enter temperature value: ");
scanf("%f", &temp);
printf("Enter unit of measurement (C for Celsius, F for Fahrenheit, K for Kelvin): ");
scanf(" %c", &unit);

convertTemperature(temp, unit);

return 0;
}

void convertTemperature(float temp, char unit) { float celsius, fahrenheit, kelvin;

switch(unit) {
    case 'C':
    case 'c':
        celsius = temp;
        fahrenheit = (temp * 9/5) + 32;
        kelvin = temp + 273.15;
        printf("%.2f Celsius is equivalent to %.2f Fahrenheit and %.2f Kelvin.\n", celsius, fahrenheit, kelvin);
        break;
    case 'F':
    case 'f':
        fahrenheit = temp;
        celsius = (temp - 32) * 5/9;
        kelvin = celsius + 273.15;
        printf("%.2f Fahrenheit is equivalent to %.2f Celsius and %.2f Kelvin.\n", fahrenheit, celsius, kelvin);
        break;
    case 'K':
    case 'k':
        kelvin = temp;
        celsius = temp - 273.15;
        fahrenheit = (celsius * 9/5) + 32;
        printf("%.2f Kelvin is equivalent to %.2f Celsius and %.2f Fahrenheit.\n", kelvin, celsius, fahrenheit);
        break;
    default:
        printf("Invalid unit of measurement.\n");
        break;
}
}
