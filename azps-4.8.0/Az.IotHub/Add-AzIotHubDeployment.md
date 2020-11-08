---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220940"
---
# <span data-ttu-id="42f21-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="42f21-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="42f21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42f21-102">SYNOPSIS</span></span>
<span data-ttu-id="42f21-103">Dodaj wdrożenie programu IoT Edge w docelowym Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="42f21-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="42f21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42f21-104">SYNTAX</span></span>

### <span data-ttu-id="42f21-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42f21-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f21-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="42f21-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f21-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="42f21-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42f21-108">Opis</span><span class="sxs-lookup"><span data-stu-id="42f21-108">DESCRIPTION</span></span>
<span data-ttu-id="42f21-109">W przypadku obliczania na żądanie można utworzyć wyniki wdrażania programu Edge za pomocą metryk zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="42f21-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="42f21-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="42f21-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="42f21-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42f21-111">EXAMPLES</span></span>

### <span data-ttu-id="42f21-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42f21-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="42f21-113">Utwórz wdrożenie krawędziowe z metadanymi domyślnymi.</span><span class="sxs-lookup"><span data-stu-id="42f21-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="42f21-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="42f21-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="42f21-115">Utwórz wdrożenie krawędziowe o priorytecie 3, które obowiązują w sytuacji, gdy urządzenie jest oznakowane w budynku 9, a środowisko to "test".</span><span class="sxs-lookup"><span data-stu-id="42f21-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="42f21-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="42f21-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="42f21-117">Utwórz wdrożenie na podstawie metryki użytkownika.</span><span class="sxs-lookup"><span data-stu-id="42f21-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="42f21-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="42f21-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="42f21-119">Utwórz wdrożenie krawędzi z etykietami.</span><span class="sxs-lookup"><span data-stu-id="42f21-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="42f21-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="42f21-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="42f21-121">Utwórz wdrożenie na krawędzi z zawartością.</span><span class="sxs-lookup"><span data-stu-id="42f21-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="42f21-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42f21-122">PARAMETERS</span></span>

### <span data-ttu-id="42f21-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f21-123">-DefaultProfile</span></span>
<span data-ttu-id="42f21-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42f21-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42f21-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42f21-125">-InputObject</span></span>
<span data-ttu-id="42f21-126">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="42f21-126">IotHub object</span></span>

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

### <span data-ttu-id="42f21-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="42f21-127">-IotHubName</span></span>
<span data-ttu-id="42f21-128">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="42f21-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="42f21-129">-Label</span><span class="sxs-lookup"><span data-stu-id="42f21-129">-Label</span></span>
<span data-ttu-id="42f21-130">Mapa etykiet, które mają zostać zastosowane do wdrożenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="42f21-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="42f21-131">-Metric</span><span class="sxs-lookup"><span data-stu-id="42f21-131">-Metric</span></span>
<span data-ttu-id="42f21-132">Kolekcja zapytań dla definicji metryk wdrażania programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="42f21-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="42f21-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="42f21-133">-ModulesContent</span></span>
<span data-ttu-id="42f21-134">Zawartość wdrożenia modułów na urządzeniach IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="42f21-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="42f21-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42f21-135">-Name</span></span>
<span data-ttu-id="42f21-136">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="42f21-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="42f21-137">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="42f21-137">-Priority</span></span>
<span data-ttu-id="42f21-138">Waga wdrożenia w przypadku reguł konkurujących (najwyższy serwer WINS).</span><span class="sxs-lookup"><span data-stu-id="42f21-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="42f21-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f21-139">-ResourceGroupName</span></span>
<span data-ttu-id="42f21-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="42f21-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="42f21-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42f21-141">-ResourceId</span></span>
<span data-ttu-id="42f21-142">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="42f21-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="42f21-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="42f21-143">-TargetCondition</span></span>
<span data-ttu-id="42f21-144">Warunek docelowy, w którym obowiązuje wdrożenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="42f21-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="42f21-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42f21-145">-Confirm</span></span>
<span data-ttu-id="42f21-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42f21-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42f21-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42f21-147">-WhatIf</span></span>
<span data-ttu-id="42f21-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42f21-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42f21-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42f21-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42f21-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f21-150">CommonParameters</span></span>
<span data-ttu-id="42f21-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f21-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f21-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f21-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f21-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42f21-153">INPUTS</span></span>

### <span data-ttu-id="42f21-154">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="42f21-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="42f21-155">System. String</span><span class="sxs-lookup"><span data-stu-id="42f21-155">System.String</span></span>

## <span data-ttu-id="42f21-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42f21-156">OUTPUTS</span></span>

### <span data-ttu-id="42f21-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="42f21-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="42f21-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42f21-158">NOTES</span></span>

## <span data-ttu-id="42f21-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42f21-159">RELATED LINKS</span></span>
