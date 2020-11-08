---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050895"
---
# Get-AzApiManagementOperation

## STRESZCZENIe
Pobiera listę lub określoną operację interfejsu API.

## POLECENIA

### GetAllApiOperations (domyślny)
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetById
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
**Element get-AzApiManagementOperation** pobiera listę lub określoną operację interfejsu API.

## Przykłady

### Przykład 1: uzyskiwanie wszystkich operacji zarządzania interfejsem API
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

To polecenie pobiera wszystkie operacje zarządzania interfejsem API.

### Przykład 2: uzyskiwanie operacji zarządzania interfejsem API według identyfikatora operacji
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

To polecenie pobiera operację zarządzania interfejsem API, podając Identyfikator operacji o nazwie Operation0003.

## PARAMETRÓW

### -ApiId
Określa identyfikator operacji interfejsu API.

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

### -ApiRevision
Identyfikator wersji interfejsu API. Ten parametr jest opcjonalny. Jeśli nie określono tej funkcji, operacja zostanie pobrana z obecnej aktywnej wersji interfejsu API.

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

### -Context
Określa wystąpienie obiektu **PsApiManagementContext** .

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

### -OperationId
Określa identyfikator operacji.

```yaml
Type: System.String
Parameter Sets: GetById
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

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzApiManagementOperation](./New-AzApiManagementOperation.md)

[Remove-AzApiManagementOperation](./Remove-AzApiManagementOperation.md)

[Set-AzApiManagementOperation](./Set-AzApiManagementOperation.md)


