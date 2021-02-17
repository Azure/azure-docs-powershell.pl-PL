---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238810"
---
# <span data-ttu-id="ad2e6-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="ad2e6-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="ad2e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2e6-103">Usuwa grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-103">Removes a host group.</span></span>

## <span data-ttu-id="ad2e6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad2e6-104">SYNTAX</span></span>

### <span data-ttu-id="ad2e6-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ad2e6-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2e6-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="ad2e6-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2e6-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="ad2e6-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2e6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad2e6-108">DESCRIPTION</span></span>
<span data-ttu-id="ad2e6-109">To polecenie cmdlet spowoduje usunięcie grupy hostów</span><span class="sxs-lookup"><span data-stu-id="ad2e6-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="ad2e6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad2e6-110">EXAMPLES</span></span>

### <span data-ttu-id="ad2e6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad2e6-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="ad2e6-112">To polecenie pobiera i usuwa grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="ad2e6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ad2e6-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="ad2e6-114">To polecenie usuwa grupę danego hosta.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-114">This command removes the given host group.</span></span>

## <span data-ttu-id="ad2e6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad2e6-115">PARAMETERS</span></span>

### <span data-ttu-id="ad2e6-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ad2e6-116">-AsJob</span></span>
<span data-ttu-id="ad2e6-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ad2e6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad2e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2e6-118">-DefaultProfile</span></span>
<span data-ttu-id="ad2e6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad2e6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad2e6-120">-InputObject</span></span>
<span data-ttu-id="ad2e6-121">Obiekt lokalny grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-121">The local object of the host group.</span></span>

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

### <span data-ttu-id="ad2e6-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad2e6-122">-Name</span></span>
<span data-ttu-id="ad2e6-123">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-123">The name of the host group.</span></span>

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

### <span data-ttu-id="ad2e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad2e6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad2e6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad2e6-126">-ResourceId</span></span>
<span data-ttu-id="ad2e6-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="ad2e6-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad2e6-128">-Confirm</span></span>
<span data-ttu-id="ad2e6-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2e6-130">-WhatIf</span></span>
<span data-ttu-id="ad2e6-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad2e6-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2e6-133">CommonParameters</span></span>
<span data-ttu-id="ad2e6-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2e6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad2e6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2e6-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad2e6-136">INPUTS</span></span>

### <span data-ttu-id="ad2e6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ad2e6-137">System.String</span></span>

### <span data-ttu-id="ad2e6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="ad2e6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="ad2e6-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad2e6-139">OUTPUTS</span></span>

### <span data-ttu-id="ad2e6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ad2e6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ad2e6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad2e6-141">NOTES</span></span>

## <span data-ttu-id="ad2e6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad2e6-142">RELATED LINKS</span></span>
