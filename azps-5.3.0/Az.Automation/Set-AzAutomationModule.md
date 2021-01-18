---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502259"
---
# Set-AzAutomationModule

## STRESZCZENIe
Umożliwia zaktualizowanie modułu w automatyzacji.

## POLECENIA

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzAutomationModule** aktualizuje moduł w usłudze Azure Automation.
To polecenie akceptuje plik skompresowany z rozszerzeniem nazwy pliku zip.
Plik zawiera folder zawierający plik z jednym z następujących typów: 
- Moduł wps_2, który ma rozszerzenie nazwy pliku PSM1 lub dll 
- Manifest modułu wps_2, który ma rozszerzenie nazwy pliku psd1 nazwa pliku zip, nazwa folderu i nazwa pliku w folderze, muszą być takie same.
Określ plik zip jako adres URL, do którego usługa automatyzacji może uzyskać dostęp.
W przypadku zaimportowania modułu wps_2 do automatyzacji za pomocą tego polecenia cmdlet lub polecenia cmdlet New-AzAutomationModule operacja jest asynchroniczna.
Polecenie kończy się, czy importowanie powiedzie się, czy nie.
Aby sprawdzić, czy to powiodło, uruchom następujące polecenie: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Sprawdź, czy właściwość **ProvisioningState** została pomyślnie zakończona.

## Przykłady

### Przykład 1: aktualizowanie modułu
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

To polecenie importuje zaktualizowaną wersję istniejącego modułu o nazwie ContosoModule do konta usługi Automation o nazwie Contoso17.  Moduł jest przechowywany w obiekcie blob platformy Azure na koncie magazynu o nazwie contosostorage i kontenerze o nazwie moduły.

## PARAMETRÓW

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
Określa adres URL pliku zip zawierającego nową wersję modułu, którego używa to polecenie cmdlet.

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

### -ContentLinkVersion
Określa wersję modułu, z którym to polecenie cmdlet aktualizuje automatyzację.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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
Określa nazwę modułu zaimportowanego za pomocą tego polecenia cmdlet.

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
Określa nazwę grupy zasobów, dla której ten aplet polecenia zaktualizuje moduł.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. URI

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. module

## INFORMACYJN

## LINKI POKREWNE

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Nowe — AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


