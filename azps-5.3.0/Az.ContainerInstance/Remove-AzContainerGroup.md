---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503898"
---
# <span data-ttu-id="a3661-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a3661-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="a3661-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3661-102">SYNOPSIS</span></span>
<span data-ttu-id="a3661-103">Usuwa grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="a3661-103">Removes a container group.</span></span>

## <span data-ttu-id="a3661-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3661-104">SYNTAX</span></span>

### <span data-ttu-id="a3661-105">RemoveContainerGroupByResourceGroupAndNameParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a3661-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3661-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a3661-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3661-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="a3661-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3661-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a3661-108">DESCRIPTION</span></span>
<span data-ttu-id="a3661-109">Polecenie cmdlet **Remove-AzContainerGroup** usuwa grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="a3661-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="a3661-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3661-110">EXAMPLES</span></span>

### <span data-ttu-id="a3661-111">Przykład 1. usuwa grupę kontenerów</span><span class="sxs-lookup"><span data-stu-id="a3661-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="a3661-112">To polecenie umożliwia usunięcie określonej grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="a3661-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="a3661-113">Przykład 2: Usunięcie grupy kontenerów według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="a3661-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="a3661-114">To polecenie usuwa grupę kontenerów według połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="a3661-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="a3661-115">Przykład 3: usuwa grupę kontenerów według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="a3661-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="a3661-116">To polecenie usuwa grupę kontenerów według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="a3661-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="a3661-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3661-117">PARAMETERS</span></span>

### <span data-ttu-id="a3661-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3661-118">-DefaultProfile</span></span>
<span data-ttu-id="a3661-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3661-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3661-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3661-120">-InputObject</span></span>
<span data-ttu-id="a3661-121">Grupa kontenerów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a3661-121">The container group to remove.</span></span>

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

### <span data-ttu-id="a3661-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3661-122">-Name</span></span>
<span data-ttu-id="a3661-123">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="a3661-123">The container group name.</span></span>

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

### <span data-ttu-id="a3661-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3661-124">-PassThru</span></span>
<span data-ttu-id="a3661-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a3661-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a3661-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3661-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3661-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3661-127">The resource group name.</span></span>

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

### <span data-ttu-id="a3661-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3661-128">-ResourceId</span></span>
<span data-ttu-id="a3661-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a3661-129">The resource id.</span></span>

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

### <span data-ttu-id="a3661-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3661-130">-Confirm</span></span>
<span data-ttu-id="a3661-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3661-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3661-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3661-132">-WhatIf</span></span>
<span data-ttu-id="a3661-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3661-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3661-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3661-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3661-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3661-135">CommonParameters</span></span>
<span data-ttu-id="a3661-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3661-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3661-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3661-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3661-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3661-138">INPUTS</span></span>

### <span data-ttu-id="a3661-139">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a3661-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="a3661-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a3661-140">System.String</span></span>

## <span data-ttu-id="a3661-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3661-141">OUTPUTS</span></span>

### <span data-ttu-id="a3661-142">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a3661-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a3661-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3661-143">NOTES</span></span>

## <span data-ttu-id="a3661-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3661-144">RELATED LINKS</span></span>
