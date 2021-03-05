---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 475c4ab3105aa8ae01543c0f3674d5d119604a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009825"
---
# Set-AzAutomationModule

## SYNOPSIS
Aktualizuje moduł w automatyzacji.

## SKŁADNIA

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzAutomationModule** aktualizuje moduł w usłudze Azure Automation.
To polecenie akceptuje plik skompresowany z rozszerzeniem nazwy pliku zip.
Plik zawiera folder zawierający plik, który jest jednym z następujących typów: 
- wps_2, który ma rozszerzenie nazwy pliku psm1 lub dll 
- wps_2 manifestu modułu, który ma rozszerzenie nazwy pliku psd1: nazwa pliku zip, nazwa folderu i nazwa pliku w folderze muszą być takie same.
Określ plik zip jako adres URL, do który może uzyskać dostęp usługa automatyzacji.
W przypadku importowania modułu wps_2 do automatyzacji za pomocą tego polecenia cmdlet lub New-AzAutomationModule cmdlet operacja jest asynchroniczna.
Polecenie zakończy się powodzeniem lub niepowodzeniem importowania.
Aby sprawdzić, czy się powiodło, uruchom następujące polecenie: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Check the **ProvisioningState property** for a value of Succeeded (Pomyślnie).

## PRZYKŁADY

### Przykład 1. Aktualizowanie modułu
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

To polecenie importuje zaktualizowaną wersję istniejącego modułu o nazwie ContosoModule do konta automatyzacji o nazwie Contoso17.  Moduł jest przechowywany w obiekcie blob platformy Azure na koncie magazynu o nazwie contosostorage i kontenerze o nazwanych modułach.

## PARAMETERS

### -AutomationAccountName
Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet aktualizuje moduł.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkUri
Określa adres URL pliku zip zawierającego nową wersję modułu importowanego przez to polecenie cmdlet.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - ContentLinkVersion
Określa wersję modułu, dla którego to polecenie cmdlet aktualizuje automatyzację.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — Nazwa
Określa nazwę modułu importowanego przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, dla której to polecenie cmdlet aktualizuje moduł.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### System.Uri

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Automation.Model.Module

## NOTATKI

## LINKI POKREWNE

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[New-AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


