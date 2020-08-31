# apkName

Change output apk name using build.gradle

         android {
             applicationVariants.all { variant ->
                variant.outputs.all {
                def flavor = variant.productFlavors[0].name.capitalize()
                def version = variant.versionName
                def date = new Date()
                def formattedDate = date.format('ddMMyy')
                outputFileName = "AppName${flavor}${version}_${formattedDate}.apk"
             }
           }
        }
