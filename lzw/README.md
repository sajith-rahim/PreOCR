Encoding:
The input data is encoded using the encoder.py file,
the dictionary of size 256 is built and initialized,
using the python dictionary data structure
in the dictionary, key are characters and values are the ascii values
the lzw compression algorithm is applied and we get the compressed data,
the program outputs the compressed data and stores it to an 
output file named inputFileName.lzw


python encoder.py <inputFileName.txt> <number of Bits>


Decoding:
The compressed data is decompressed using the decoder.py file,
the dictionary of size 256 is built and initialized,
using the python dictionary data structure
in the dictionary, key are characters and values are the ascii values
the lzw decompression algorithm is applied and we get the decompressed data,
the program outputs the decompressed data and stores it to an 
output file named inputFileName_decoded.txt

python decoder.py <inputFileName.lzw> <number of Bits>