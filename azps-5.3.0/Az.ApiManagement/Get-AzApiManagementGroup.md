---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502491"
---
# Get-AzApiManagementGroup

## STRESZCZENIe
Pobiera wszystkie lub określone grupy zarządzania API.

## POLECENIA

### GetAllGroups (domyślny)
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByGroupId
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByUserId
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByProductId
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzApiManagementGroup** pobiera wszystkie lub określone grupy zarządzania API.

## Przykłady

### Przykład 1: pobieranie wszystkich grup
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

To polecenie pobiera wszystkie grupy.

### Przykład 2: Uzyskiwanie grupy według identyfikatorów
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

To polecenie pobiera identyfikator grupy o nazwie 0123456789.

### Przykład 3: pobieranie grupy według nazwy
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

To polecenie uzyskuje grupę o nazwie Group0002.

### Przykład 4: pobieranie wszystkich grup użytkowników
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

To polecenie pobiera wszystkie grupy użytkowników o IDENTYFIKATORze użytkownika o nazwie 0123456789.

## PARAMETRÓW

### -Context
Określa wystąpienie PsApiManagementContext.

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

### -GroupId
Określa identyfikator grupy.
Jeśli jest określony, polecenie cmdlet próbuje znaleźć grupę według identyfikatora.

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę grupy zarządzania.

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

### -ProductId
Identyfikator istniejącego produktu.
Jeśli ta grupa zostanie wybrana, zostaną zwrócone wszystkie grupy, do których przypisano produkt.
Ten parametr jest opcjonalny.

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserId
Określa identyfikator istniejącego produktu.
Jeśli zostanie określona, polecenie cmdlet zwróci wszystkie grupy, do których przypisano produkt.

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
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

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzApiManagementGroup](./New-AzApiManagementGroup.md)

[Remove-AzApiManagementGroup](./Remove-AzApiManagementGroup.md)

[Set-AzApiManagementGroup](./Set-AzApiManagementGroup.md)


