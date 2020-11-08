---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054677"
---
# Add-AzureWebRole

## STRESZCZENIe
Dodaje rolę pracownika sieci Web.

## POLECENIA

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Add-AzureWebRole** umożliwia dodanie roli pracownika sieci Web.

## Przykłady

### Przykład 1. Dodaj domyślną rolę
```
PS C:\> Add-AzureWebRole
```

To polecenie dodaje rolę sieci Web, która ma domyślną konfigurację Webrole1 jako nazwę i jedno wystąpienie.

### Przykład 2: Dodawanie roli o nazwie
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

To polecenie dodaje pojedynczą rolę sieci Web o nazwie MyWebRole do bieżącej aplikacji.

### Przykład 3: Dodawanie roli z nazwą i liczbą wystąpień
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

To polecenie dodaje rolę sieci Web o nazwie MyWebRole do bieżącej aplikacji.
Polecenie cmdlet ma liczbę wystąpień roli 2.

### Przykład 4: Dodawanie roli o nazwie i szablonie
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

To polecenie dodaje pojedynczą rolę sieci Web o nazwie MyWebRole do bieżącej aplikacji.
Polecenie określa folder o nazwie MyWebTemplateFolder jako szablon szkieletu.

## PARAMETRÓW

### -Wystąpienia
Określa liczbę wystąpień.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę roli sieci Web.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -TemplateFolder
Określa folder szablonów.

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

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureWorkerRole](./Add-AzureWorkerRole.md)

[Nowe — AzureRoleTemplate](./New-AzureRoleTemplate.md)


