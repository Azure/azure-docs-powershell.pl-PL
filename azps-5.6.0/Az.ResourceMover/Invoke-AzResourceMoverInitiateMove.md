---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: e075da17009c863e8c564eb5379495a1bdaff505
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999946"
---
# Invoke-AzResourceMoverInitiateMove

## SYNOPSIS
Przenosi zestaw zasobów uwzględniony w treści żądania.
Operacja przenoszenia jest wyzwalana po tym, jak moveResources znajdują się w stanie moveState "MovePending" lub "MoveFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do commitPending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.

## SKŁADNIA

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Przenosi zestaw zasobów uwzględniony w treści żądania.
Operacja przenoszenia jest wyzwalana po tym, jak moveResources znajdują się w stanie moveState "MovePending" lub "MoveFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do commitPending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.

## PRZYKŁADY

### Przykład 1. Sprawdzanie poprawności zależności przed zainicjowanie przeniesienia zasobów.
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly


AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 9:39:37 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 9:39:37 AM
Status         : Succeeded

```

Sprawdź poprawność zależności przed zainicjowanie przeniesienia zasobów.

### Przykład 2. Inicjowanie przenoszenia zestawu zasobów w kolekcji przenoszenia przy użyciu jako danych wejściowych "MoveResource Name".
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" 

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 11:56:33 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 11:55:21 AM
Status         : Succeeded

```

Zainicjuj przenoszenie zestawu zasobów w kolekcji przenoszenia, używając jako danych wejściowych "MoveResource Name".

### Przykład 3. Zainicjowanie przenoszenia zestawu zasobów w kolekcji przenoszenia przy użyciu wartości wejściowej "SourceARMID".
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:01:35 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:00:21 PM
Status         : Succeeded

```

Zainicjuj przenoszenie zestawu zasobów w kolekcji Przenoszenia, używając jako danych wejściowych "SourceARMID".

## PARAMETERS

### — AsJob
Uruchamianie polecenia jako zadania

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveCollectionName
Nazwa kolekcji przenoszenia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveResource
Pobiera lub ustawia listę identyfikatorów zasobów, domyślnie akceptuje przenoszenie identyfikatorów zasobów, chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveResourceInputType
Definiuje typ danych wejściowych zasobu przenoszenia.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Uruchamianie polecenia asynchronicznie

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Identyfikator subskrypcji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidateOnly
Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wstępnego uruchomienia.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IOperationStatus

## NOTATKI

ALIASY

## LINKI POKREWNE

