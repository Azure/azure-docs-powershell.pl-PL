---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: bb88bc38f6102f18b4d45b3b80902886975e2628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987050"
---
# Get-AzAutomationDscNodeReport

## SYNOPSIS
Pobiera raporty wysyłane z węzła DSC do automatyzacji.

## SKŁADNIA

### ByAll (Domyślne)
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

## OPIS
Polecenie **cmdlet Get-AzAutomationDscNodeReport** pobiera raporty wysyłane z węzła APS Desired State Configuration (DSC) do usługi Azure Automation.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich raportów dla węzła DSC
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.
Polecenie przechowuje ten obiekt w $Node zmienną.
Drugie polecenie pobiera metadane dla wszystkich raportów wysyłanych z węzła DSC o nazwie Komputer14 do konta automatyzacji o nazwie Contoso17.
To polecenie określa węzeł przy użyciu właściwości **Id** $Node obiektu.

### Przykład 2. Uzyskiwanie raportu dla węzła DSC według identyfikatora raportu
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.
Polecenie przechowuje ten obiekt w $Node zmienną.
Drugie polecenie pobiera metadane dla raportu wskazanego przez określony identyfikator wysłany z węzła DSC o nazwie Komputer14 do konta automatyzacji o nazwie Contoso17.

### Przykład 3. Uzyskiwanie najnowszego raportu dla węzła DSC
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

Pierwsze polecenie pobiera węzeł DSC dla komputera o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.
Polecenie przechowuje ten obiekt w $Node zmienną.
Drugie polecenie pobiera metadane dla najnowszego raportu wysyłanego z węzła DSC o nazwie Komputer14 do konta automatyzacji o nazwie Contoso17.

## PARAMETERS

### -AutomationAccountName
Określa nazwę konta automatyzacji.
To polecenie cmdlet eksportuje raporty dla węzła DSC należącego do konta, które określa ten parametr.

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

### - EndTime
Określa czas zakończenia.
To polecenie cmdlet pobiera raporty o odbieranych wcześniej automatyzacjach.

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

### — Identyfikator
Określa unikatowy identyfikator raportu węzła DSC dla tego polecenia cmdlet.

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

### — najnowsza wersja
Wskazuje, że to polecenie cmdlet pobiera najnowszy raport DSC tylko dla określonego węzła.

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

### - NodeId
Określa unikatowy identyfikator węzła DSC, dla którego to polecenie cmdlet pobiera raporty.

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
Określa nazwę grupy zasobów zawierającej węzeł DSC, dla którego to polecenie cmdlet pobiera raporty.

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

### — StartTime
Określa czas rozpoczęcia.
To polecenie cmdlet pobiera raporty, które po tym czasie otrzymano automatyzację.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.Guid

### System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Automation.Model.DscNode

## NOTATKI

## LINKI POKREWNE

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Export-AzAutomationDscNodeReportContent](./Export-AzAutomationDscNodeReportContent.md)


