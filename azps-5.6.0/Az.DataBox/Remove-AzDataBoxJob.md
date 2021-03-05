---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 5a9415b5590b6f78c5ca703dba8293c153de819d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998110"
---
# <span data-ttu-id="22289-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="22289-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="22289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22289-102">SYNOPSIS</span></span>
<span data-ttu-id="22289-103">Usuwa zadanie skrzynki danych.</span><span class="sxs-lookup"><span data-stu-id="22289-103">Deletes the databox job</span></span>

## <span data-ttu-id="22289-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22289-104">SYNTAX</span></span>

### <span data-ttu-id="22289-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="22289-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22289-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22289-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22289-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22289-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22289-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="22289-108">DESCRIPTION</span></span>
<span data-ttu-id="22289-109">Polecenie **cmdlet Remove-AzDataBoxJob** służy do usuwania gotowego zadania pola danych z listy zadań skrzynki danych.</span><span class="sxs-lookup"><span data-stu-id="22289-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="22289-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22289-110">EXAMPLES</span></span>

### <span data-ttu-id="22289-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22289-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="22289-112">Usuwa określone zadanie pola danych.</span><span class="sxs-lookup"><span data-stu-id="22289-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="22289-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="22289-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="22289-114">Wymusza usunięcie określonego zadania pola danych bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="22289-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="22289-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="22289-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="22289-116">Usuwa określone zadanie pola danych.</span><span class="sxs-lookup"><span data-stu-id="22289-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="22289-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22289-117">PARAMETERS</span></span>

### <span data-ttu-id="22289-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22289-118">-DefaultProfile</span></span>
<span data-ttu-id="22289-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="22289-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22289-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="22289-120">-Force</span></span>
<span data-ttu-id="22289-121">Wymusz usunięcie bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="22289-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="22289-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22289-122">-InputObject</span></span>
<span data-ttu-id="22289-123">InputObject typu PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="22289-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="22289-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="22289-124">-Name</span></span>
<span data-ttu-id="22289-125">Databox Job Name</span><span class="sxs-lookup"><span data-stu-id="22289-125">Databox Job Name</span></span>

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

### <span data-ttu-id="22289-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22289-126">-PassThru</span></span>
<span data-ttu-id="22289-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="22289-127">PassThru</span></span>

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

### <span data-ttu-id="22289-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22289-128">-ResourceGroupName</span></span>
<span data-ttu-id="22289-129">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="22289-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="22289-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22289-130">-ResourceId</span></span>
<span data-ttu-id="22289-131">Identyfikator zasobu zadania w skrzynce danych</span><span class="sxs-lookup"><span data-stu-id="22289-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="22289-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22289-132">-Confirm</span></span>
<span data-ttu-id="22289-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="22289-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22289-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22289-134">-WhatIf</span></span>
<span data-ttu-id="22289-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22289-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22289-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="22289-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22289-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22289-137">CommonParameters</span></span>
<span data-ttu-id="22289-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22289-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22289-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22289-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22289-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22289-140">INPUTS</span></span>

### <span data-ttu-id="22289-141">System.String</span><span class="sxs-lookup"><span data-stu-id="22289-141">System.String</span></span>

## <span data-ttu-id="22289-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22289-142">OUTPUTS</span></span>

### <span data-ttu-id="22289-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="22289-143">System.Void</span></span>

## <span data-ttu-id="22289-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22289-144">NOTES</span></span>

## <span data-ttu-id="22289-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22289-145">RELATED LINKS</span></span>
