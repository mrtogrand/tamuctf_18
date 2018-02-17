# Band Aid

The binary had some conditional GOTO at 0x08048cf4 which i replaced with nop. This made it print out this stuff:

``` this code needs a band aid
result
L/R8ejlvVP4+JvgvsSI+JaLn6YCArf5fTAIfUwMNCrJ8HkRkQLEB5RH5COF1+9mSQoGY8wG23AtDyM0OEgm+zFCTibFOgieixjrv5OHAIB+akOahMWoyt/qAGnK9ZsLsv20apyzlH0llafbfQ0MkurU/c8O3Xj3m0VL1GOjHk14=
LS0tLS1CRUdJTiBSU0EgUFJJVkFURSBLRVktLS0tLQpNSUlDV3dJQkFBS0JnUUNjVDRaalluR2lNWXRFZDcrL1l0RmdHRTNlZ1RrV0Jpd2hXQ240MUxQU1lzdXErNE9RCnBuQk1ZUjVZdExiOTRXTzdpNnZHYU9PTnNzSE5kWUFkblJETThpTFN2L3JUMHVPdGdTd2RaTmlMQzduNmdILzgKOFJqRlFFTGptSldRemdzWDhDVXFkWm80SnJNZkJTbXd3RFlBNUJtMGI3Nmd6bXFoK3lMWGErdW5PUUlEQVFBQgpBb0dBYWNhUy9adzNvM2Q5Yy9iSkpqMDd6SmlGMFdXRytQVnlWWm93eFBkRFBNS29hbXRMYTg2RnZkb1d6QloyCm9yVXNaVlN1Q0ZVZ2I5b2d0ZVdtcmVPRTR1d0FQK0RGKzJpU1h0MlZxTEdJZ29ieDZib0YrTktjMXNvUUFEaFQKNkw2emZNSzFNVzZwSDVYUGNVNUg4QU1TWUREYVFxeEVtWEp0azg4OUxJTVpVUUVDUVFDNDRYVjRqdEwwcjFkcQpjY1ByTlIrTEp4UjExMkJPMEhXLzduRVEwQUtUbUhIZ2EvbmV1ejMycHF1TVNRM2xodXRTNW5kanNzdmJ3dHJuCjNWdVhKRUJaQWtFQTJIQ1E0bE12MHI5Y3B2b2lCTVR0cDlYS2dIeU5Vbmd3dE1SODZ6VE0vK1dudlhTWjlDZk8KWXhyMlVvd2daMTlPNXpCZDFrVGRZQnNMbFVoL2syekI0UUpBWWtMeVBIRXNqZi9qWmgreEVZSGFrZ3JqUlA2RApvV0FLTlVoMXI0bmUxTE5oVXZZUWgrRGN2Z3MzZ2dnUjZyd2F0cVRuTDRZSDgzVk5BNDhTN3ZIRmdRSkFkeFZvCkFiNDNQOExkM1ZrZVFuVi9OS3FpSWhObFJneXU3Nlp6L0kwdWhWVDc5M2NpQlgycFJrbmRZUW1NQXBRanUzdVgKQlg4YU5maHJaUlZnYStLWXdRSkFYY1RKemE3ODNFeVk1YmxTZWIvWlJGYzZjdnFERDlRSDRXRVQ1b000ZjFnWgprZlI3Ti9qcEc4b09sZkl5d2o1RStaaHJaSTlEY1RmQjVnQWlFRHFrQmc9PQotLS0tLUVORCBSU0EgUFJJVkFURSBLRVktLS0tLQ==
LS0tLS1CRUdJTiBQVUJMSUMgS0VZLS0tLS0KTUlHZk1BMEdDU3FHU0liM0RRRUJBUVVBQTRHTkFEQ0JpUUtCZ1FDY1Q0WmpZbkdpTVl0RWQ3Ky9ZdEZnR0UzZQpnVGtXQml3aFdDbjQxTFBTWXN1cSs0T1FwbkJNWVI1WXRMYjk0V083aTZ2R2FPT05zc0hOZFlBZG5SRE04aUxTCnYvclQwdU90Z1N3ZFpOaUxDN242Z0gvODhSakZRRUxqbUpXUXpnc1g4Q1VxZFpvNEpyTWZCU213d0RZQTVCbTAKYjc2Z3ptcWgreUxYYSt1bk9RSURBUUFCCi0tLS0tRU5EIFBVQkxJQyBLRVktLS0tLQ==```

this is three different lines. the first i haven't cracked but the second two are base64 encoded - here they are decoded:

```-----BEGIN PUBLIC KEY-----
MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQCcT4ZjYnGiMYtEd7+/YtFgGE3e
gTkWBiwhWCn41LPSYsuq+4OQpnBMYR5YtLb94WO7i6vGaOONssHNdYAdnRDM8iLS
v/rT0uOtgSwdZNiLC7n6gH/88RjFQELjmJWQzgsX8CUqdZo4JrMfBSmwwDYA5Bm0
b76gzmqh+yLXa+unOQIDAQAB
-----END PUBLIC KEY-----%  ```


```-----BEGIN RSA PRIVATE KEY-----
MIICWwIBAAKBgQCcT4ZjYnGiMYtEd7+/YtFgGE3egTkWBiwhWCn41LPSYsuq+4OQ
pnBMYR5YtLb94WO7i6vGaOONssHNdYAdnRDM8iLSv/rT0uOtgSwdZNiLC7n6gH/8
8RjFQELjmJWQzgsX8CUqdZo4JrMfBSmwwDYA5Bm0b76gzmqh+yLXa+unOQIDAQAB
AoGAacaS/Zw3o3d9c/bJJj07zJiF0WWG+PVyVZowxPdDPMKoamtLa86FvdoWzBZ2
orUsZVSuCFUgb9ogteWmreOE4uwAP+DF+2iSXt2VqLGIgobx6boF+NKc1soQADhT
6L6zfMK1MW6pH5XPcU5H8AMSYDDaQqxEmXJtk889LIMZUQECQQC44XV4jtL0r1dq
ccPrNR+LJxR112BO0HW/7nEQ0AKTmHHga/neuz32pquMSQ3lhutS5ndjssvbwtrn
3VuXJEBZAkEA2HCQ4lMv0r9cpvoiBMTtp9XKgHyNUngwtMR86zTM/+WnvXSZ9CfO
Yxr2UowgZ19O5zBd1kTdYBsLlUh/k2zB4QJAYkLyPHEsjf/jZh+xEYHakgrjRP6D
oWAKNUh1r4ne1LNhUvYQh+Dcvgs3gggR6rwatqTnL4YH83VNA48S7vHFgQJAdxVo
Ab43P8Ld3VkeQnV/NKqiIhNlRgyu76Zz/I0uhVT793ciBX2pRkndYQmMApQju3uX
BX8aNfhrZRVga+KYwQJAXcTJza783EyY5blSeb/ZRFc6cvqDD9QH4WET5oM4f1gZ
kfR7N/jpG8oOlfIywj5E+ZhrZI9DcTfB5gAiEDqkBg==
-----END RSA PRIVATE KEY-----%```

and here's the first thing again:

```L/R8ejlvVP4+JvgvsSI+JaLn6YCArf5fTAIfUwMNCrJ8HkRkQLEB5RH5COF1+9mSQoGY8wG23AtDyM0OEgm+zFCTibFOgieixjrv5OHAIB+akOahMWoyt/qAGnK9ZsLsv20apyzlH0llafbfQ0MkurU/c8O3Xj3m0VL1GOjHk14=```