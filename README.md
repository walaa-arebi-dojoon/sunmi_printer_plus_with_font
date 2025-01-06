
# Sunmi printer 
this package is forked from https://pub.dev/packages/sunmi_printer_plus
i added the ability to change font family 

the list of fonts i added 
enum SunmiTextStyleFontFamily {
  SOMAR,
  RAKKAS,
  PLAYWRITE,
  DANCING_SCRIPT,
  DEFAULT
}


to add a font you would like to use foloow the steps in commit 532c66f351966e9a3072adbefb1ace07d4a2bb15

1- add your font to android/src/main/assets

2- in android/src/main/kotlin/br/com/brasizza/sunmi_printer_plus/SunmiPrinterClass.kt  you can find 
```
      private fun getFontFamily(fontFamily: String?): String {
          return when (fontFamily) {
              "SOMAR" -> "somar.ttf"
              "PLAYWRITE" -> "Playwrite.ttf"
              "RAKKAS" -> "Rakkas-Regular.ttf"
              "DANCING_SCRIPT" -> "DancingScript.ttf"
              
              else -> ""
          }
      }
```
add your font enum name and font file name

3- in lib/core/enums/enums.dart you can find 
```
enum SunmiTextStyleFontFamily {
  /// give somar font family to your text.
  SOMAR,

  /// give Khediawy font family to your text.
  RAKKAS,

  /// give Playwrite font family to your text.
  PLAYWRITE,

  /// give DancingScript font family to your text.
  DANCING_SCRIPT,

  DEFAULT

  ///add more fonts here
}
```

add the enum of your font name 

you are ready to go !
