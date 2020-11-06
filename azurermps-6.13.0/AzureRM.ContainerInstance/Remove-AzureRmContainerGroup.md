---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: f1971f8bf0e7d8e779743739b8dd041effe3ba5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526218"
---
# <span data-ttu-id="bf9df-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="bf9df-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="bf9df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf9df-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9df-103">Usuwa grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="bf9df-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf9df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf9df-104">SYNTAX</span></span>

### <span data-ttu-id="bf9df-105">RemoveContainerGroupByResourceGroupAndNameParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf9df-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf9df-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="bf9df-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf9df-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="bf9df-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf9df-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bf9df-108">DESCRIPTION</span></span>
<span data-ttu-id="bf9df-109">Polecenie cmdlet **Remove-AzureRmContainerGroup** usuwa grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="bf9df-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="bf9df-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf9df-110">EXAMPLES</span></span>

### <span data-ttu-id="bf9df-111">Przykład 1. usuwa grupę kontenerów</span><span class="sxs-lookup"><span data-stu-id="bf9df-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="bf9df-112">To polecenie umożliwia usunięcie określonej grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="bf9df-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="bf9df-113">Przykład 2: Usunięcie grupy kontenerów według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="bf9df-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="bf9df-114">To polecenie usuwa grupę kontenerów według połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="bf9df-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="bf9df-115">Przykład 3: usuwa grupę kontenerów według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf9df-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="bf9df-116">To polecenie usuwa grupę kontenerów według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf9df-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="bf9df-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf9df-117">PARAMETERS</span></span>

### <span data-ttu-id="bf9df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9df-118">-DefaultProfile</span></span>
<span data-ttu-id="bf9df-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf9df-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9df-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf9df-120">-InputObject</span></span>
<span data-ttu-id="bf9df-121">Grupa kontenerów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="bf9df-121">The container group to remove.</span></span>

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

### <span data-ttu-id="bf9df-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf9df-122">-Name</span></span>
<span data-ttu-id="bf9df-123">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="bf9df-123">The container group name.</span></span>

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

### <span data-ttu-id="bf9df-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf9df-124">-PassThru</span></span>
<span data-ttu-id="bf9df-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bf9df-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bf9df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9df-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf9df-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf9df-127">The resource group name.</span></span>

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

### <span data-ttu-id="bf9df-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf9df-128">-ResourceId</span></span>
<span data-ttu-id="bf9df-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf9df-129">The resource id.</span></span>

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

### <span data-ttu-id="bf9df-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf9df-130">-Confirm</span></span>
<span data-ttu-id="bf9df-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf9df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf9df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf9df-132">-WhatIf</span></span>
<span data-ttu-id="bf9df-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf9df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf9df-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf9df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf9df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9df-135">CommonParameters</span></span>
<span data-ttu-id="bf9df-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf9df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9df-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf9df-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9df-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf9df-138">INPUTS</span></span>

### <span data-ttu-id="bf9df-139">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="bf9df-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="bf9df-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf9df-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="bf9df-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bf9df-141">System.String</span></span>

## <span data-ttu-id="bf9df-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf9df-142">OUTPUTS</span></span>

### <span data-ttu-id="bf9df-143">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="bf9df-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="bf9df-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf9df-144">NOTES</span></span>

## <span data-ttu-id="bf9df-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf9df-145">RELATED LINKS</span></span>
