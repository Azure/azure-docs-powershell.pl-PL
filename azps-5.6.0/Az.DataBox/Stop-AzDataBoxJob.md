---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 60fdd8223f073ffd6de76db659e6bd989f48fada
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998670"
---
# <span data-ttu-id="f1705-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="f1705-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="f1705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1705-102">SYNOPSIS</span></span>
<span data-ttu-id="f1705-103">Anulowanie bieżącego zadania pola danych, jeśli zadanie jest w stanie anulowania.</span><span class="sxs-lookup"><span data-stu-id="f1705-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="f1705-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1705-104">SYNTAX</span></span>

### <span data-ttu-id="f1705-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f1705-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1705-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1705-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1705-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1705-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1705-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1705-108">DESCRIPTION</span></span>
<span data-ttu-id="f1705-109">Polecenie **cmdlet Stop-AzDataBoxJob** służy do anulowania zadania skrzynki danych.</span><span class="sxs-lookup"><span data-stu-id="f1705-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="f1705-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1705-110">EXAMPLES</span></span>

### <span data-ttu-id="f1705-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f1705-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="f1705-112">Anulowanie określonego zadania pola danych</span><span class="sxs-lookup"><span data-stu-id="f1705-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="f1705-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f1705-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="f1705-114">Wymuszanie anulowania określonego zadania skrzynki danych bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="f1705-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="f1705-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f1705-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="f1705-116">Anulowanie określonego zadania pola danych</span><span class="sxs-lookup"><span data-stu-id="f1705-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="f1705-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1705-117">PARAMETERS</span></span>

### <span data-ttu-id="f1705-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1705-118">-DefaultProfile</span></span>
<span data-ttu-id="f1705-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1705-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1705-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f1705-120">-Force</span></span>
<span data-ttu-id="f1705-121">Wymusij zatrzymanie bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="f1705-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="f1705-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1705-122">-InputObject</span></span>
<span data-ttu-id="f1705-123">InputObject typu PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="f1705-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1705-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1705-124">-Name</span></span>
<span data-ttu-id="f1705-125">Databox Job Name</span><span class="sxs-lookup"><span data-stu-id="f1705-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1705-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1705-126">-PassThru</span></span>
<span data-ttu-id="f1705-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="f1705-127">PassThru</span></span>

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

### <span data-ttu-id="f1705-128">— Powód</span><span class="sxs-lookup"><span data-stu-id="f1705-128">-Reason</span></span>
<span data-ttu-id="f1705-129">Powód anulowania</span><span class="sxs-lookup"><span data-stu-id="f1705-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="f1705-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1705-130">-ResourceGroupName</span></span>
<span data-ttu-id="f1705-131">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="f1705-131">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1705-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1705-132">-ResourceId</span></span>
<span data-ttu-id="f1705-133">Identyfikator zasobu skrzynki danych</span><span class="sxs-lookup"><span data-stu-id="f1705-133">Databox Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1705-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1705-134">-Confirm</span></span>
<span data-ttu-id="f1705-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f1705-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1705-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1705-136">-WhatIf</span></span>
<span data-ttu-id="f1705-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1705-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1705-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f1705-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1705-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1705-139">CommonParameters</span></span>
<span data-ttu-id="f1705-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1705-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1705-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1705-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1705-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1705-142">INPUTS</span></span>

### <span data-ttu-id="f1705-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f1705-143">System.String</span></span>

## <span data-ttu-id="f1705-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1705-144">OUTPUTS</span></span>

### <span data-ttu-id="f1705-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="f1705-145">System.Void</span></span>

## <span data-ttu-id="f1705-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1705-146">NOTES</span></span>

## <span data-ttu-id="f1705-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1705-147">RELATED LINKS</span></span>
