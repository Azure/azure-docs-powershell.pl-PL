---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183722"
---
# Invoke-AzResourceMoverPrepare

## SYNOPSIS
Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.
Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.

## SKŁADNIA

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.
Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.

## PRZYKŁADY

### Przykład 1. Sprawdzanie poprawność zależności przed przygotowaniem się na zasoby
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

Sprawdź poprawność zależności przed przygotowaniem się na zasoby.

### Przykład 2. Inicjowanie przygotowywania zestawu zasobów w kolekcji przenoszenia przy użyciu jako danych wejściowych "MoveResource Name"
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia, używając jako danych wejściowych "MoveResource Name".

### Przykład 3. Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia przy użyciu funkcji "SourceARMID"
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia za pomocą pliku "SourceARMID".

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

## OUTPUTS

### Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api20191001Preview.IOperationStatus

## NOTATKI

ALIASY

## LINKI POKREWNE

