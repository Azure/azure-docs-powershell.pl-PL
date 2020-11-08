---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: bed6126dbd1ea57a29d041daf10a3deb05f2dc92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051187"
---
# New-AzApiManagementProperty

## STRESZCZENIe
Tworzy nową właściwość.

## POLECENIA

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzApiManagementProperty** tworzy **Właściwość** zarządzania interfejsem Azure API.

## Przykłady

### Przykład 1. Tworzenie właściwości zawierającej Tagi
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.
Drugie polecenie tworzy właściwość i przypisuje ciągi w $Tags jako znaczniki we właściwości.

### Przykład 2: Tworzenie właściwości zawierającej tajną wartość
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

To polecenie tworzy **Właściwość** z zaszyfrowaną wartością.

## PARAMETRÓW

### -Context
Określa obiekt **PsApiManagementContext** .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Type: System.String
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
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.String[]
Parameter Sets: (All)
Aliases:

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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext

### System. String

### System. Management. Automation. SwitchParameter

### System. String []

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzApiManagementProperty](./Remove-AzApiManagementProperty.md)

[Set-AzApiManagementProperty](./Set-AzApiManagementProperty.md)


