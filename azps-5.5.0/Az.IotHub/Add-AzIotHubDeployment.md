---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 0e3065cb2ee668f6b0ef5b20ac25ee51d922edc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188275"
---
# <span data-ttu-id="e8439-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="e8439-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="e8439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8439-102">SYNOPSIS</span></span>
<span data-ttu-id="e8439-103">Dodaj wdrożenie IoT Edge w docelowym centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="e8439-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="e8439-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e8439-104">SYNTAX</span></span>

### <span data-ttu-id="e8439-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e8439-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8439-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e8439-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8439-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e8439-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8439-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e8439-108">DESCRIPTION</span></span>
<span data-ttu-id="e8439-109">Wdrożenia brzegowe można tworzyć za pomocą metryk zdefiniowanych przez użytkownika do oceny na żądanie.</span><span class="sxs-lookup"><span data-stu-id="e8439-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="e8439-110">Aby https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="e8439-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="e8439-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e8439-111">EXAMPLES</span></span>

### <span data-ttu-id="e8439-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8439-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="e8439-113">Utwórz wdrożenie przeglądarki Edge z domyślnymi metadanymi.</span><span class="sxs-lookup"><span data-stu-id="e8439-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="e8439-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e8439-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="e8439-115">Utwórz wdrożenie programu Edge o priorytecie 3, które ma zastosowanie pod warunkiem, że urządzenie jest otagowane w budynku 9, a środowisko jest "testowe".</span><span class="sxs-lookup"><span data-stu-id="e8439-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="e8439-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e8439-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="e8439-117">Utwórz wdrożenie w programie Edge z metrykami użytkowników.</span><span class="sxs-lookup"><span data-stu-id="e8439-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="e8439-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e8439-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="e8439-119">Utwórz wdrożenie edge z etykietami.</span><span class="sxs-lookup"><span data-stu-id="e8439-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="e8439-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="e8439-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="e8439-121">Utwórz wdrożenie edge z zawartością.</span><span class="sxs-lookup"><span data-stu-id="e8439-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="e8439-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8439-122">PARAMETERS</span></span>

### <span data-ttu-id="e8439-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8439-123">-DefaultProfile</span></span>
<span data-ttu-id="e8439-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8439-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8439-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8439-125">-InputObject</span></span>
<span data-ttu-id="e8439-126">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="e8439-126">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8439-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e8439-127">-IotHubName</span></span>
<span data-ttu-id="e8439-128">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="e8439-128">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8439-129">— Etykieta</span><span class="sxs-lookup"><span data-stu-id="e8439-129">-Label</span></span>
<span data-ttu-id="e8439-130">Mapa etykiet, które mają zostać zastosowane do wdrożenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="e8439-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="e8439-131">— Metryka</span><span class="sxs-lookup"><span data-stu-id="e8439-131">-Metric</span></span>
<span data-ttu-id="e8439-132">Kolekcja zapytań dla definicji wdrażania IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="e8439-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="e8439-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="e8439-133">-ModulesContent</span></span>
<span data-ttu-id="e8439-134">Zawartość wdrażania modułów dla urządzeń Edge IoT.</span><span class="sxs-lookup"><span data-stu-id="e8439-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="e8439-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e8439-135">-Name</span></span>
<span data-ttu-id="e8439-136">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e8439-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="e8439-137">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="e8439-137">-Priority</span></span>
<span data-ttu-id="e8439-138">Waga wdrożenia w przypadku konkurencji (najwyższe zwycięstwo).</span><span class="sxs-lookup"><span data-stu-id="e8439-138">Weight of deployment in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8439-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8439-139">-ResourceGroupName</span></span>
<span data-ttu-id="e8439-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e8439-140">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8439-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8439-141">-ResourceId</span></span>
<span data-ttu-id="e8439-142">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="e8439-142">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8439-143">- TargetCondition</span><span class="sxs-lookup"><span data-stu-id="e8439-143">-TargetCondition</span></span>
<span data-ttu-id="e8439-144">Warunek docelowy, którego dotyczy wdrożenie programu Edge.</span><span class="sxs-lookup"><span data-stu-id="e8439-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="e8439-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8439-145">-Confirm</span></span>
<span data-ttu-id="e8439-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e8439-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8439-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8439-147">-WhatIf</span></span>
<span data-ttu-id="e8439-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8439-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8439-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e8439-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8439-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8439-150">CommonParameters</span></span>
<span data-ttu-id="e8439-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8439-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8439-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8439-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8439-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8439-153">INPUTS</span></span>

### <span data-ttu-id="e8439-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e8439-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e8439-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e8439-155">System.String</span></span>

## <span data-ttu-id="e8439-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8439-156">OUTPUTS</span></span>

### <span data-ttu-id="e8439-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="e8439-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="e8439-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e8439-158">NOTES</span></span>

## <span data-ttu-id="e8439-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8439-159">RELATED LINKS</span></span>
