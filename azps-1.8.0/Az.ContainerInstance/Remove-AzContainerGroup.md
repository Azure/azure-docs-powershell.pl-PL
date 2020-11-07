---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: fb9b2c23618d731f6f107f755ca6ef41dfe439ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710154"
---
# <span data-ttu-id="10074-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="10074-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="10074-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10074-102">SYNOPSIS</span></span>
<span data-ttu-id="10074-103">Usuwa grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="10074-103">Removes a container group.</span></span>

## <span data-ttu-id="10074-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10074-104">SYNTAX</span></span>

### <span data-ttu-id="10074-105">RemoveContainerGroupByResourceGroupAndNameParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10074-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10074-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="10074-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10074-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="10074-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10074-108">Opis</span><span class="sxs-lookup"><span data-stu-id="10074-108">DESCRIPTION</span></span>
<span data-ttu-id="10074-109">Polecenie cmdlet **Remove-AzContainerGroup** usuwa grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="10074-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="10074-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10074-110">EXAMPLES</span></span>

### <span data-ttu-id="10074-111">Przykład 1. usuwa grupę kontenerów</span><span class="sxs-lookup"><span data-stu-id="10074-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="10074-112">To polecenie umożliwia usunięcie określonej grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="10074-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="10074-113">Przykład 2: Usunięcie grupy kontenerów według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="10074-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="10074-114">To polecenie usuwa grupę kontenerów według połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="10074-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="10074-115">Przykład 3: usuwa grupę kontenerów według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="10074-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="10074-116">To polecenie usuwa grupę kontenerów według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="10074-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="10074-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10074-117">PARAMETERS</span></span>

### <span data-ttu-id="10074-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10074-118">-DefaultProfile</span></span>
<span data-ttu-id="10074-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10074-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10074-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10074-120">-InputObject</span></span>
<span data-ttu-id="10074-121">Grupa kontenerów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="10074-121">The container group to remove.</span></span>

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

### <span data-ttu-id="10074-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10074-122">-Name</span></span>
<span data-ttu-id="10074-123">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="10074-123">The container group name.</span></span>

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

### <span data-ttu-id="10074-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10074-124">-PassThru</span></span>
<span data-ttu-id="10074-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="10074-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="10074-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10074-126">-ResourceGroupName</span></span>
<span data-ttu-id="10074-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10074-127">The resource group name.</span></span>

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

### <span data-ttu-id="10074-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10074-128">-ResourceId</span></span>
<span data-ttu-id="10074-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="10074-129">The resource id.</span></span>

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

### <span data-ttu-id="10074-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10074-130">-Confirm</span></span>
<span data-ttu-id="10074-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10074-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10074-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10074-132">-WhatIf</span></span>
<span data-ttu-id="10074-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10074-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10074-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10074-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10074-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10074-135">CommonParameters</span></span>
<span data-ttu-id="10074-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10074-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10074-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10074-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10074-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10074-138">INPUTS</span></span>

### <span data-ttu-id="10074-139">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="10074-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="10074-140">System. String</span><span class="sxs-lookup"><span data-stu-id="10074-140">System.String</span></span>

## <span data-ttu-id="10074-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10074-141">OUTPUTS</span></span>

### <span data-ttu-id="10074-142">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="10074-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="10074-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10074-143">NOTES</span></span>

## <span data-ttu-id="10074-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10074-144">RELATED LINKS</span></span>