---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: e6aec3bc5d19cc89d6d2e854815fd78c5788fdb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710532"
---
# New-AzAutomationModule

## STRESZCZENIe
Importuje moduł do automatyzacji.

## POLECENIA

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzAutomationModule** importuje moduł do usługi Azure Automation.
To polecenie akceptuje plik skompresowany z rozszerzeniem nazwy pliku zip.
Plik zawiera folder zawierający plik z jednym z następujących typów: 
- Moduł wps_2, który ma rozszerzenie nazwy pliku PSM1 lub dll 
- Manifest modułu wps_2, który ma rozszerzenie nazwy pliku psd1 nazwa pliku zip, nazwa folderu i nazwa pliku w folderze, muszą być takie same.
Określ plik zip jako adres URL, do którego usługa automatyzacji może uzyskać dostęp.
W przypadku zaimportowania modułu wps_2 do automatyzacji za pomocą tego polecenia cmdlet lub polecenia cmdlet Set-AzAutomationModule operacja jest asynchroniczna.
Polecenie kończy się, czy importowanie powiedzie się, czy nie.
Aby sprawdzić, czy to powiodło, uruchom następujące polecenie: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Sprawdź, czy właściwość **ProvisioningState** została pomyślnie zakończona.

## Przykłady

### Przykład 1: Importowanie modułu
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

To polecenie importuje moduł o nazwie ContosoModule do konta usługi Automation o nazwie Contoso17.
Moduł jest przechowywany w obiekcie blob platformy Azure na koncie magazynu o nazwie contosostorage i kontenerze o nazwie moduły.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet importuje moduł.

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
Adres URL do pakietu zip modułu

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
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
Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje moduł.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. URI

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. module

## INFORMACYJN

## LINKI POKREWNE

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


