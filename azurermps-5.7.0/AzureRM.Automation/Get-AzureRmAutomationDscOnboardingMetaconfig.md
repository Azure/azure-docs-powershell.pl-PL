---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 34dcb85de9520882b9202edd38ae2e44d1bcafee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718963"
---
# Get-AzureRmAutomationDscOnboardingMetaconfig

## STRESZCZENIe
Tworzy plik meta-Configuration. mof.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmAutomationDscOnboardingMetaconfig** powoduje utworzenie plików MOF (APS) o konfiguracji pożądanego stanu (DSC).
To polecenie cmdlet tworzy plik MOF dla każdej określonej nazwy komputera.
Polecenie cmdlet tworzy folder dla plików MOF.
Możesz uruchomić polecenie cmdlet Set-DscLocalConfigurationManager dla tego folderu, aby dołączać te komputery do konta usługi Azure Automation jako węzłów DSC.

## Przykłady

### Przykład 1: serwer dołączający do automatyzacji DSC
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

Pierwsze polecenie powoduje utworzenie plików meta konfiguracji DSC dla dwóch serwerów dla konta usługi Automation o nazwie Contoso17.
Polecenie zapisuje te pliki na komputerze stacjonarnym.

Drugie polecenie używa polecenia cmdlet **Set-DscLocalConfigurationManager** w celu zastosowania konfiguracji meta do określonych komputerów jako węzłów DSC.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji.
Możesz dołączać komputery, które parametr *ComputerName* określa konto, które określa ten parametr.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ComputerName
Określa tablicę nazw komputerów, dla których to polecenie cmdlet generuje pliki MOF.
Jeśli nie podano tego parametru, polecenie cmdlet generuje plik MOF dla bieżącego komputera (localhost).

```yaml
Type: String[]
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie i zastąpienie istniejących plików MOF o tej samej nazwie.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFolder
Określa nazwę folderu, w którym to polecenie cmdlet przechowuje pliki MOF.

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

### -ResourceGroupName
Określa nazwę grupy zasobów.
To polecenie cmdlet tworzy pliki MOF na komputerach stacjonarnych w grupie zasobów, którą określa ten parametr.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. DscOnboardingMetaconfig

## INFORMACYJN

## LINKI POKREWNE

