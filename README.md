#Saludos Terricolas soy Juan Aguilera un entusiasta del mundo Linux y la ciberseguridad.
#Ahora estudiante de programacion en Python 

def print_banner(text):
    # Define the ASCII art for each character
    characters = {
        'A': ['  A  ', ' A A ', 'AAAAA', 'A   A', 'A   A'],
        'B': ['BBBB ', 'B   B', 'BBBB ', 'B   B', 'BBBB '],
        'C': [' CCCC', 'C    ', 'C    ', 'C    ', ' CCCC'],
        'D': ['DDD  ', 'D  D ', 'D   D', 'D  D ', 'DDD  '],
        'E': ['EEEEE', 'E    ', 'EEE  ', 'E    ', 'EEEEE'],
        'F': ['FFFFF', 'F    ', 'FFF  ', 'F    ', 'F    '],
        'G': [' GGGG', 'G    ', 'G  GG', 'G   G', ' GGGG'],
        'H': ['H   H', 'H   H', 'HHHHH', 'H   H', 'H   H'],
        'I': ['IIIII', '  I  ', '  I  ', '  I  ', 'IIIII'],
        'J': [' JJJJ', '    J', '    J', 'J   J', ' JJJ '],
        'K': ['K   K', 'K  K ', 'KKK  ', 'K  K ', 'K   K'],
        'L': ['L    ', 'L    ', 'L    ', 'L    ', 'LLLLL'],
        'M': ['M   M', 'MM MM', 'M M M', 'M   M', 'M   M'],
        'N': ['N   N', 'NN  N', 'N N N', 'N  NN', 'N   N'],
        'O': [' OOO ', 'O   O', 'O   O', 'O   O', ' OOO '],
        'P': ['PPPP ', 'P   P', 'PPPP ', 'P    ', 'P    '],
        'Q': [' QQQ ', 'Q   Q', 'Q   Q', 'Q  QQ', ' QQQQ'],
        'R': ['RRRR ', 'R   R', 'RRRR ', 'R  R ', 'R   R'],
        'S': [' SSSS', 'S    ', ' SSS ', '    S', 'SSSS '],
        'T': ['TTTTT', '  T  ', '  T  ', '  T  ', '  T  '],
        'U': ['U   U', 'U   U', 'U   U', 'U   U', ' UUU '],
        'V': ['V   V', 'V   V', 'V   V', ' V V ', '  V  '],
        'W': ['W   W', 'W   W', 'W W W', 'WW WW', 'W   W'],
        'X': ['X   X', ' X X ', '  X  ', ' X X ', 'X   X'],
        'Y': ['Y   Y', ' Y Y ', '  Y  ', '  Y  ', '  Y  '],
        'Z': ['ZZZZZ', '   Z ', '  Z  ', ' Z   ', 'ZZZZZ'],
        ' ': ['     ', '     ', '     ', '     ', '     '],
        '!': ['  !  ', '  !  ', '  !  ', '     ', '  !  '],
        '.': ['     ', '     ', '     ', '     ', '  .  '],
        ',': ['     ', '     ', '     ', '  ,  ', ' ,   '],
        '?': ['?????', '     ', '  ?? ', '     ', '  ?  '],
        '@': [' @@@ ', '@   @', '@ @@@', '@     ', ' @@@ '],
        '#': ['  #  ', ' ### ', '#####', ' ### ', '  #  '],
        '$': [' $$$ ', '$ $  ', ' $$$ ', '  $ $', '$$$  '],
        '%': ['%   %', '   % ', '  %  ', ' %   ', '%   %'],
        '&': [' &&& ', '&   &', ' &&& ', '&  & ', ' &&&&'],
        '*': ['     ', '* * *', '  *  ', '* * *', '     '],
        '(': ['  (  ', ' (   ', ' (   ', ' (   ', '  (  '],
        ')': ['  )  ', '   ) ', '   ) ', '   ) ', '  )  '],
        '-': ['     ', '     ', ' --- ', '     ', '     '],
        '_': ['     ', '     ', '     ', '     ', '_____'],
        '=': ['     ', '=====', '     ', '=====', '     '],
        '+': ['     ', '  +  ', ' +++ ', '  +  ', '     '],
        '/': ['    /', '   / ', '  /  ', ' /   ', '/    '],
        '\\': ['\\    ', ' \\   ', '  \\  ', '   \\ ', '    \\'],
        '|': ['  |  ', '  |  ', '  |  ', '  |  ', '  |  '],
        ':': ['     ', '  :  ', '     ', '  :  ', '     '],
        ';': ['     ', '  ;  ', '     ', '  ;  ', ' ;   '],
        '\'': ['  \'  ', '  \'  ', '     ', '     ', '     '],
        '\"': [' \" \" ', ' \" \" ', '     ', '     ', '     '],
        '<': ['   < ', '  <  ', ' <   ', '  <  ', '   < '],
        '>': [' >   ', '  >  ', '   > ', '  >  ', ' >   '],
        '[': [' [[  ', ' [   ', ' [   ', ' [   ', ' [[  '],
        ']': ['  ]] ', '   ] ', '   ] ', '   ] ', '  ]] '],
        '{': ['  {{ ', ' {   ', ' {{  ', ' {   ', '  {{ '],
        '}': [' }}  ', '   } ', '  }} ', '   } ', ' }}  '],
        '0': [' 000 ', '0   0', '0   0', '0   0', ' 000 '],
        '1': ['  11 ', ' 1 1 ', '   1 ', '   1 ', ' 111 '],
        '2': [' 222 ', '2   2', '   2 ', '  2  ', '22222'],
        '3': [' 333 ', '3   3', '   33', '3   3', ' 333 '],
        '4': ['4   4', '4   4', '44444', '    4', '    4'],
        '5': ['55555', '5    ', '5555 ', '    5', '5555 '],
        '6': [' 666 ', '6    ', '6666 ', '6   6', ' 666 '],
        '7': ['77777', '   7 ', '  7  ', ' 7   ', '7    '],
        '8': [' 888 ', '8   8', ' 888 ', '8   8', ' 888 '],
        '9': [' 999 ', '9   9', ' 9999', '    9', ' 999 '],
    }
    # Iterate over each row of the ASCII art for each character in the text
    for i in range(5):
        for char in text:
            # Print each row of the ASCII art for the character
            print(characters[char][i], end='  ')
        print()  # Move to the next line

# Example usage
print_banner("WELLCOME")


<!--
**mrcaos/mrcaos** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.


Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
