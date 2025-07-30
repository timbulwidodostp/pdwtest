# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Durbin-Watson test for serial correlation in panel models Use pdwtest (plm) With (In) R Software
install.packages("plm")
library("plm")
pdwtest = read.csv("https://raw.githubusercontent.com/timbulwidodostp/pdwtest/main/pdwtest/pdwtest.csv",sep = ";")
# Estimation Durbin-Watson test for serial correlation in panel models Use pdwtest (plm) With (In) R Software
# Model Common Effect
Common = plm (Dependen ~ Indenpenden_1 + Indenpenden_2, data = pdwtest, effect = "twoways", model = "pooling")
pdwtest(Common)
# Model Fixed Effect
Fixed = plm (Dependen ~ Indenpenden_1 + Indenpenden_2, data = pdwtest, effect = "twoways", model = "within")
pdwtest(Fixed)
# Model Random Effect
Random = plm (Dependen ~ Indenpenden_1 + Indenpenden_2, data = pdwtest, effect = "twoways", model = "random")
pdwtest(Random)
# Durbin-Watson test for serial correlation in panel models Use pdwtest (plm) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished