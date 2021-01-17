---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3f2b09e047a4a7e39efe6f0f1724776f14a90d2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490310"
---
# <span data-ttu-id="77be4-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="77be4-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="77be4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77be4-102">SYNOPSIS</span></span>
<span data-ttu-id="77be4-103">Usuwa wdrożenie i wszystkie skojarzone operacje</span><span class="sxs-lookup"><span data-stu-id="77be4-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="77be4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77be4-104">SYNTAX</span></span>

### <span data-ttu-id="77be4-105">RemoveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77be4-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77be4-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="77be4-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77be4-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="77be4-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77be4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="77be4-108">DESCRIPTION</span></span>
<span data-ttu-id="77be4-109">Polecenie cmdlet **Remove-AzDeployment** umożliwia usunięcie wdrożenia platformy Azure w zakresie subskrypcji oraz wszelkich skojarzonych operacji.</span><span class="sxs-lookup"><span data-stu-id="77be4-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="77be4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77be4-110">EXAMPLES</span></span>

### <span data-ttu-id="77be4-111">Przykład 1: usunięcie wdrożenia o danej nazwie</span><span class="sxs-lookup"><span data-stu-id="77be4-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="77be4-112">To polecenie powoduje usunięcie wdrożenia "RolesDeployment" w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="77be4-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="77be4-113">Przykład 2: uzyskiwanie wdrożenia i usuwanie go</span><span class="sxs-lookup"><span data-stu-id="77be4-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="77be4-114">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie subskrypcji i usuwa je.</span><span class="sxs-lookup"><span data-stu-id="77be4-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="77be4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77be4-115">PARAMETERS</span></span>

### <span data-ttu-id="77be4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77be4-116">-AsJob</span></span>
<span data-ttu-id="77be4-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="77be4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77be4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77be4-118">-DefaultProfile</span></span>
<span data-ttu-id="77be4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77be4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77be4-120">-ID</span><span class="sxs-lookup"><span data-stu-id="77be4-120">-Id</span></span>
<span data-ttu-id="77be4-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="77be4-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="77be4-122">przykład:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="77be4-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77be4-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77be4-123">-InputObject</span></span>
<span data-ttu-id="77be4-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="77be4-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77be4-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77be4-125">-Name</span></span>
<span data-ttu-id="77be4-126">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="77be4-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77be4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77be4-127">-PassThru</span></span>
<span data-ttu-id="77be4-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="77be4-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="77be4-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="77be4-129">-Pre</span></span>
<span data-ttu-id="77be4-130">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="77be4-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="77be4-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77be4-131">-Confirm</span></span>
<span data-ttu-id="77be4-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77be4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77be4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77be4-133">-WhatIf</span></span>
<span data-ttu-id="77be4-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77be4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77be4-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77be4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77be4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77be4-136">CommonParameters</span></span>
<span data-ttu-id="77be4-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77be4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77be4-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77be4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77be4-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77be4-139">INPUTS</span></span>

### <span data-ttu-id="77be4-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="77be4-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="77be4-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77be4-141">OUTPUTS</span></span>

### <span data-ttu-id="77be4-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77be4-142">System.Boolean</span></span>

## <span data-ttu-id="77be4-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77be4-143">NOTES</span></span>

## <span data-ttu-id="77be4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77be4-144">RELATED LINKS</span></span>
