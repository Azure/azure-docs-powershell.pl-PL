---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386570"
---
# <span data-ttu-id="34ada-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="34ada-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="34ada-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34ada-102">SYNOPSIS</span></span>
<span data-ttu-id="34ada-103">Aktualizowanie modyfikowalnych pól wdrożenia programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="34ada-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="34ada-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34ada-104">SYNTAX</span></span>

### <span data-ttu-id="34ada-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34ada-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ada-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="34ada-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ada-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="34ada-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34ada-108">Opis</span><span class="sxs-lookup"><span data-stu-id="34ada-108">DESCRIPTION</span></span>
<span data-ttu-id="34ada-109">Zaktualizuj określone właściwości wdrożenia programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="34ada-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="34ada-110">Uwaga: zawartość konfiguracji jest niezmienna.</span><span class="sxs-lookup"><span data-stu-id="34ada-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="34ada-111">Właściwości konfiguracji, które można aktualizować, to "etykiety", "metryki", "Priority" i "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="34ada-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="34ada-112"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="34ada-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="34ada-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34ada-113">EXAMPLES</span></span>

### <span data-ttu-id="34ada-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34ada-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="34ada-115">Zmienianie priorytetu wdrożenia programu IoT Edge i aktualizowanie jego warunku docelowego.</span><span class="sxs-lookup"><span data-stu-id="34ada-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="34ada-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="34ada-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="34ada-117">Aktualizowanie metryk i etykiet wdrażania programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="34ada-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="34ada-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34ada-118">PARAMETERS</span></span>

### <span data-ttu-id="34ada-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ada-119">-DefaultProfile</span></span>
<span data-ttu-id="34ada-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34ada-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ada-121">-Force</span><span class="sxs-lookup"><span data-stu-id="34ada-121">-Force</span></span>
<span data-ttu-id="34ada-122">Umożliwia zamienienie obiektu wdrożenia, nawet jeśli został on zaktualizowany od czasu ostatniego pobrania.</span><span class="sxs-lookup"><span data-stu-id="34ada-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="34ada-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34ada-123">-InputObject</span></span>
<span data-ttu-id="34ada-124">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="34ada-124">IotHub object</span></span>

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

### <span data-ttu-id="34ada-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="34ada-125">-IotHubName</span></span>
<span data-ttu-id="34ada-126">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="34ada-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="34ada-127">-Label</span><span class="sxs-lookup"><span data-stu-id="34ada-127">-Label</span></span>
<span data-ttu-id="34ada-128">Mapa etykiet, które mają zostać zastosowane do wdrożenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="34ada-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="34ada-129">-Metric</span><span class="sxs-lookup"><span data-stu-id="34ada-129">-Metric</span></span>
<span data-ttu-id="34ada-130">Kolekcja zapytań dla definicji metryk wdrażania programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="34ada-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="34ada-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34ada-131">-Name</span></span>
<span data-ttu-id="34ada-132">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="34ada-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="34ada-133">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="34ada-133">-Priority</span></span>
<span data-ttu-id="34ada-134">Waga wdrożenia w przypadku reguł konkurujących (najwyższy serwer WINS).</span><span class="sxs-lookup"><span data-stu-id="34ada-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="34ada-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ada-135">-ResourceGroupName</span></span>
<span data-ttu-id="34ada-136">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="34ada-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="34ada-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34ada-137">-ResourceId</span></span>
<span data-ttu-id="34ada-138">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="34ada-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="34ada-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="34ada-139">-TargetCondition</span></span>
<span data-ttu-id="34ada-140">Warunek docelowy, w którym obowiązuje wdrożenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="34ada-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="34ada-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34ada-141">-Confirm</span></span>
<span data-ttu-id="34ada-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34ada-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ada-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ada-143">-WhatIf</span></span>
<span data-ttu-id="34ada-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34ada-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34ada-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34ada-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ada-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ada-146">CommonParameters</span></span>
<span data-ttu-id="34ada-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ada-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ada-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ada-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ada-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34ada-149">INPUTS</span></span>

### <span data-ttu-id="34ada-150">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="34ada-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="34ada-151">System. String</span><span class="sxs-lookup"><span data-stu-id="34ada-151">System.String</span></span>

## <span data-ttu-id="34ada-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34ada-152">OUTPUTS</span></span>

### <span data-ttu-id="34ada-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="34ada-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="34ada-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34ada-154">NOTES</span></span>

## <span data-ttu-id="34ada-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34ada-155">RELATED LINKS</span></span>
