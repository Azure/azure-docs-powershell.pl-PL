---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225693"
---
# <span data-ttu-id="8afd1-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8afd1-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="8afd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8afd1-102">SYNOPSIS</span></span>
<span data-ttu-id="8afd1-103">Tworzenie lub aktualizowanie grupy zabezpieczeń urządzenia</span><span class="sxs-lookup"><span data-stu-id="8afd1-103">Create or update device security group</span></span>

## <span data-ttu-id="8afd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8afd1-104">SYNTAX</span></span>

### <span data-ttu-id="8afd1-105">ResourceIdLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8afd1-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8afd1-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="8afd1-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8afd1-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="8afd1-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8afd1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8afd1-108">DESCRIPTION</span></span>
<span data-ttu-id="8afd1-109">Polecenie cmdlet Set-AzDeviceSecurityGroup służy do tworzenia lub aktualizowania grupy zabezpieczeń urządzenia zdefiniowanej w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="8afd1-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="8afd1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8afd1-110">EXAMPLES</span></span>

### <span data-ttu-id="8afd1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8afd1-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="8afd1-112">Aktualizowanie istniejącej grupy zabezpieczeń urządzenia z Centrum IoT "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" z typem reguły "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="8afd1-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="8afd1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8afd1-113">PARAMETERS</span></span>

### <span data-ttu-id="8afd1-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="8afd1-114">-AllowlistRule</span></span>
<span data-ttu-id="8afd1-115">Zezwalanie na reguły list.</span><span class="sxs-lookup"><span data-stu-id="8afd1-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8afd1-116">-DefaultProfile</span></span>
<span data-ttu-id="8afd1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8afd1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8afd1-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="8afd1-118">-DenylistRule</span></span>
<span data-ttu-id="8afd1-119">Odmowa reguł listy.</span><span class="sxs-lookup"><span data-stu-id="8afd1-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afd1-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="8afd1-120">-HubResourceId</span></span>
<span data-ttu-id="8afd1-121">Identyfikator zasobu Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="8afd1-121">IoT Hub resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afd1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8afd1-122">-InputObject</span></span>
<span data-ttu-id="8afd1-123">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="8afd1-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8afd1-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8afd1-124">-Name</span></span>
<span data-ttu-id="8afd1-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8afd1-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afd1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8afd1-126">-ResourceId</span></span>
<span data-ttu-id="8afd1-127">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="8afd1-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8afd1-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="8afd1-128">-ThresholdRule</span></span>
<span data-ttu-id="8afd1-129">Reguły progu.</span><span class="sxs-lookup"><span data-stu-id="8afd1-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afd1-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="8afd1-130">-TimeWindowRule</span></span>
<span data-ttu-id="8afd1-131">Reguły dotyczące okien czasu.</span><span class="sxs-lookup"><span data-stu-id="8afd1-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afd1-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8afd1-132">-Confirm</span></span>
<span data-ttu-id="8afd1-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8afd1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8afd1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8afd1-134">-WhatIf</span></span>
<span data-ttu-id="8afd1-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8afd1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8afd1-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8afd1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8afd1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8afd1-137">CommonParameters</span></span>
<span data-ttu-id="8afd1-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8afd1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8afd1-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8afd1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8afd1-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8afd1-140">INPUTS</span></span>

### <span data-ttu-id="8afd1-141">Microsoft. Azure. Commands. Security. models. DeviceSecurityGroups. PSThresholdCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="8afd1-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="8afd1-142">Microsoft. Azure. Commands. Security. models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="8afd1-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="8afd1-143">Microsoft. Azure. Commands. Security. models. DeviceSecurityGroups. PSAllowlistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="8afd1-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="8afd1-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="8afd1-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="8afd1-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8afd1-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="8afd1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8afd1-146">System.String</span></span>

## <span data-ttu-id="8afd1-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8afd1-147">OUTPUTS</span></span>

### <span data-ttu-id="8afd1-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8afd1-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="8afd1-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8afd1-149">NOTES</span></span>

## <span data-ttu-id="8afd1-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8afd1-150">RELATED LINKS</span></span>
