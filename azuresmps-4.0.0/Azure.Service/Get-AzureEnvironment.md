---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055318"
---
# Get-AzureEnvironment

## STRESZCZENIe
Pobiera środowiska Azure

## POLECENIA

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureEnvironment** pobiera środowiska platformy Azure dostępne dla programu Windows PowerShell.

Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.
Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.
Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

Polecenie cmdlet **Get-AzureEnvironment** pobiera środowiska z pliku danych abonamentu, a nie z platformy Azure.
Jeśli plik danych subskrypcji jest nieaktualny, uruchom polecenie cmdlet **Add-AzureAccount** lub **Import-PublishSettingsFile** , aby je odświeżyć.

W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

## Przykłady

### Przykład 1. Pobierz wszystkie środowiska
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

To polecenie uzyskuje wszystkie środowiska dostępne w programie Windows PowerShell.

### Przykład 2: uzyskiwanie środowiska według nazwy
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

W tym przykładzie jest pobierany środowisko AzureCloud.

### Przykład 3: pobieranie wszystkich właściwości we wszystkich środowiskach
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

To polecenie pobiera wszystkie właściwości wszystkich środowisk.

W poleceniu użyto polecenia cmdlet **Get-AzureEnvironment** w celu uzyskania wszystkich środowisk Azure dla tego konta.
Następnie korzysta z polecenia cmdlet **ForEach-Object** , aby uruchomić polecenie **Get-AzureEnvironment** z parametrem **name** w każdym środowisku.
Wartość parametru **name** to właściwość **EnvironmentName** każdego środowiska.

Bez parametrów polecenie **Get-AzureEnvironment** pobiera tylko wybrane właściwości środowiska.

## PARAMETRÓW

### -Name (nazwa)
Pobiera tylko określone środowisko.
Wpisz nazwę środowiska.
W wartości parametru jest uwzględniana wielkość liter.
Znaki wieloznaczne są niedozwolone.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.

## WYSYŁA

### System. Management. Automation. PSCustomObject
Domyślnie funkcja **Get-AzureEnvironment** zwraca obiekt niestandardowy.

### Microsoft. platformy windowsazure. Commands. Utilities. Common. WindowsAzureEnvironment
Po uruchomieniu funkcji **Get-AzureEnvironment** z parametrem **name** zwraca obiekt  **WindowsAzureEnvironment** .

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureAccount](./Add-AzureAccount.md)

[Dodaj-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import — AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


