---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050720"
---
# <span data-ttu-id="31669-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31669-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="31669-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31669-102">SYNOPSIS</span></span>
<span data-ttu-id="31669-103">Usuwa wdrożenie grupy zasobów i wszystkie skojarzone z nią operacje.</span><span class="sxs-lookup"><span data-stu-id="31669-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="31669-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31669-104">SYNTAX</span></span>

### <span data-ttu-id="31669-105">RemoveByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="31669-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31669-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="31669-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31669-107">Opis</span><span class="sxs-lookup"><span data-stu-id="31669-107">DESCRIPTION</span></span>

<span data-ttu-id="31669-108">Polecenie cmdlet **Remove-AzResourceGroupDeployment** umożliwia usunięcie wdrożenia grupy zasobów platformy Azure oraz wszystkich skojarzonych operacji.</span><span class="sxs-lookup"><span data-stu-id="31669-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="31669-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31669-109">EXAMPLES</span></span>

### <span data-ttu-id="31669-110">Przykład 1: usunięcie wdrożenia grupy zasobów z identyfikatorem ResourceId</span><span class="sxs-lookup"><span data-stu-id="31669-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="31669-111">To polecenie umożliwia usunięcie wdrożenia grupy zasobów z pełnym kwalifikowanym identyfikatorem zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="31669-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="31669-112">Udane usunięcie zwraca wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="31669-112">Successful removal returns true.</span></span>

### <span data-ttu-id="31669-113">Przykład 2: usunięcie wdrożenia grupy zasobów z ResourceGroupName i resourceName</span><span class="sxs-lookup"><span data-stu-id="31669-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="31669-114">To polecenie umożliwia usunięcie wdrożenia grupy zasobów z podanym ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="31669-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="31669-115">Udane usunięcie zwraca wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="31669-115">Successful removal returns true.</span></span>

## <span data-ttu-id="31669-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31669-116">PARAMETERS</span></span>

### <span data-ttu-id="31669-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="31669-117">-ApiVersion</span></span>
<span data-ttu-id="31669-118">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="31669-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="31669-119">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="31669-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31669-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31669-120">-DefaultProfile</span></span>
<span data-ttu-id="31669-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="31669-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31669-122">-ID</span><span class="sxs-lookup"><span data-stu-id="31669-122">-Id</span></span>
<span data-ttu-id="31669-123">Określa identyfikator wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="31669-123">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="31669-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31669-124">-Name</span></span>
<span data-ttu-id="31669-125">Określa nazwę wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="31669-125">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="31669-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="31669-126">-Pre</span></span>
<span data-ttu-id="31669-127">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="31669-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="31669-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31669-128">-ResourceGroupName</span></span>
<span data-ttu-id="31669-129">Określa nazwę grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="31669-129">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="31669-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31669-130">-Confirm</span></span>
<span data-ttu-id="31669-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31669-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31669-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31669-132">-WhatIf</span></span>
<span data-ttu-id="31669-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31669-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31669-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31669-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31669-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31669-135">CommonParameters</span></span>
<span data-ttu-id="31669-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31669-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31669-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31669-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31669-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31669-138">INPUTS</span></span>

### <span data-ttu-id="31669-139">System. String</span><span class="sxs-lookup"><span data-stu-id="31669-139">System.String</span></span>

## <span data-ttu-id="31669-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31669-140">OUTPUTS</span></span>

### <span data-ttu-id="31669-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31669-141">System.Boolean</span></span>

## <span data-ttu-id="31669-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31669-142">NOTES</span></span>

## <span data-ttu-id="31669-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31669-143">RELATED LINKS</span></span>

[<span data-ttu-id="31669-144">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31669-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="31669-145">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31669-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="31669-146">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31669-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="31669-147">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31669-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


