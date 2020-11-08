---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 2fbe6f707fe76e83591fe23c71b4de29a8bbf91c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221863"
---
# <span data-ttu-id="30a60-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="30a60-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="30a60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30a60-102">SYNOPSIS</span></span>
<span data-ttu-id="30a60-103">Usuwa wdrożenie i wszystkie skojarzone operacje</span><span class="sxs-lookup"><span data-stu-id="30a60-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="30a60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30a60-104">SYNTAX</span></span>

### <span data-ttu-id="30a60-105">RemoveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="30a60-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a60-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="30a60-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a60-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="30a60-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30a60-108">Opis</span><span class="sxs-lookup"><span data-stu-id="30a60-108">DESCRIPTION</span></span>
<span data-ttu-id="30a60-109">Polecenie cmdlet **Remove-AzDeployment** umożliwia usunięcie wdrożenia platformy Azure w zakresie subskrypcji oraz wszelkich skojarzonych operacji.</span><span class="sxs-lookup"><span data-stu-id="30a60-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="30a60-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30a60-110">EXAMPLES</span></span>

### <span data-ttu-id="30a60-111">Przykład 1: usunięcie wdrożenia o danej nazwie</span><span class="sxs-lookup"><span data-stu-id="30a60-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="30a60-112">To polecenie powoduje usunięcie wdrożenia "RolesDeployment" w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="30a60-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="30a60-113">Przykład 2: uzyskiwanie wdrożenia i usuwanie go</span><span class="sxs-lookup"><span data-stu-id="30a60-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="30a60-114">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie subskrypcji i usuwa je.</span><span class="sxs-lookup"><span data-stu-id="30a60-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="30a60-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30a60-115">PARAMETERS</span></span>

### <span data-ttu-id="30a60-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="30a60-116">-ApiVersion</span></span>
<span data-ttu-id="30a60-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="30a60-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="30a60-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="30a60-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="30a60-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30a60-119">-AsJob</span></span>
<span data-ttu-id="30a60-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="30a60-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30a60-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a60-121">-DefaultProfile</span></span>
<span data-ttu-id="30a60-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30a60-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a60-123">-ID</span><span class="sxs-lookup"><span data-stu-id="30a60-123">-Id</span></span>
<span data-ttu-id="30a60-124">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="30a60-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="30a60-125">przykład:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="30a60-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="30a60-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="30a60-126">-InputObject</span></span>
<span data-ttu-id="30a60-127">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="30a60-127">The deployment object.</span></span>

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

### <span data-ttu-id="30a60-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="30a60-128">-Name</span></span>
<span data-ttu-id="30a60-129">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="30a60-129">The name of the deployment.</span></span>

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

### <span data-ttu-id="30a60-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30a60-130">-PassThru</span></span>
<span data-ttu-id="30a60-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="30a60-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="30a60-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="30a60-132">-Pre</span></span>
<span data-ttu-id="30a60-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="30a60-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="30a60-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30a60-134">-Confirm</span></span>
<span data-ttu-id="30a60-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a60-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a60-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a60-136">-WhatIf</span></span>
<span data-ttu-id="30a60-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a60-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30a60-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30a60-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a60-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a60-139">CommonParameters</span></span>
<span data-ttu-id="30a60-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a60-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a60-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30a60-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a60-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30a60-142">INPUTS</span></span>

### <span data-ttu-id="30a60-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="30a60-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="30a60-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30a60-144">OUTPUTS</span></span>

### <span data-ttu-id="30a60-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30a60-145">System.Boolean</span></span>

## <span data-ttu-id="30a60-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30a60-146">NOTES</span></span>

## <span data-ttu-id="30a60-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30a60-147">RELATED LINKS</span></span>
