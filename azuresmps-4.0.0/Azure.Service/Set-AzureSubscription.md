---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054916"
---
# Set-AzureSubscription

## STRESZCZENIe
Zmienia subskrypcję platformy Azure.

## POLECENIA

### UpdateSubscriptionByIdParameterSetName (domyślny)
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UpdateSubscriptionByNameParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AddSubscriptionParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureSubscription** ustala i zmienia właściwości obiektu subskrypcji platformy Azure.
Za pomocą tego polecenia cmdlet można pracować w ramach subskrypcji platformy Azure, która nie jest domyślną subskrypcją, ani na zmianę bieżącego konta magazynu.
Aby uzyskać informacje o bieżących i domyślnych subskrypcjach, zobacz polecenie cmdlet **SELECT-AzureSubscription** .

To polecenie cmdlet działa w ramach obiektu subskrypcji platformy Azure, a nie Twojej bieżącej subskrypcji platformy Azure.
Aby utworzyć i zainicjować obsługę administracyjną subskrypcji platformy Azure, odwiedź witrynę [Azure Portal](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .

To polecenie cmdlet zmienia dane w pliku danych subskrypcji, które tworzysz po użyciu polecenia cmdlet **Add-AzureAccount** lub **Import-AzurePublishSettingsFile** w celu dodania konta platformy Azure do programu Windows PowerShell.

W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

## Przykłady

### Przykład 1. Jeśli zmienisz istniejące subscription1
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

W tym przykładzie zmienisz certyfikat subskrypcji o nazwie ContosoEngineering.

### Przykład 2: zmienianie punktu końcowego usługi
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

To polecenie umożliwia dodanie lub zmianę niestandardowego punktu końcowego usługi dla subskrypcji ContosoEngineering.

### Przykład 3: czyszczenie wartości właściwości
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

To polecenie ustawia wartości właściwości certyfikat i ResourceManagerEndpoint na null ($Null).
Spowoduje to wyczyszczenie wartości tych właściwości bez zmieniania innych ustawień.

### Przykład 4: używanie alternatywnego pliku danych subskrypcji
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

To polecenie powoduje zmianę bieżącego konta magazynu subskrypcji usługi ContosoFinance na ContosoStorage01.
W poleceniu użyto parametru **SubscriptionDataFile** w celu zmiany danych w pliku danych subskrypcji C:\Azure\SubscriptionData.xml.
Domyślnie funkcja **Set-AzureSubscription** używa domyślnego pliku danych subskrypcji w profilu użytkownika mobilnego.

## PARAMETRÓW

### -Certificate
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CurrentStorageAccountName
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Środowisko
Określa środowisko Azure.

Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.
Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.
Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Zwraca wartość $True, jeśli wykonanie polecenia powiedzie się i $False, jeśli nie powiodło się.
Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet. Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceManagerEndpoint
Określa punkt końcowy danych Menedżera zasobów platformy Azure, w tym dane dotyczące grup zasobów skojarzonych z kontem.
Aby uzyskać więcej informacji na temat Menedżera zasobów platformy Azure, zobacz [polecenia cmdlet Menedżera zasobów platformy Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) i [Używanie programu Windows PowerShell z Menedżerem zasobów](https://go.microsoft.com/fwlink/?LinkID=394767)  () https://go.microsoft.com/fwlink/?LinkID=394767) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subskrypcji
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.

## WYSYŁA

### Brak lub system. Boolean
Po użyciu parametru *PassThru* to polecenie cmdlet zwraca wartość logiczną.
Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureAccount](./Add-AzureAccount.md)

[Get-AzureSubscription](./Get-AzureSubscription.md)

[Import — AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Wybierz — AzureSubscription](./Select-AzureSubscription.md)


