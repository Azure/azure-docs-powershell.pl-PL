---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: 2cae601904b15e2508886374c1b607ed8aec4b93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871752"
---
# <span data-ttu-id="e4d62-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d62-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="e4d62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4d62-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d62-103">Usuwa wdrożenie grupy zasobów i wszystkie skojarzone z nią operacje.</span><span class="sxs-lookup"><span data-stu-id="e4d62-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="e4d62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4d62-104">SYNTAX</span></span>

### <span data-ttu-id="e4d62-105">RemoveByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4d62-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4d62-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e4d62-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d62-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e4d62-107">DESCRIPTION</span></span>
<span data-ttu-id="e4d62-108">Polecenie cmdlet **Remove-AzResourceGroupDeployment** umożliwia usunięcie wdrożenia grupy zasobów platformy Azure oraz wszystkich skojarzonych operacji.</span><span class="sxs-lookup"><span data-stu-id="e4d62-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="e4d62-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4d62-109">EXAMPLES</span></span>

## <span data-ttu-id="e4d62-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4d62-110">PARAMETERS</span></span>

### <span data-ttu-id="e4d62-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e4d62-111">-ApiVersion</span></span>
<span data-ttu-id="e4d62-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4d62-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e4d62-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="e4d62-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e4d62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d62-114">-DefaultProfile</span></span>
<span data-ttu-id="e4d62-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4d62-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4d62-116">-ID</span><span class="sxs-lookup"><span data-stu-id="e4d62-116">-Id</span></span>
<span data-ttu-id="e4d62-117">Określa identyfikator wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e4d62-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="e4d62-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4d62-118">-Name</span></span>
<span data-ttu-id="e4d62-119">Określa nazwę wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e4d62-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="e4d62-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="e4d62-120">-Pre</span></span>
<span data-ttu-id="e4d62-121">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="e4d62-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e4d62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d62-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4d62-123">Określa nazwę grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e4d62-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="e4d62-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4d62-124">-Confirm</span></span>
<span data-ttu-id="e4d62-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4d62-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4d62-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d62-126">-WhatIf</span></span>
<span data-ttu-id="e4d62-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4d62-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4d62-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4d62-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4d62-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d62-129">CommonParameters</span></span>
<span data-ttu-id="e4d62-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d62-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d62-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4d62-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d62-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4d62-132">INPUTS</span></span>

### <span data-ttu-id="e4d62-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e4d62-133">System.String</span></span>

## <span data-ttu-id="e4d62-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4d62-134">OUTPUTS</span></span>

### <span data-ttu-id="e4d62-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4d62-135">System.Boolean</span></span>

## <span data-ttu-id="e4d62-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4d62-136">NOTES</span></span>

## <span data-ttu-id="e4d62-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4d62-137">RELATED LINKS</span></span>

[<span data-ttu-id="e4d62-138">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d62-138">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="e4d62-139">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d62-139">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="e4d62-140">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d62-140">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="e4d62-141">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d62-141">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


