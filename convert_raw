# convert the int array for an embedded pico-8 game back to a pico-8 cart
# note - you need to manually add a cart image using pico-8 itself
ints = []
with open("source", "r") as filestream:
  new_file = open("output.p8.png", mode="wb")
  for line in filestream:
    currentline = line.split(",")
    for value in currentline:
      if (value.isdigit()):
        int_val = int(value)
        ints.append(int_val)

  output = bytearray(ints)
  new_file.write(output)
  new_file.close()
