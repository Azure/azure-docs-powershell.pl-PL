---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 08cde5aed74b194ede03f695eaf071d18467cb1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962129"
---
# <span data-ttu-id="5293e-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="5293e-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="5293e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5293e-102">SYNOPSIS</span></span>
<span data-ttu-id="5293e-103">Tworzy krok.</span><span class="sxs-lookup"><span data-stu-id="5293e-103">Creates a step.</span></span>

## <span data-ttu-id="5293e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5293e-104">SYNTAX</span></span>

### <span data-ttu-id="5293e-105">Czekaj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5293e-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5293e-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="5293e-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5293e-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="5293e-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5293e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5293e-108">DESCRIPTION</span></span>
<span data-ttu-id="5293e-109">Polecenie **cmdlet New-AzDeploymentManagerStep** tworzy krok wdrożenia, do których można się odwołać w wdrożeniach.</span><span class="sxs-lookup"><span data-stu-id="5293e-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="5293e-110">Określ właściwości *Name (Nazwa* *Grupy Zasobów)* i Required (Nazwa Grupy Zasobów).</span><span class="sxs-lookup"><span data-stu-id="5293e-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="5293e-111">Zwrócony obiekt można zmodyfikować lokalnie, a następnie zastosować zmiany do kroku za pomocą Set-AzDeploymentManagerStep cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5293e-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="5293e-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5293e-112">EXAMPLES</span></span>

### <span data-ttu-id="5293e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5293e-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="5293e-114">Tworzy krok w grupie ContosoResourceGroup o nazwie ContosoService1WaitStep z centralną polsce (Centralną grupę zasobów) jako lokalizacją zasobu.</span><span class="sxs-lookup"><span data-stu-id="5293e-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="5293e-115">Właściwość Czas trwania zapewnia czas trwania etapu realizacji przed uruchomieniem następnego kroku.</span><span class="sxs-lookup"><span data-stu-id="5293e-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="5293e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5293e-116">PARAMETERS</span></span>

### <span data-ttu-id="5293e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5293e-117">-DefaultProfile</span></span>
<span data-ttu-id="5293e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5293e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5293e-119">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="5293e-119">-Duration</span></span>
<span data-ttu-id="5293e-120">Czas trwania oczekiwania w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="5293e-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="5293e-121">Np.: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="5293e-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5293e-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="5293e-122">-HealthCheckProperties</span></span>
<span data-ttu-id="5293e-123">Właściwości kontroli kondycji.</span><span class="sxs-lookup"><span data-stu-id="5293e-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5293e-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="5293e-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="5293e-125">Ścieżka do pliku, w którym są zdefiniowane właściwości kontroli kondycji.</span><span class="sxs-lookup"><span data-stu-id="5293e-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5293e-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5293e-126">-Location</span></span>
<span data-ttu-id="5293e-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="5293e-127">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5293e-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5293e-128">-Name</span></span>
<span data-ttu-id="5293e-129">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="5293e-129">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5293e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5293e-130">-ResourceGroupName</span></span>
<span data-ttu-id="5293e-131">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="5293e-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5293e-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="5293e-132">-Tag</span></span>
<span data-ttu-id="5293e-133">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="5293e-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5293e-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5293e-134">-Confirm</span></span>
<span data-ttu-id="5293e-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5293e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5293e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5293e-136">-WhatIf</span></span>
<span data-ttu-id="5293e-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5293e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5293e-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5293e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5293e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5293e-139">CommonParameters</span></span>
<span data-ttu-id="5293e-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5293e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5293e-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5293e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5293e-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5293e-142">INPUTS</span></span>

### <span data-ttu-id="5293e-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5293e-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5293e-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5293e-144">OUTPUTS</span></span>

### <span data-ttu-id="5293e-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="5293e-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="5293e-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5293e-146">NOTES</span></span>

## <span data-ttu-id="5293e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5293e-147">RELATED LINKS</span></span>
