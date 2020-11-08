---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 1fac3ef0db0022bcb837392bf1c0b64e63c40401
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234721"
---
# <span data-ttu-id="ca65d-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="ca65d-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="ca65d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca65d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca65d-103">Aktualizowanie modyfikowalnych pól wdrożenia programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="ca65d-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="ca65d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca65d-104">SYNTAX</span></span>

### <span data-ttu-id="ca65d-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ca65d-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca65d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca65d-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca65d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca65d-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca65d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ca65d-108">DESCRIPTION</span></span>
<span data-ttu-id="ca65d-109">Zaktualizuj określone właściwości wdrożenia programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="ca65d-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="ca65d-110">Uwaga: zawartość konfiguracji jest niezmienna.</span><span class="sxs-lookup"><span data-stu-id="ca65d-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="ca65d-111">Właściwości konfiguracji, które można aktualizować, to "etykiety", "metryki", "Priority" i "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="ca65d-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="ca65d-112"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="ca65d-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="ca65d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca65d-113">EXAMPLES</span></span>

### <span data-ttu-id="ca65d-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca65d-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="ca65d-115">Zmienianie priorytetu wdrożenia programu IoT Edge i aktualizowanie jego warunku docelowego.</span><span class="sxs-lookup"><span data-stu-id="ca65d-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

## <span data-ttu-id="ca65d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca65d-116">PARAMETERS</span></span>

### <span data-ttu-id="ca65d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca65d-117">-DefaultProfile</span></span>
<span data-ttu-id="ca65d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca65d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca65d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ca65d-119">-Force</span></span>
<span data-ttu-id="ca65d-120">Umożliwia zamienienie obiektu wdrożenia, nawet jeśli został on zaktualizowany od czasu ostatniego pobrania.</span><span class="sxs-lookup"><span data-stu-id="ca65d-120">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="ca65d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca65d-121">-InputObject</span></span>
<span data-ttu-id="ca65d-122">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="ca65d-122">IotHub object</span></span>

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

### <span data-ttu-id="ca65d-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ca65d-123">-IotHubName</span></span>
<span data-ttu-id="ca65d-124">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="ca65d-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ca65d-125">-Label</span><span class="sxs-lookup"><span data-stu-id="ca65d-125">-Label</span></span>
<span data-ttu-id="ca65d-126">Mapa etykiet, które mają zostać zastosowane do wdrożenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="ca65d-126">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="ca65d-127">-Metric</span><span class="sxs-lookup"><span data-stu-id="ca65d-127">-Metric</span></span>
<span data-ttu-id="ca65d-128">Kolekcja zapytań dla definicji metryk wdrażania programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="ca65d-128">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="ca65d-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca65d-129">-Name</span></span>
<span data-ttu-id="ca65d-130">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ca65d-130">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="ca65d-131">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="ca65d-131">-Priority</span></span>
<span data-ttu-id="ca65d-132">Waga wdrożenia w przypadku reguł konkurujących (najwyższy serwer WINS).</span><span class="sxs-lookup"><span data-stu-id="ca65d-132">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="ca65d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca65d-133">-ResourceGroupName</span></span>
<span data-ttu-id="ca65d-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ca65d-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ca65d-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca65d-135">-ResourceId</span></span>
<span data-ttu-id="ca65d-136">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="ca65d-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ca65d-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="ca65d-137">-TargetCondition</span></span>
<span data-ttu-id="ca65d-138">Warunek docelowy, w którym obowiązuje wdrożenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="ca65d-138">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="ca65d-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca65d-139">-Confirm</span></span>
<span data-ttu-id="ca65d-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca65d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca65d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca65d-141">-WhatIf</span></span>
<span data-ttu-id="ca65d-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca65d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca65d-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca65d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca65d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca65d-144">CommonParameters</span></span>
<span data-ttu-id="ca65d-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca65d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca65d-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca65d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca65d-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca65d-147">INPUTS</span></span>

### <span data-ttu-id="ca65d-148">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ca65d-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ca65d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ca65d-149">System.String</span></span>

## <span data-ttu-id="ca65d-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca65d-150">OUTPUTS</span></span>

### <span data-ttu-id="ca65d-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ca65d-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="ca65d-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca65d-152">NOTES</span></span>

## <span data-ttu-id="ca65d-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca65d-153">RELATED LINKS</span></span>
