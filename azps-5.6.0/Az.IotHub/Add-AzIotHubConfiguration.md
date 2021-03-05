---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 2521d73d26b281e2dbc242e860869e4e31c78208
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997935"
---
# <span data-ttu-id="67c75-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="67c75-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="67c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67c75-102">SYNOPSIS</span></span>
<span data-ttu-id="67c75-103">Dodaj konfigurację automatycznego zarządzania urządzeniami IoT w docelowym centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="67c75-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="67c75-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67c75-104">SYNTAX</span></span>

### <span data-ttu-id="67c75-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67c75-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67c75-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67c75-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67c75-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="67c75-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67c75-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="67c75-108">DESCRIPTION</span></span>
<span data-ttu-id="67c75-109">Zawartość konfiguracji jest niewielka i zmienia się w zależności od urządzenia lub celu modułu.</span><span class="sxs-lookup"><span data-stu-id="67c75-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="67c75-110">Konfiguracje urządzeń mają postać {"deviceContent":{...}}</span><span class="sxs-lookup"><span data-stu-id="67c75-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="67c75-111">Konfiguracje modułów mają postać {"moduleContent":{...}}</span><span class="sxs-lookup"><span data-stu-id="67c75-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="67c75-112">Konfiguracje można zdefiniować za pomocą metryk dostarczonych przez użytkownika na potrzeby oceny na żądanie.</span><span class="sxs-lookup"><span data-stu-id="67c75-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="67c75-113">Metryki użytkowników są różne i mają postać {"queries":{...}}</span><span class="sxs-lookup"><span data-stu-id="67c75-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="67c75-114">lub {"metrics":{"queries":{...}}}.</span><span class="sxs-lookup"><span data-stu-id="67c75-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="67c75-115">Uwaga: Warunek docelowy dla modułów musi zaczynać się od wartości "from devices.modules where".</span><span class="sxs-lookup"><span data-stu-id="67c75-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="67c75-116">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="67c75-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="67c75-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67c75-117">EXAMPLES</span></span>

### <span data-ttu-id="67c75-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67c75-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="67c75-119">Utwórz konfigurację urządzenia przy użyciu domyślnych metadanych.</span><span class="sxs-lookup"><span data-stu-id="67c75-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="67c75-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="67c75-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="67c75-121">Utwórz konfigurację urządzenia o priorytecie 3, która ma zastosowanie pod warunkiem, że urządzenie jest otagowane w budynku 9, a środowisko jest "testowe".</span><span class="sxs-lookup"><span data-stu-id="67c75-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="67c75-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="67c75-122">Example 3</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="67c75-123">Utwórz konfigurację urządzenia przy użyciu metryk użytkowników.</span><span class="sxs-lookup"><span data-stu-id="67c75-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="67c75-124">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="67c75-124">Example 4</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="67c75-125">Utwórz konfigurację urządzenia za pomocą etykiet.</span><span class="sxs-lookup"><span data-stu-id="67c75-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="67c75-126">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="67c75-126">Example 5</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="67c75-127">Utwórz konfigurację urządzenia z zawartością.</span><span class="sxs-lookup"><span data-stu-id="67c75-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="67c75-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67c75-128">PARAMETERS</span></span>

### <span data-ttu-id="67c75-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c75-129">-DefaultProfile</span></span>
<span data-ttu-id="67c75-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67c75-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67c75-131">- DeviceContent</span><span class="sxs-lookup"><span data-stu-id="67c75-131">-DeviceContent</span></span>
<span data-ttu-id="67c75-132">Konfiguracja urządzeń z usługą IotHub.</span><span class="sxs-lookup"><span data-stu-id="67c75-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="67c75-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67c75-133">-InputObject</span></span>
<span data-ttu-id="67c75-134">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="67c75-134">IotHub object</span></span>

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

### <span data-ttu-id="67c75-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="67c75-135">-IotHubName</span></span>
<span data-ttu-id="67c75-136">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="67c75-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="67c75-137">— Label</span><span class="sxs-lookup"><span data-stu-id="67c75-137">-Label</span></span>
<span data-ttu-id="67c75-138">Mapa etykiet, które mają zostać zastosowane do konfiguracji docelowej.</span><span class="sxs-lookup"><span data-stu-id="67c75-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="67c75-139">— Metryka</span><span class="sxs-lookup"><span data-stu-id="67c75-139">-Metric</span></span>
<span data-ttu-id="67c75-140">Zbieranie zapytań na temat definicji metryk konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="67c75-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="67c75-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="67c75-141">-Name</span></span>
<span data-ttu-id="67c75-142">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="67c75-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="67c75-143">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="67c75-143">-Priority</span></span>
<span data-ttu-id="67c75-144">Waga konfiguracji urządzenia w przypadku konkurencji (największe zwycięstwo).</span><span class="sxs-lookup"><span data-stu-id="67c75-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="67c75-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c75-145">-ResourceGroupName</span></span>
<span data-ttu-id="67c75-146">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="67c75-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="67c75-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67c75-147">-ResourceId</span></span>
<span data-ttu-id="67c75-148">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="67c75-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="67c75-149">- TargetCondition</span><span class="sxs-lookup"><span data-stu-id="67c75-149">-TargetCondition</span></span>
<span data-ttu-id="67c75-150">Warunek docelowy, którego dotyczy konfiguracja urządzenia.</span><span class="sxs-lookup"><span data-stu-id="67c75-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="67c75-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67c75-151">-Confirm</span></span>
<span data-ttu-id="67c75-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="67c75-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67c75-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c75-153">-WhatIf</span></span>
<span data-ttu-id="67c75-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67c75-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67c75-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="67c75-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67c75-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c75-156">CommonParameters</span></span>
<span data-ttu-id="67c75-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67c75-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c75-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67c75-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c75-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67c75-159">INPUTS</span></span>

### <span data-ttu-id="67c75-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="67c75-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="67c75-161">System.String</span><span class="sxs-lookup"><span data-stu-id="67c75-161">System.String</span></span>

## <span data-ttu-id="67c75-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67c75-162">OUTPUTS</span></span>

### <span data-ttu-id="67c75-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="67c75-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="67c75-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67c75-164">NOTES</span></span>

## <span data-ttu-id="67c75-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67c75-165">RELATED LINKS</span></span>
