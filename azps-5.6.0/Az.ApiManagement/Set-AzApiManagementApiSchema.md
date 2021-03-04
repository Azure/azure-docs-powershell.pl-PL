---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 3cacc873684844ddb97f9cf125e2b2482747b470
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959841"
---
# Set-AzApiManagementApiSchema

## SYNOPSIS
Modyfikuje schemat interfejsu API

## SKŁADNIA

### ExpandedParameters (domyślne)
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzApiManagementApiSchema** modyfikuje schemat interfejsu API zarządzania interfejsami API platformy Azure.

## PRZYKŁADY

### Przykład 1. Modyfikuje schemat interfejsu API
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

Przykład aktualizacji schematu interfejsu API

### Przykład 2

Modyfikuje schemat interfejsu API. (wygenerowane automatycznie)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementApiSchema -ApiId 'echo-api' -Context <PsApiManagementContext> -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json -SchemaId '2'
```

## PARAMETERS

### -ApiId
Identyfikator istniejącego interfejsu API.
Ten parametr jest wymagany.

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — kontekst
Wystąpienie tekstu PsApiManagementContext.
Ten parametr jest wymagany.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -InputObject
Wystąpienie obiektu PsApiManagementApiSchema.
Ten parametr jest wymagany.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Jeśli określono, wówczas wystąpienie microsoft.azure.commands.apiManagement.ServiceManagement.Models.PsApiManagementApi typ reprezentujący zestaw interfejs API.

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

### -ResourceId
Arm ResourceId schematu diagnostycznego lub api. Ten parametr jest wymagany.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SchemaDocument
Dokument schematu interfejsu API jako ciąg znaków. Ten parametr jest wymagany. Nie określono parametru SchemaDocumentFile.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchemaDocumentContentType
ContentType schematu interfejsu API. Ten parametr jest opcjonalny.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchemaDocumentFilePath
Ścieżka pliku dokumentu schematu interfejsu API. Ten parametr jest wymagany. Nie określono parametru SchemaDocument.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SchemaId
Identyfikator istniejącego schematu.
Ten parametr jest wymagany.

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext

### System.String

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema

### System.Management.Automation.SwitchParameters

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi

## NOTATKI

## LINKI POKREWNE

[Get-AzApiManagementApiSchema](./Get-AzApiManagementApiSchema.md)

[New-AzApiManagementApiSchema](./New-AzApiManagementApiSchema.md)

[Remove-AzApiManagementApiSchema](./Remove-AzApiManagementApiSchema.md)

