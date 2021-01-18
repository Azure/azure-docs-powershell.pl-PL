---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499918"
---
# <span data-ttu-id="e190c-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e190c-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="e190c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e190c-102">SYNOPSIS</span></span>
<span data-ttu-id="e190c-103">Usuwa wdrożenie grupy zasobów i wszystkie skojarzone z nią operacje.</span><span class="sxs-lookup"><span data-stu-id="e190c-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="e190c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e190c-104">SYNTAX</span></span>

### <span data-ttu-id="e190c-105">RemoveByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e190c-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e190c-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e190c-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e190c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e190c-107">DESCRIPTION</span></span>

<span data-ttu-id="e190c-108">Polecenie cmdlet **Remove-AzResourceGroupDeployment** umożliwia usunięcie wdrożenia grupy zasobów platformy Azure oraz wszystkich skojarzonych operacji.</span><span class="sxs-lookup"><span data-stu-id="e190c-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="e190c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e190c-109">EXAMPLES</span></span>

### <span data-ttu-id="e190c-110">Przykład 1: usunięcie wdrożenia grupy zasobów z identyfikatorem ResourceId</span><span class="sxs-lookup"><span data-stu-id="e190c-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="e190c-111">To polecenie umożliwia usunięcie wdrożenia grupy zasobów z pełnym kwalifikowanym identyfikatorem zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e190c-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="e190c-112">Udane usunięcie zwraca wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="e190c-112">Successful removal returns true.</span></span>

### <span data-ttu-id="e190c-113">Przykład 2: usunięcie wdrożenia grupy zasobów z ResourceGroupName i resourceName</span><span class="sxs-lookup"><span data-stu-id="e190c-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="e190c-114">To polecenie umożliwia usunięcie wdrożenia grupy zasobów z podanym ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e190c-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="e190c-115">Udane usunięcie zwraca wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="e190c-115">Successful removal returns true.</span></span>

## <span data-ttu-id="e190c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e190c-116">PARAMETERS</span></span>

### <span data-ttu-id="e190c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e190c-117">-DefaultProfile</span></span>
<span data-ttu-id="e190c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e190c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e190c-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e190c-119">-Id</span></span>
<span data-ttu-id="e190c-120">Określa identyfikator wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e190c-120">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e190c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e190c-121">-Name</span></span>
<span data-ttu-id="e190c-122">Określa nazwę wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e190c-122">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e190c-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="e190c-123">-Pre</span></span>
<span data-ttu-id="e190c-124">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="e190c-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e190c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e190c-125">-ResourceGroupName</span></span>
<span data-ttu-id="e190c-126">Określa nazwę grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e190c-126">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e190c-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e190c-127">-Confirm</span></span>
<span data-ttu-id="e190c-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e190c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e190c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e190c-129">-WhatIf</span></span>
<span data-ttu-id="e190c-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e190c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e190c-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e190c-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e190c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e190c-132">CommonParameters</span></span>
<span data-ttu-id="e190c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e190c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e190c-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e190c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e190c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e190c-135">INPUTS</span></span>

### <span data-ttu-id="e190c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e190c-136">System.String</span></span>

## <span data-ttu-id="e190c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e190c-137">OUTPUTS</span></span>

### <span data-ttu-id="e190c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e190c-138">System.Boolean</span></span>

## <span data-ttu-id="e190c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e190c-139">NOTES</span></span>

## <span data-ttu-id="e190c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e190c-140">RELATED LINKS</span></span>

[<span data-ttu-id="e190c-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e190c-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="e190c-142">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e190c-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="e190c-143">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e190c-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="e190c-144">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e190c-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


