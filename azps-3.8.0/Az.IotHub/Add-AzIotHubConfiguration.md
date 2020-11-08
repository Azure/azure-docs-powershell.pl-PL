---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053213"
---
# <span data-ttu-id="b72e2-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="b72e2-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="b72e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b72e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b72e2-103">Dodaj konfigurację automatycznej zarządzania urządzeniami IoT w docelowym Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="b72e2-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="b72e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b72e2-104">SYNTAX</span></span>

### <span data-ttu-id="b72e2-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b72e2-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b72e2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b72e2-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b72e2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b72e2-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b72e2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b72e2-108">DESCRIPTION</span></span>
<span data-ttu-id="b72e2-109">Zawartość konfiguracji ma format JSON i jest niewielka w zależności od zamierzonego urządzenia lub modułu.</span><span class="sxs-lookup"><span data-stu-id="b72e2-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="b72e2-110">Konfiguracje urządzeń są w postaci {"deviceContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="b72e2-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="b72e2-111">Konfiguracje modułów są w postaci {"moduleContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="b72e2-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="b72e2-112">Konfiguracje można definiować za pomocą metryk dostarczanych przez użytkownika na potrzeby oceny popytu.</span><span class="sxs-lookup"><span data-stu-id="b72e2-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="b72e2-113">Metryki użytkowników są notacją JSON i w postaci {"zapytania": {...}}</span><span class="sxs-lookup"><span data-stu-id="b72e2-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="b72e2-114">lub {"metryki": {"zapytania": {...}}}.</span><span class="sxs-lookup"><span data-stu-id="b72e2-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="b72e2-115">Uwaga: warunki docelowe modułów muszą rozpoczynać się od "od urządzenia. moduły, gdzie".</span><span class="sxs-lookup"><span data-stu-id="b72e2-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="b72e2-116"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="b72e2-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="b72e2-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b72e2-117">EXAMPLES</span></span>

### <span data-ttu-id="b72e2-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b72e2-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="b72e2-119">Utwórz konfigurację urządzenia przy użyciu metadanych domyślnych.</span><span class="sxs-lookup"><span data-stu-id="b72e2-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="b72e2-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b72e2-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="b72e2-121">Utwórz konfigurację urządzenia o priorytecie 3, które obowiązują w sytuacji, gdy urządzenie jest oznakowane w budynku 9, a środowisko to "test".</span><span class="sxs-lookup"><span data-stu-id="b72e2-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="b72e2-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b72e2-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="b72e2-123">Utwórz konfigurację urządzenia za pomocą metryk użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b72e2-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="b72e2-124">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b72e2-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="b72e2-125">Utwórz konfigurację urządzenia przy użyciu etykiet.</span><span class="sxs-lookup"><span data-stu-id="b72e2-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="b72e2-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b72e2-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="b72e2-127">Utwórz konfigurację urządzenia przy użyciu zawartości.</span><span class="sxs-lookup"><span data-stu-id="b72e2-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="b72e2-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b72e2-128">PARAMETERS</span></span>

### <span data-ttu-id="b72e2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b72e2-129">-DefaultProfile</span></span>
<span data-ttu-id="b72e2-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b72e2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b72e2-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="b72e2-131">-DeviceContent</span></span>
<span data-ttu-id="b72e2-132">Konfiguracja urządzeń z IotHub.</span><span class="sxs-lookup"><span data-stu-id="b72e2-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="b72e2-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b72e2-133">-InputObject</span></span>
<span data-ttu-id="b72e2-134">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="b72e2-134">IotHub object</span></span>

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

### <span data-ttu-id="b72e2-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b72e2-135">-IotHubName</span></span>
<span data-ttu-id="b72e2-136">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="b72e2-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b72e2-137">-Label</span><span class="sxs-lookup"><span data-stu-id="b72e2-137">-Label</span></span>
<span data-ttu-id="b72e2-138">Mapa etykiet, które mają zostać zastosowane do konfiguracji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b72e2-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="b72e2-139">-Metric</span><span class="sxs-lookup"><span data-stu-id="b72e2-139">-Metric</span></span>
<span data-ttu-id="b72e2-140">Kolekcja zapytań dla definicji metryk konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="b72e2-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="b72e2-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b72e2-141">-Name</span></span>
<span data-ttu-id="b72e2-142">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="b72e2-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="b72e2-143">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="b72e2-143">-Priority</span></span>
<span data-ttu-id="b72e2-144">Waga konfiguracji urządzenia w przypadku reguł konkurujących (najwyższy serwer WINS).</span><span class="sxs-lookup"><span data-stu-id="b72e2-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="b72e2-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b72e2-145">-ResourceGroupName</span></span>
<span data-ttu-id="b72e2-146">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b72e2-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b72e2-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b72e2-147">-ResourceId</span></span>
<span data-ttu-id="b72e2-148">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="b72e2-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b72e2-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="b72e2-149">-TargetCondition</span></span>
<span data-ttu-id="b72e2-150">Warunek docelowy, w którym jest stosowana Konfiguracja urządzenia.</span><span class="sxs-lookup"><span data-stu-id="b72e2-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="b72e2-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b72e2-151">-Confirm</span></span>
<span data-ttu-id="b72e2-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b72e2-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b72e2-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b72e2-153">-WhatIf</span></span>
<span data-ttu-id="b72e2-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b72e2-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b72e2-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b72e2-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b72e2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b72e2-156">CommonParameters</span></span>
<span data-ttu-id="b72e2-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b72e2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b72e2-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b72e2-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b72e2-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b72e2-159">INPUTS</span></span>

### <span data-ttu-id="b72e2-160">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b72e2-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b72e2-161">System. String</span><span class="sxs-lookup"><span data-stu-id="b72e2-161">System.String</span></span>

## <span data-ttu-id="b72e2-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b72e2-162">OUTPUTS</span></span>

### <span data-ttu-id="b72e2-163">Microsoft. Azure. Commands. Management. IotHub. models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="b72e2-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="b72e2-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b72e2-164">NOTES</span></span>

## <span data-ttu-id="b72e2-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b72e2-165">RELATED LINKS</span></span>
