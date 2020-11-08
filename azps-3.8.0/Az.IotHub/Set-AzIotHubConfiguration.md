---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 9b6c9b77ae29214c7d998e3d2c859e4ac7521db1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050380"
---
# <span data-ttu-id="d0df9-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0df9-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="d0df9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0df9-102">SYNOPSIS</span></span>
<span data-ttu-id="d0df9-103">Zaktualizuj modyfikowalne pola rejestracji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d0df9-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="d0df9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0df9-104">SYNTAX</span></span>

### <span data-ttu-id="d0df9-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0df9-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0df9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0df9-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0df9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0df9-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0df9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d0df9-108">DESCRIPTION</span></span>
<span data-ttu-id="d0df9-109">Zaktualizuj określone właściwości konfiguracji automatycznej zarządzania urządzeniami IoT.</span><span class="sxs-lookup"><span data-stu-id="d0df9-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="d0df9-110">Uwaga: zawartość konfiguracji jest niezmienna.</span><span class="sxs-lookup"><span data-stu-id="d0df9-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="d0df9-111">Właściwości konfiguracji, które można aktualizować, to "etykiety", "metryki", "Priority" i "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="d0df9-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="d0df9-112"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="d0df9-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="d0df9-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0df9-113">EXAMPLES</span></span>

### <span data-ttu-id="d0df9-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0df9-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="d0df9-115">Zmienianie priorytetu konfiguracji urządzenia i aktualizowanie jego warunku docelowego</span><span class="sxs-lookup"><span data-stu-id="d0df9-115">Alter the priority of a device configuration and update its target condition</span></span>

## <span data-ttu-id="d0df9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0df9-116">PARAMETERS</span></span>

### <span data-ttu-id="d0df9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0df9-117">-DefaultProfile</span></span>
<span data-ttu-id="d0df9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0df9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0df9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d0df9-119">-Force</span></span>
<span data-ttu-id="d0df9-120">Umożliwia zamienienie obiektu konfiguracji, nawet jeśli został on zaktualizowany od czasu ostatniego pobrania.</span><span class="sxs-lookup"><span data-stu-id="d0df9-120">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="d0df9-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d0df9-121">-InputObject</span></span>
<span data-ttu-id="d0df9-122">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="d0df9-122">IotHub object</span></span>

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

### <span data-ttu-id="d0df9-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d0df9-123">-IotHubName</span></span>
<span data-ttu-id="d0df9-124">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="d0df9-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d0df9-125">-Label</span><span class="sxs-lookup"><span data-stu-id="d0df9-125">-Label</span></span>
<span data-ttu-id="d0df9-126">Mapa etykiet, które mają zostać zastosowane do konfiguracji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d0df9-126">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="d0df9-127">-Metric</span><span class="sxs-lookup"><span data-stu-id="d0df9-127">-Metric</span></span>
<span data-ttu-id="d0df9-128">Kolekcja zapytań dla definicji metryk konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d0df9-128">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="d0df9-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0df9-129">-Name</span></span>
<span data-ttu-id="d0df9-130">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d0df9-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="d0df9-131">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="d0df9-131">-Priority</span></span>
<span data-ttu-id="d0df9-132">Waga konfiguracji urządzenia w przypadku reguł konkurujących (najwyższy serwer WINS).</span><span class="sxs-lookup"><span data-stu-id="d0df9-132">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="d0df9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0df9-133">-ResourceGroupName</span></span>
<span data-ttu-id="d0df9-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d0df9-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d0df9-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0df9-135">-ResourceId</span></span>
<span data-ttu-id="d0df9-136">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="d0df9-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d0df9-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="d0df9-137">-TargetCondition</span></span>
<span data-ttu-id="d0df9-138">Warunek docelowy, w którym jest stosowana Konfiguracja urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d0df9-138">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="d0df9-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0df9-139">-Confirm</span></span>
<span data-ttu-id="d0df9-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0df9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0df9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0df9-141">-WhatIf</span></span>
<span data-ttu-id="d0df9-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0df9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0df9-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0df9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0df9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0df9-144">CommonParameters</span></span>
<span data-ttu-id="d0df9-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0df9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0df9-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0df9-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0df9-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0df9-147">INPUTS</span></span>

### <span data-ttu-id="d0df9-148">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d0df9-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d0df9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d0df9-149">System.String</span></span>

## <span data-ttu-id="d0df9-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0df9-150">OUTPUTS</span></span>

### <span data-ttu-id="d0df9-151">Microsoft. Azure. Commands. Management. IotHub. models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0df9-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="d0df9-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0df9-152">NOTES</span></span>

## <span data-ttu-id="d0df9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0df9-153">RELATED LINKS</span></span>
