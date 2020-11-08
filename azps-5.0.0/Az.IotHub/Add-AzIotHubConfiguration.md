---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232262"
---
# <span data-ttu-id="58014-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="58014-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="58014-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58014-102">SYNOPSIS</span></span>
<span data-ttu-id="58014-103">Dodaj konfigurację automatycznej zarządzania urządzeniami IoT w docelowym Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="58014-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="58014-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58014-104">SYNTAX</span></span>

### <span data-ttu-id="58014-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="58014-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58014-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="58014-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58014-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="58014-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58014-108">Opis</span><span class="sxs-lookup"><span data-stu-id="58014-108">DESCRIPTION</span></span>
<span data-ttu-id="58014-109">Zawartość konfiguracji ma format JSON i jest niewielka w zależności od zamierzonego urządzenia lub modułu.</span><span class="sxs-lookup"><span data-stu-id="58014-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="58014-110">Konfiguracje urządzeń są w postaci {"deviceContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="58014-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="58014-111">Konfiguracje modułów są w postaci {"moduleContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="58014-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="58014-112">Konfiguracje można definiować za pomocą metryk dostarczanych przez użytkownika na potrzeby oceny popytu.</span><span class="sxs-lookup"><span data-stu-id="58014-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="58014-113">Metryki użytkowników są notacją JSON i w postaci {"zapytania": {...}}</span><span class="sxs-lookup"><span data-stu-id="58014-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="58014-114">lub {"metryki": {"zapytania": {...}}}.</span><span class="sxs-lookup"><span data-stu-id="58014-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="58014-115">Uwaga: warunki docelowe modułów muszą rozpoczynać się od "od urządzenia. moduły, gdzie".</span><span class="sxs-lookup"><span data-stu-id="58014-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="58014-116"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="58014-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="58014-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58014-117">EXAMPLES</span></span>

### <span data-ttu-id="58014-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58014-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="58014-119">Utwórz konfigurację urządzenia przy użyciu metadanych domyślnych.</span><span class="sxs-lookup"><span data-stu-id="58014-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="58014-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="58014-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="58014-121">Utwórz konfigurację urządzenia o priorytecie 3, które obowiązują w sytuacji, gdy urządzenie jest oznakowane w budynku 9, a środowisko to "test".</span><span class="sxs-lookup"><span data-stu-id="58014-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="58014-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="58014-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="58014-123">Utwórz konfigurację urządzenia za pomocą metryk użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58014-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="58014-124">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="58014-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="58014-125">Utwórz konfigurację urządzenia przy użyciu etykiet.</span><span class="sxs-lookup"><span data-stu-id="58014-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="58014-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="58014-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="58014-127">Utwórz konfigurację urządzenia przy użyciu zawartości.</span><span class="sxs-lookup"><span data-stu-id="58014-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="58014-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58014-128">PARAMETERS</span></span>

### <span data-ttu-id="58014-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58014-129">-DefaultProfile</span></span>
<span data-ttu-id="58014-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58014-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58014-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="58014-131">-DeviceContent</span></span>
<span data-ttu-id="58014-132">Konfiguracja urządzeń z IotHub.</span><span class="sxs-lookup"><span data-stu-id="58014-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="58014-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="58014-133">-InputObject</span></span>
<span data-ttu-id="58014-134">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="58014-134">IotHub object</span></span>

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

### <span data-ttu-id="58014-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="58014-135">-IotHubName</span></span>
<span data-ttu-id="58014-136">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="58014-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="58014-137">-Label</span><span class="sxs-lookup"><span data-stu-id="58014-137">-Label</span></span>
<span data-ttu-id="58014-138">Mapa etykiet, które mają zostać zastosowane do konfiguracji docelowej.</span><span class="sxs-lookup"><span data-stu-id="58014-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="58014-139">-Metric</span><span class="sxs-lookup"><span data-stu-id="58014-139">-Metric</span></span>
<span data-ttu-id="58014-140">Kolekcja zapytań dla definicji metryk konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="58014-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="58014-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58014-141">-Name</span></span>
<span data-ttu-id="58014-142">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="58014-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="58014-143">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="58014-143">-Priority</span></span>
<span data-ttu-id="58014-144">Waga konfiguracji urządzenia w przypadku reguł konkurujących (najwyższy serwer WINS).</span><span class="sxs-lookup"><span data-stu-id="58014-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="58014-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58014-145">-ResourceGroupName</span></span>
<span data-ttu-id="58014-146">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="58014-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="58014-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58014-147">-ResourceId</span></span>
<span data-ttu-id="58014-148">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="58014-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="58014-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="58014-149">-TargetCondition</span></span>
<span data-ttu-id="58014-150">Warunek docelowy, w którym jest stosowana Konfiguracja urządzenia.</span><span class="sxs-lookup"><span data-stu-id="58014-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="58014-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58014-151">-Confirm</span></span>
<span data-ttu-id="58014-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58014-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58014-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58014-153">-WhatIf</span></span>
<span data-ttu-id="58014-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58014-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58014-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58014-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58014-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58014-156">CommonParameters</span></span>
<span data-ttu-id="58014-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58014-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58014-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58014-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58014-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58014-159">INPUTS</span></span>

### <span data-ttu-id="58014-160">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="58014-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="58014-161">System. String</span><span class="sxs-lookup"><span data-stu-id="58014-161">System.String</span></span>

## <span data-ttu-id="58014-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58014-162">OUTPUTS</span></span>

### <span data-ttu-id="58014-163">Microsoft. Azure. Commands. Management. IotHub. models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="58014-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="58014-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58014-164">NOTES</span></span>

## <span data-ttu-id="58014-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58014-165">RELATED LINKS</span></span>
