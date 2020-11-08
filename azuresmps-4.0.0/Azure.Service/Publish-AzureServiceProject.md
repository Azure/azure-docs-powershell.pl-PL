---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054849"
---
# Publish-AzureServiceProject

## STRESZCZENIe
Publikowanie bieżącej usługi na platformie Windows Azure.

## POLECENIA

### PublishFromServiceDefinition (domyślny)
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### PublishFromPackage
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Publish-AzureServiceProject** umożliwia publikowanie bieżącej usługi w chmurze.
Możesz określić konfigurację publikowania (taką jak **subskrypcja** , **StorageAccountName** , **Lokalizacja** , miejsce **) w** wierszu polecenia lub w ustawieniach lokalnych za pomocą polecenia cmdlet **Set-AzureServiceProject** .

## Przykłady

### Przykład 1. publikowanie projektu usługi z wartościami domyślnymi
```
PS C:\> Publish-AzureServiceProject
```

W tym przykładzie jest publikowana bieżąca usługa przy użyciu bieżących ustawień usługi i bieżącego profilu publikowania platformy Azure.

### Przykład 2: Tworzenie pakietu wdrażania
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

W tym przykładzie przedstawiono tworzenie pliku pakietu wdrażania (cspkg) w katalogu usługi i nie można go publikować na platformie Windows Azure.

## PARAMETRÓW

### -AffinityGroup
Określa grupę koligacji, która ma być używana przez usługę.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Konfiguracja
Określa plik konfiguracji usługi.
Jeśli określisz ten parametr, określ parametr *Package* .

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Deploymentname
Określa nazwę wdrożenia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uruchom
Otwiera okno przeglądarki, w którym można wyświetlić aplikację po jej wdrożeniu.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Region, w którym aplikacja będzie hostowana.
Możliwe wartości: 
  
- W dowolnym miejscu w Azji
- Dowolne miejsce w Europie
- Dowolne miejsce w USA
- Azja Wschodnia
- Wschodnie USA
- Północno-środkowe USA
- Europa Północna
- Południowa Centrala amerykańska
- Azja Południowo-Wschodnia
- Europa Zachodnia
- Zachodnie USA
 
Jeśli nie określono lokalizacji, zostanie wykorzystana lokalizacja określona w ostatniej rozmowie z **poleceniem Set-AzureServiceProject** . Jeśli żadna lokalizacja nie została kiedykolwiek określona, lokalizacja będzie wybierana losowo z lokalizacji "Północna Centrala Amerykańska" oraz "Południowa Centrala Amerykańska".

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Package
Określa plik pakietu do wdrożenia.
Określ plik lokalny z rozszerzeniem nazwy pliku cspkg lub identyfikatorem URI obiektu BLOB zawierającego pakiet.
Jeśli określisz ten parametr, nie określaj parametru *ServiceName* .

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

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

### -ServiceName
Określa nazwę, która ma być używana w usłudze podczas publikowania na platformie Windows Azure.
Nazwa określa część etykiety w poddomenie cloudapp.net, która jest używana do zaadresowania usługi w systemie Windows Azure (czyli **name**. cloudapp.NET).
Każda nazwa określona podczas publikowania usługi zastępuje nazwę podaną w momencie utworzenia usługi.
(Zobacz polecenie cmdlet **New-AzureServiceProject** ).

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Miejsce wdrożenia, które ma być używane w tej usłudze.
Możliwe wartości to "przemieszczanie" i "produkcja".
Jeśli nie określono żadnego miejsca, zostanie użyte gniazdo podane w ostatniej rozmowie z Set-AzureDeploymentSlot.
Jeśli nie określono żadnego gniazda, zostanie użyte gniazdo "produkcja".

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Określa nazwę konta magazynu systemu Windows Azure, która ma być używana podczas publikowania usługi.
Ta wartość nie jest używana do momentu opublikowania usługi.
Jeśli ten parametr nie jest określony, wartość jest uzyskiwana z ostatniego polecenia **Set-AzureServiceProject** .
Jeśli nie określono żadnego konta magazynu, zostanie użyta nazwa konta magazynu odpowiadająca nazwie usługi.
Jeśli takie konto magazynu nie istnieje, polecenie cmdlet usiłuje utworzyć nowy.
Jednak próba może się nie powieść, jeśli konto magazynu zgodne z nazwą usługi istnieje w innej subskrypcji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


