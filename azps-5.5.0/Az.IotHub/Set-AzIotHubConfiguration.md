---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190346"
---
# <span data-ttu-id="3c576-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c576-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="3c576-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c576-102">SYNOPSIS</span></span>
<span data-ttu-id="3c576-103">Zaktualizuj pola, które można wyciszyć podczas rejestracji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3c576-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="3c576-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3c576-104">SYNTAX</span></span>

### <span data-ttu-id="3c576-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="3c576-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c576-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3c576-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c576-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3c576-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c576-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3c576-108">DESCRIPTION</span></span>
<span data-ttu-id="3c576-109">Aktualizowanie określonych właściwości konfiguracji automatycznego zarządzania urządzeniami IoT.</span><span class="sxs-lookup"><span data-stu-id="3c576-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="3c576-110">Uwaga: nie można zmylić zawartości konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3c576-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="3c576-111">Właściwości konfiguracji, które można aktualizować, to"etykiety", "metryki", "priorytet" i "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="3c576-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="3c576-112">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="3c576-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="3c576-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3c576-113">EXAMPLES</span></span>

### <span data-ttu-id="3c576-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c576-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="3c576-115">Zmienianie priorytetu konfiguracji urządzenia i aktualizowanie jej warunku docelowego</span><span class="sxs-lookup"><span data-stu-id="3c576-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="3c576-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3c576-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="3c576-117">Aktualizowanie metryk i etykiet konfiguracji urządzenia</span><span class="sxs-lookup"><span data-stu-id="3c576-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="3c576-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c576-118">PARAMETERS</span></span>

### <span data-ttu-id="3c576-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c576-119">-DefaultProfile</span></span>
<span data-ttu-id="3c576-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c576-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c576-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3c576-121">-Force</span></span>
<span data-ttu-id="3c576-122">Pozwala na zamienianie obiektu konfiguracyjne, nawet jeśli został zaktualizowany od czasu ostatniego pobrania.</span><span class="sxs-lookup"><span data-stu-id="3c576-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="3c576-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c576-123">-InputObject</span></span>
<span data-ttu-id="3c576-124">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="3c576-124">IotHub object</span></span>

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

### <span data-ttu-id="3c576-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3c576-125">-IotHubName</span></span>
<span data-ttu-id="3c576-126">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="3c576-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3c576-127">— Etykieta</span><span class="sxs-lookup"><span data-stu-id="3c576-127">-Label</span></span>
<span data-ttu-id="3c576-128">Mapa etykiet, które mają zostać zastosowane do konfiguracji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3c576-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="3c576-129">— Metryka</span><span class="sxs-lookup"><span data-stu-id="3c576-129">-Metric</span></span>
<span data-ttu-id="3c576-130">Kolekcja zapytań dla definicji metryk konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3c576-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="3c576-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3c576-131">-Name</span></span>
<span data-ttu-id="3c576-132">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3c576-132">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c576-133">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="3c576-133">-Priority</span></span>
<span data-ttu-id="3c576-134">Waga konfiguracji urządzenia w przypadku konkurencji (największe zwycięstwo).</span><span class="sxs-lookup"><span data-stu-id="3c576-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="3c576-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c576-135">-ResourceGroupName</span></span>
<span data-ttu-id="3c576-136">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3c576-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3c576-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c576-137">-ResourceId</span></span>
<span data-ttu-id="3c576-138">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="3c576-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3c576-139">- TargetCondition</span><span class="sxs-lookup"><span data-stu-id="3c576-139">-TargetCondition</span></span>
<span data-ttu-id="3c576-140">Warunek docelowy, którego dotyczy konfiguracja urządzenia.</span><span class="sxs-lookup"><span data-stu-id="3c576-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="3c576-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c576-141">-Confirm</span></span>
<span data-ttu-id="3c576-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3c576-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c576-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c576-143">-WhatIf</span></span>
<span data-ttu-id="3c576-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c576-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c576-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3c576-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c576-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c576-146">CommonParameters</span></span>
<span data-ttu-id="3c576-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c576-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c576-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c576-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c576-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c576-149">INPUTS</span></span>

### <span data-ttu-id="3c576-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3c576-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3c576-151">System.String</span><span class="sxs-lookup"><span data-stu-id="3c576-151">System.String</span></span>

## <span data-ttu-id="3c576-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c576-152">OUTPUTS</span></span>

### <span data-ttu-id="3c576-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c576-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="3c576-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3c576-154">NOTES</span></span>

## <span data-ttu-id="3c576-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c576-155">RELATED LINKS</span></span>
