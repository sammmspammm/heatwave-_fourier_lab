# Heatwave Fourier Lab

An interactive web page that explains half-range Fourier series (cosine and sine) and Parseval's identity using the hourly temperature of a heatwave day.

## What it shows

- The problem: finding the afternoon peak, the hot hours and a heatwave warning from hourly temperatures.
- The mirror trick that turns one day of data into a repeating curve (cosine series and sine series).
- A live lab: add Fourier waves one by one and watch the curve and the error change.
- One full numerical example for a coefficient, plus a hand example (x on (0, pi) giving the sum of 1/n^4 = pi^4/96).
- A Parseval energy check and a heatwave decision with advice.
- A tab for your own readings: paste hourly temperatures or upload a CSV (the Open-Meteo hourly CSV works).

## How to run

Open `index.html` in any browser. No installation is needed. The fonts load from Google Fonts when online and fall back to system fonts otherwise.

## Data

The default day is simulated from a formula:

    T(t) = mean + A cos(2 pi (t - 15) / 24) + 0.18 A cos(4 pi (t - 13) / 24) + noise

with mean 35.5 C, swing A = 7.5 C and noise 0.6 C, sampled hourly at t = 0, 1, ..., 24 h (25 observations). Replace it with real readings from a source such as Open-Meteo Historical Weather, data.gov.in or IMD station records, and cite the source.

## Limits

Simulated data, one day, simplified warning levels (the real IMD criteria also use departure from normal), and the mirror extension is a mathematical device.
