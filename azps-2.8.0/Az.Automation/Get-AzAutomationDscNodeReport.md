---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: a8d0244b9a26616e796a4e867a193da4ed3888d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706820"
---
# Get-AzAutomationDscNodeReport

## STRESZCZENIe
Umożliwia pobieranie raportów wysłanych z węzła DSC do automatyzacji.

## POLECENIA

### ByAll (domyślny)
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByLatest
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzAutomationDscNodeReport** pobiera raporty wysyłane z węzła APS (Konfiguracja stanu żądanego) do usługi Azure Automation.

## Przykłady

### Przykład 1. pobieranie wszystkich raportów dla węzła DSC
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Computer14 na koncie automatyzacji o nazwie Contoso17.
Polecenie zapisuje ten obiekt w zmiennej $Node.
Drugie polecenie pobiera metadane wszystkich raportów wysyłanych z węzła DSC o nazwie Computer14 do konta usługi Automation o nazwie Contoso17.
Polecenie określa węzeł za pomocą właściwości **Identyfikator** obiektu $Node.

### Przykład 2: uzyskiwanie raportu dla węzła DSC według identyfikatora raportu
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Computer14 na koncie automatyzacji o nazwie Contoso17.
Polecenie zapisuje ten obiekt w zmiennej $Node.
Drugie polecenie pobiera metadane dla raportu określonego IDENTYFIKATORem wysłanym z węzła DSC o nazwie Computer14 do konta usługi Automation o nazwie Contoso17.

### Przykład 3: uzyskiwanie najnowszego raportu dla węzła DSC
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Computer14 na koncie automatyzacji o nazwie Contoso17.
Polecenie zapisuje ten obiekt w zmiennej $Node.
Drugie polecenie pobiera metadane najnowszego raportu wysłanego z węzła DSC o nazwie Computer14 do konta usługi Automation o nazwie Contoso17.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji.
To polecenie cmdlet powoduje wyeksportowanie raportów dla węzła DSC należącego do konta, które jest określone przez ten parametr.

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

### -EndTime
Określa godzinę zakończenia.
To polecenie cmdlet umożliwia pobieranie raportów, które zostały odebrane przed upływem tego czasu.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Określa unikatowy identyfikator raportu węzła DSC dla tego polecenia cmdlet, który ma zostać wyświetlony.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Najnowsze
Wskazuje, że ten aplet polecenia pobiera najnowszy raport DSC tylko dla określonego węzła.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeId
Określa unikatowy identyfikator węzła DSC, dla którego ten aplet polecenia pobiera raporty.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej węzeł DSC, dla którego ten aplet polecenia pobiera raporty.

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

### -StartTime
Określa godzinę rozpoczęcia.
To polecenie cmdlet umożliwia pobieranie raportów, które zostały odebrane po upływie tego czasu.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. GUID

### System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. DscNode

## INFORMACYJN

## LINKI POKREWNE

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Eksportowanie — AzAutomationDscNodeReportContent](./Export-AzAutomationDscNodeReportContent.md)


