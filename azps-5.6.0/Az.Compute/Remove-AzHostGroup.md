---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: f05855c7fa677c384e9d8d0c5385d6014d80d312
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983306"
---
# <span data-ttu-id="8c1f1-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="8c1f1-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="8c1f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c1f1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1f1-103">Usuwa grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-103">Removes a host group.</span></span>

## <span data-ttu-id="8c1f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c1f1-104">SYNTAX</span></span>

### <span data-ttu-id="8c1f1-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c1f1-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1f1-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="8c1f1-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1f1-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="8c1f1-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c1f1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c1f1-108">DESCRIPTION</span></span>
<span data-ttu-id="8c1f1-109">To polecenie cmdlet spowoduje usunięcie grupy hostów</span><span class="sxs-lookup"><span data-stu-id="8c1f1-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="8c1f1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c1f1-110">EXAMPLES</span></span>

### <span data-ttu-id="8c1f1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c1f1-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="8c1f1-112">To polecenie pobiera i usuwa grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="8c1f1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8c1f1-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="8c1f1-114">To polecenie usuwa grupę danego hosta.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-114">This command removes the given host group.</span></span>

## <span data-ttu-id="8c1f1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c1f1-115">PARAMETERS</span></span>

### <span data-ttu-id="8c1f1-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8c1f1-116">-AsJob</span></span>
<span data-ttu-id="8c1f1-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8c1f1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c1f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c1f1-118">-DefaultProfile</span></span>
<span data-ttu-id="8c1f1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c1f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c1f1-120">-InputObject</span></span>
<span data-ttu-id="8c1f1-121">Obiekt lokalny grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c1f1-122">-Name</span></span>
<span data-ttu-id="8c1f1-123">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c1f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c1f1-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c1f1-126">-ResourceId</span></span>
<span data-ttu-id="8c1f1-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f1-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c1f1-128">-Confirm</span></span>
<span data-ttu-id="8c1f1-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c1f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c1f1-130">-WhatIf</span></span>
<span data-ttu-id="8c1f1-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c1f1-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c1f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1f1-133">CommonParameters</span></span>
<span data-ttu-id="8c1f1-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c1f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c1f1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c1f1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1f1-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c1f1-136">INPUTS</span></span>

### <span data-ttu-id="8c1f1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8c1f1-137">System.String</span></span>

### <span data-ttu-id="8c1f1-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="8c1f1-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="8c1f1-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c1f1-139">OUTPUTS</span></span>

### <span data-ttu-id="8c1f1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8c1f1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8c1f1-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c1f1-141">NOTES</span></span>

## <span data-ttu-id="8c1f1-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c1f1-142">RELATED LINKS</span></span>
