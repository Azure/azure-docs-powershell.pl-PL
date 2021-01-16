---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337081"
---
# <span data-ttu-id="c9bc8-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="c9bc8-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="c9bc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="c9bc8-103">Usuwa zadanie DATAbox</span><span class="sxs-lookup"><span data-stu-id="c9bc8-103">Deletes the databox job</span></span>

## <span data-ttu-id="c9bc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9bc8-104">SYNTAX</span></span>

### <span data-ttu-id="c9bc8-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9bc8-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9bc8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9bc8-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9bc8-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9bc8-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9bc8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c9bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="c9bc8-109">Polecenie cmdlet **Remove-AzDataBoxJob** służy do usuwania gotowego zadania DATAbox z listy zadań DATAbox.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="c9bc8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9bc8-110">EXAMPLES</span></span>

### <span data-ttu-id="c9bc8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9bc8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="c9bc8-112">Usuwa określone zadanie DATAbox</span><span class="sxs-lookup"><span data-stu-id="c9bc8-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="c9bc8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c9bc8-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="c9bc8-114">Usuwa określone zadanie DATAbox bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="c9bc8-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="c9bc8-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c9bc8-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="c9bc8-116">Usuwa określone zadanie DATAbox</span><span class="sxs-lookup"><span data-stu-id="c9bc8-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="c9bc8-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9bc8-117">PARAMETERS</span></span>

### <span data-ttu-id="c9bc8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9bc8-118">-DefaultProfile</span></span>
<span data-ttu-id="c9bc8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9bc8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c9bc8-120">-Force</span></span>
<span data-ttu-id="c9bc8-121">Wymuszaj usunięcie bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="c9bc8-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="c9bc8-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c9bc8-122">-InputObject</span></span>
<span data-ttu-id="c9bc8-123">Inputobject typu PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="c9bc8-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="c9bc8-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9bc8-124">-Name</span></span>
<span data-ttu-id="c9bc8-125">Nazwa zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="c9bc8-125">Databox Job Name</span></span>

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

### <span data-ttu-id="c9bc8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9bc8-126">-PassThru</span></span>
<span data-ttu-id="c9bc8-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="c9bc8-127">PassThru</span></span>

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

### <span data-ttu-id="c9bc8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9bc8-128">-ResourceGroupName</span></span>
<span data-ttu-id="c9bc8-129">Nazwa grupy zasobów zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="c9bc8-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="c9bc8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9bc8-130">-ResourceId</span></span>
<span data-ttu-id="c9bc8-131">Identyfikator zasobu zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="c9bc8-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="c9bc8-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9bc8-132">-Confirm</span></span>
<span data-ttu-id="c9bc8-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9bc8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9bc8-134">-WhatIf</span></span>
<span data-ttu-id="c9bc8-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9bc8-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9bc8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9bc8-137">CommonParameters</span></span>
<span data-ttu-id="c9bc8-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9bc8-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9bc8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9bc8-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9bc8-140">INPUTS</span></span>

### <span data-ttu-id="c9bc8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c9bc8-141">System.String</span></span>

## <span data-ttu-id="c9bc8-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9bc8-142">OUTPUTS</span></span>

### <span data-ttu-id="c9bc8-143">System. void</span><span class="sxs-lookup"><span data-stu-id="c9bc8-143">System.Void</span></span>

## <span data-ttu-id="c9bc8-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9bc8-144">NOTES</span></span>

## <span data-ttu-id="c9bc8-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9bc8-145">RELATED LINKS</span></span>
