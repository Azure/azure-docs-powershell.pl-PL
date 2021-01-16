---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355921"
---
# <span data-ttu-id="3d6ad-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="3d6ad-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="3d6ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d6ad-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6ad-103">Tworzy krok.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-103">Creates a step.</span></span>

## <span data-ttu-id="3d6ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d6ad-104">SYNTAX</span></span>

### <span data-ttu-id="3d6ad-105">Poczekaj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3d6ad-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6ad-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="3d6ad-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6ad-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="3d6ad-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d6ad-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3d6ad-108">DESCRIPTION</span></span>
<span data-ttu-id="3d6ad-109">Polecenie cmdlet **New-AzDeploymentManagerStep** umożliwia utworzenie kroku wdrożenia, do którego można odwoływać się w trakcie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="3d6ad-110">Określ *imię i nazwisko*, *ResourceGroupName* oraz wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="3d6ad-111">Zwrócony obiekt można zmodyfikować lokalnie, a następnie zastosować zmiany do kroku przy użyciu polecenia cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="3d6ad-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d6ad-112">EXAMPLES</span></span>

### <span data-ttu-id="3d6ad-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3d6ad-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="3d6ad-114">Tworzy krok w ContosoResourceGroup o nazwie ContosoService1WaitStep z centralą centralną jako lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="3d6ad-115">Właściwość Duration zawiera czas trwania, przez jaki rozmieszczenie będzie oczekiwać przed uruchomieniem następnego kroku.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="3d6ad-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d6ad-116">PARAMETERS</span></span>

### <span data-ttu-id="3d6ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6ad-117">-DefaultProfile</span></span>
<span data-ttu-id="3d6ad-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d6ad-119">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="3d6ad-119">-Duration</span></span>
<span data-ttu-id="3d6ad-120">Czas oczekiwania na oczekiwanie w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="3d6ad-121">Na przykład: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="3d6ad-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="3d6ad-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="3d6ad-122">-HealthCheckProperties</span></span>
<span data-ttu-id="3d6ad-123">Właściwości kontroli kondycji.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-123">The health check properties.</span></span>

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

### <span data-ttu-id="3d6ad-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="3d6ad-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="3d6ad-125">Ścieżka do pliku, w którym są zdefiniowane właściwości kontroli kondycji.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="3d6ad-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3d6ad-126">-Location</span></span>
<span data-ttu-id="3d6ad-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-127">The location of the resource.</span></span>

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

### <span data-ttu-id="3d6ad-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d6ad-128">-Name</span></span>
<span data-ttu-id="3d6ad-129">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-129">The name of the step.</span></span>

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

### <span data-ttu-id="3d6ad-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6ad-130">-ResourceGroupName</span></span>
<span data-ttu-id="3d6ad-131">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-131">The resource group.</span></span>

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

### <span data-ttu-id="3d6ad-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d6ad-132">-Tag</span></span>
<span data-ttu-id="3d6ad-133">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="3d6ad-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d6ad-134">-Confirm</span></span>
<span data-ttu-id="3d6ad-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d6ad-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6ad-136">-WhatIf</span></span>
<span data-ttu-id="3d6ad-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d6ad-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d6ad-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6ad-139">CommonParameters</span></span>
<span data-ttu-id="3d6ad-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d6ad-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6ad-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d6ad-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6ad-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d6ad-142">INPUTS</span></span>

### <span data-ttu-id="3d6ad-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d6ad-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d6ad-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d6ad-144">OUTPUTS</span></span>

### <span data-ttu-id="3d6ad-145">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="3d6ad-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="3d6ad-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d6ad-146">NOTES</span></span>

## <span data-ttu-id="3d6ad-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d6ad-147">RELATED LINKS</span></span>
