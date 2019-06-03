Programa de ejemplo para decodificar ficheros de waveforms codificados con Huffman.

Está en c++ con el estandar c++11. En linux se puede compilar de esta forma:

:code:`$ g++ -std=c++11 decode_huffman_standalone.cc -o decode_huffman_standalone`

Luego para ejecutarlo:

.. code-block::

    $ ./decode_huffman_standalone
    Usage: rawdatareader <filein> <tree_file> <fileout> <npmts> <offset>

Los argumentos son los siguientes:

- :code:`filein`: fichero de texto con las waveforms en cuestión por columnas)
- :code:`tree_file`: fichero de texto con el huffman tree definido.
- :code:`fileout`: ruta del fichero de salida donde se escribirán las waveforms decodificadas.
- :code:`npmts`: Número de waveforms (columnas) a leer del fichero filein.
- :code:`offset`: Número de bits a omitir al principio del fichero (en el ejemplo que me envistéis habia 16 bits de un FT).

En ese caso la forma de correrlo sería:

:code:`$ ./decode_huffman_standalone filein.txt tree.txt fileout.txt 12 16`

En windows cualquier compilador de c++ que puedas encontrar debería servir. No hay ninguna librería externa en ese ejemplo.
