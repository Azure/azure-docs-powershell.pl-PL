---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: 55ef0d4ef714c1d434915def403f5560244a3697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719601"
---
# New-AzureRmApiManagementProperty

## STRESZCZENIe
Tworzy nową właściwość.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmApiManagementProperty** tworzy **Właściwość** zarządzania interfejsem Azure API.

## Przykłady

### Przykład 1. Tworzenie właściwości zawierającej Tagi
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.

Drugie polecenie tworzy właściwość i przypisuje ciągi w $Tags jako znaczniki we właściwości.

### Przykład 2: Tworzenie właściwości zawierającej tajną wartość
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

To polecenie tworzy **Właściwość** z zaszyfrowaną wartością.

## PARAMETRÓW

### -Context
Określa obiekt **PsApiManagementContext** .

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę właściwości tworzonego polecenia cmdlet.
Maksymalna długość to 100 znaków.
Nazwy zawierają tylko litery, cyfry, kropkę, kreskę i znaki podkreślenia.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PropertyId
Określa identyfikator właściwości.
Maksymalna długość to 256 znaków.
Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.

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

### -Secret
Wskazuje, że wartość właściwości jest kluczem tajnym i powinna być szyfrowana.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Tagi, które mają być skojarzone z właściwością. Ten parametr jest opcjonalny.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Określa wartość właściwości.
Ta wartość może zawierać wyrażenia zasad.
Maksymalna długość to 1000 znaków.
Wartość nie może być pusta ani zawierać tylko odstępu.

```yaml
Type: String
Parameter Sets: (All)
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
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzureRmApiManagementProperty](./Remove-AzureRmApiManagementProperty.md)

[Set-AzureRmApiManagementProperty](./Set-AzureRmApiManagementProperty.md)


