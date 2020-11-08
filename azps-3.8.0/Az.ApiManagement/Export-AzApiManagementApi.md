---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050925"
---
# Export-AzApiManagementApi

## STRESZCZENIe
Eksportuje interfejs API do pliku.

## POLECENIA

### ExportToPipeline (domyślny)
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ExportToFile
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Export-AzApiManagementApi** eksportuje interfejs API zarządzania interfejsem Azure API do pliku w jednym z obsługiwanych formatów.

## Przykłady

### Przykład 1: eksportowanie interfejsu API w formacie programu Web Application Description Language (WADL)
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

To polecenie eksportuje interfejs API do pliku WADL.

### Przykład 2: eksportowanie interfejsu API w programie OpenApi 3,0 format specyfikacji jako dokumentu JSON
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

To polecenie eksportuje definicje interfejsów API w otwartym formacie API jako dokument JSON.

## PARAMETRÓW

### -ApiId
Określa identyfikator interfejsu API do wyeksportowania.

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
Identyfikator wersji interfejsu API. Ten parametr jest opcjonalny. Jeśli ta pozycja nie zostanie określona, zostanie wyeksportowana wersja aktualnie aktywnej wersji API.

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
Określa obiekt **PsApiManagementContext** .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Wskazuje, że ta operacja zastępuje plik o tej samej nazwie, jeśli już istnieje.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Wskazuje, że ta operacja zwraca wartość $True, jeśli interfejs API został pomyślnie wyeksportowany lub $False w inny sposób.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SaveAs
Określa ścieżkę pliku, do którego ma zostać zapisany wyeksportowany interfejs API.

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SpecificationFormat
Określa format interfejsu API.
psdx_paramvalues WADL, WSDL, Swagger, OpenApi i OpenApiJson

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext

### System. String

### Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiFormat

### System. Management. Automation. SwitchParameter

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE

[Get-AzApiManagementApi](./Get-AzApiManagementApi.md)

[Import — AzApiManagementApi](./Import-AzApiManagementApi.md)

[Nowe — AzApiManagementApi](./New-AzApiManagementApi.md)

[Remove-AzApiManagementApi](./Remove-AzApiManagementApi.md)

[Set-AzApiManagementApi](./Set-AzApiManagementApi.md)


