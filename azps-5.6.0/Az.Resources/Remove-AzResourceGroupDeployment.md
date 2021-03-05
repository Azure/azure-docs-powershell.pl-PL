---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f345b5f03fead63a1f041e364955e68d44dd9f0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974362"
---
# <span data-ttu-id="e67ed-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e67ed-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="e67ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e67ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e67ed-103">Usuwa wdrożenie grupy zasobów i wszystkie skojarzone operacje.</span><span class="sxs-lookup"><span data-stu-id="e67ed-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="e67ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e67ed-104">SYNTAX</span></span>

### <span data-ttu-id="e67ed-105">RemoveByResourceGroupName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="e67ed-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e67ed-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e67ed-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e67ed-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e67ed-107">DESCRIPTION</span></span>

<span data-ttu-id="e67ed-108">Polecenie **cmdlet Remove-AzResourceGroupDeployment** usuwa wdrożenie grupy zasobów platformy Azure i wszystkie skojarzone operacje.</span><span class="sxs-lookup"><span data-stu-id="e67ed-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="e67ed-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e67ed-109">EXAMPLES</span></span>

### <span data-ttu-id="e67ed-110">Przykład 1. Usuwanie wdrożenia grupy zasobów przy użyciu resourceid</span><span class="sxs-lookup"><span data-stu-id="e67ed-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="e67ed-111">To polecenie usuwa wdrożenie grupy zasobów z w pełni kwalifikowanym identyfikatorem zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e67ed-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="e67ed-112">Pomyślne usunięcie zwróci wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="e67ed-112">Successful removal returns true.</span></span>

### <span data-ttu-id="e67ed-113">Przykład 2. Usuwanie wdrożenia grupy zasobów z nazwami ResourceGroupName i ResourceName</span><span class="sxs-lookup"><span data-stu-id="e67ed-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="e67ed-114">To polecenie usuwa wdrożenie grupy zasobów z podaną wartością ResourceGroupName (Nazwa Grupy Zasobów) i ResourceName (Nazwa Zasobu).</span><span class="sxs-lookup"><span data-stu-id="e67ed-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="e67ed-115">Pomyślne usunięcie zwróci wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="e67ed-115">Successful removal returns true.</span></span>

## <span data-ttu-id="e67ed-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e67ed-116">PARAMETERS</span></span>

### <span data-ttu-id="e67ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67ed-117">-DefaultProfile</span></span>
<span data-ttu-id="e67ed-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e67ed-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e67ed-119">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="e67ed-119">-Id</span></span>
<span data-ttu-id="e67ed-120">Określa identyfikator wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e67ed-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="e67ed-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e67ed-121">-Name</span></span>
<span data-ttu-id="e67ed-122">Określa nazwę wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e67ed-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="e67ed-123">— Przed</span><span class="sxs-lookup"><span data-stu-id="e67ed-123">-Pre</span></span>
<span data-ttu-id="e67ed-124">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="e67ed-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e67ed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e67ed-125">-ResourceGroupName</span></span>
<span data-ttu-id="e67ed-126">Określa nazwę grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e67ed-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="e67ed-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e67ed-127">-Confirm</span></span>
<span data-ttu-id="e67ed-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e67ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e67ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e67ed-129">-WhatIf</span></span>
<span data-ttu-id="e67ed-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e67ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e67ed-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e67ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e67ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67ed-132">CommonParameters</span></span>
<span data-ttu-id="e67ed-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e67ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e67ed-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e67ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67ed-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e67ed-135">INPUTS</span></span>

### <span data-ttu-id="e67ed-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e67ed-136">System.String</span></span>

## <span data-ttu-id="e67ed-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e67ed-137">OUTPUTS</span></span>

### <span data-ttu-id="e67ed-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e67ed-138">System.Boolean</span></span>

## <span data-ttu-id="e67ed-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e67ed-139">NOTES</span></span>

## <span data-ttu-id="e67ed-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e67ed-140">RELATED LINKS</span></span>

[<span data-ttu-id="e67ed-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e67ed-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="e67ed-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e67ed-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="e67ed-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e67ed-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="e67ed-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e67ed-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


