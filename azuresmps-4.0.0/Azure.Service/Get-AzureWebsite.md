---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055240"
---
# Get-AzureWebsite

## STRESZCZENIe
Pobiera witryny sieci Web platformy Azure w bieżącej subskrypcji.

## POLECENIA

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureWebsite** pobiera informacje o witrynach sieci Web platformy Azure w bieżącej subskrypcji.

Domyślnie funkcja **Get-AzureWebsite** pobiera wszystkie witryny sieci Web platformy Azure w bieżącej subskrypcji i zwraca obiekt, który dostarcza podstawowych informacji o witrynach.
Gdy jest używany parametr *name* , funkcja **Get-AzureWebsite** zwraca obiekt z obszernymi informacjami, w tym szczegóły konfiguracji.

Bieżący abonament to subskrypcja określona jako "Bieżąca". Aby znaleźć bieżącą subskrypcję, użyj *bieżącego* parametru polecenia cmdlet [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .
Aby zmienić bieżącą subskrypcję, użyj polecenia cmdlet [SELECT-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .

W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

## Przykłady

### Przykład 1: uzyskiwanie wszystkich witryn internetowych w ramach subskrypcji
```
PS C:\> Get-AzureWebsite
```

To polecenie umożliwia pobieranie wszystkich witryn sieci Web platformy Azure w bieżącej subskrypcji.

### Przykład 2: Uzyskaj witrynę internetową według nazwy
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

To polecenie zawiera szczegółowe informacje na temat witryny sieci Web usługi ContosoWeb Azure, w tym informacje o konfiguracji.
Gdy jest używany parametr *name* , funkcja **Get-AzureWebsite** zwraca obiekt **SiteWithConfig** z rozszerzonymi informacjami na temat witryny sieci Web.

### Przykład 3: uzyskiwanie szczegółowych informacji o wszystkich witrynach internetowych
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

To polecenie umożliwia pobieranie szczegółowych informacji o wszystkich witrynach internetowych w ramach subskrypcji.
Korzysta z polecenia **Get-AzureWebsite** w celu uzyskania wszystkich witryn internetowych, a następnie użyto polecenia cmdlet **-Object** cmdlet w celu uzyskania każdej witryny sieci Web według nazwy.

### Przykład 4: uzyskiwanie informacji o miejscu wdrożenia
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

To polecenie umożliwia wyświetlenie miejsca do wdrożenia przemieszczania w witrynie internetowej ContosoWeb.
Miejsca wdrażania umożliwiają testowanie różnych wersji witryny usługi Azure w sieci Web bez konieczności ich publicznego udostępnienia.

### Przykład 5: uzyskiwanie wystąpień witryny sieci Web
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

W poleceniach w tym przykładzie użyto właściwości Instances witryny sieci Web platformy Azure, aby uzyskać informacje o obecnie uruchomionych wystąpieniach witryn.
Właściwość **Instances** została dodana do obiektu **SiteWithConfig** w wersji 0.8.3 modułu platformy Azure.

Pierwsze polecenie pobiera identyfikatory wystąpienia wszystkich obecnie uruchomionych wystąpień witryny sieci Web.
Drugie polecenie pobiera liczbę uruchomionych wystąpień witryny sieci Web.
Właściwości **Count** można użyć w dowolnej tablicy.

## PARAMETRÓW

### -Name (nazwa)
Pobiera szczegółowe informacje o konfiguracji dotyczące określonej witryny sieci Web.
Wprowadź nazwę jednej witryny sieci Web w subskrypcji.
Domyślnie polecenie **Get-AzureWebsite** pobiera wszystkie witryny sieci Web w bieżącej subskrypcji.
Wartość *nazwy* nie obsługuje symboli wieloznacznych.

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
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### -Slot
Pobiera określone miejsce wdrożenia witryny sieci Web.
Wprowadź nazwę miejsca, na przykład "przemieszczanie" lub "produkcja".
Aby uzyskać więcej informacji na temat miejsc wdrożenia, zobacz Wdrażanie etapowe w witrynach usługi Microsoft Azure w sieci Web https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .
Aby dodać miejsce wdrożenia do istniejącej witryny internetowej platformy Azure, użyj polecenia cmdlet Set-AzureWebsite.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Utilities. Web. Services. webentities. witryna
Domyślnie funkcja **Get-AzureWebsite** zwraca tablicę obiektów **witryny** .

### Microsoft. platformy windowsazure. Commands. Utilities. Web. Services. webentities. SiteWithConfig
Gdy jest używany parametr *name* , funkcja **Get-AzureWebsite** zwraca obiekt **SiteWithConfig** .

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start — AzureWebsite](./Start-AzureWebsite.md)

[Zatrzymaj — AzureWebsite](./Stop-AzureWebsite.md)

[Pokaż — AzureWebsite](./Show-AzureWebsite.md)


