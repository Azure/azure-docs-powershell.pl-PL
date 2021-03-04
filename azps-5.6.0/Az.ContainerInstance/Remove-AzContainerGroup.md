---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: f4774ea7dec4ddd8df29c0a131fbaf080cbbba94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004490"
---
# <span data-ttu-id="672b4-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="672b4-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="672b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="672b4-102">SYNOPSIS</span></span>
<span data-ttu-id="672b4-103">Usuwa grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="672b4-103">Removes a container group.</span></span>

## <span data-ttu-id="672b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="672b4-104">SYNTAX</span></span>

### <span data-ttu-id="672b4-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="672b4-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="672b4-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="672b4-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="672b4-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="672b4-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="672b4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="672b4-108">DESCRIPTION</span></span>
<span data-ttu-id="672b4-109">Polecenie **cmdlet Remove-AzContainerGroup** usuwa grupę kontenera.</span><span class="sxs-lookup"><span data-stu-id="672b4-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="672b4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="672b4-110">EXAMPLES</span></span>

### <span data-ttu-id="672b4-111">Przykład 1. Usuwanie grupy kontenerów</span><span class="sxs-lookup"><span data-stu-id="672b4-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="672b4-112">To polecenie usuwa określoną grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="672b4-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="672b4-113">Przykład 2. Usuwanie grupy kontenerów za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="672b4-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="672b4-114">To polecenie usuwa grupę kontenerów za pomocą linii rurowych.</span><span class="sxs-lookup"><span data-stu-id="672b4-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="672b4-115">Przykład 3. Usuwa grupę kontenerów według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="672b4-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="672b4-116">To polecenie usuwa grupę kontenerów według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="672b4-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="672b4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="672b4-117">PARAMETERS</span></span>

### <span data-ttu-id="672b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672b4-118">-DefaultProfile</span></span>
<span data-ttu-id="672b4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="672b4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="672b4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="672b4-120">-InputObject</span></span>
<span data-ttu-id="672b4-121">Grupa kontenerów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="672b4-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="672b4-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="672b4-122">-Name</span></span>
<span data-ttu-id="672b4-123">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="672b4-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="672b4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="672b4-124">-PassThru</span></span>
<span data-ttu-id="672b4-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="672b4-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="672b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="672b4-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="672b4-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="672b4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="672b4-128">-ResourceId</span></span>
<span data-ttu-id="672b4-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="672b4-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="672b4-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="672b4-130">-Confirm</span></span>
<span data-ttu-id="672b4-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="672b4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="672b4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="672b4-132">-WhatIf</span></span>
<span data-ttu-id="672b4-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="672b4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="672b4-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="672b4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="672b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672b4-135">CommonParameters</span></span>
<span data-ttu-id="672b4-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="672b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672b4-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="672b4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672b4-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="672b4-138">INPUTS</span></span>

### <span data-ttu-id="672b4-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="672b4-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="672b4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="672b4-140">System.String</span></span>

## <span data-ttu-id="672b4-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="672b4-141">OUTPUTS</span></span>

### <span data-ttu-id="672b4-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="672b4-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="672b4-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="672b4-143">NOTES</span></span>

## <span data-ttu-id="672b4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="672b4-144">RELATED LINKS</span></span>
