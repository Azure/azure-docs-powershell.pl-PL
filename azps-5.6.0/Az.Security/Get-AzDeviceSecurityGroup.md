---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 52fae225184b83675f21af941fa125576252ffbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014890"
---
# <span data-ttu-id="356e1-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="356e1-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="356e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="356e1-102">SYNOPSIS</span></span>
<span data-ttu-id="356e1-103">Uzyskaj grupę zabezpieczeń urządzeń (zabezpieczenia centrum IoT)</span><span class="sxs-lookup"><span data-stu-id="356e1-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="356e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="356e1-104">SYNTAX</span></span>

### <span data-ttu-id="356e1-105">ResourceIdScope (domyślna)</span><span class="sxs-lookup"><span data-stu-id="356e1-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="356e1-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="356e1-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="356e1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="356e1-107">DESCRIPTION</span></span>
<span data-ttu-id="356e1-108">Polecenie Get-AzDeviceSecurityGroup zwraca grupę zabezpieczeń urządzenia zdefiniowaną w rozwiązaniu zabezpieczeń iot</span><span class="sxs-lookup"><span data-stu-id="356e1-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="356e1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="356e1-109">EXAMPLES</span></span>

### <span data-ttu-id="356e1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="356e1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
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

<span data-ttu-id="356e1-111">Pobierz grupę zabezpieczeń urządzeń "MySecurityGroup" w centrum IoT z identyfikatorem ponownego źródła "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHubs"</span><span class="sxs-lookup"><span data-stu-id="356e1-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="356e1-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="356e1-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="356e1-113">Uzyskaj listę grupy zabezpieczeń urządzeń w centrum IoT z identyfikatorem ponownego źródła "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHubs"</span><span class="sxs-lookup"><span data-stu-id="356e1-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="356e1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="356e1-114">PARAMETERS</span></span>

### <span data-ttu-id="356e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356e1-115">-DefaultProfile</span></span>
<span data-ttu-id="356e1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="356e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="356e1-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="356e1-117">-HubResourceId</span></span>
<span data-ttu-id="356e1-118">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="356e1-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="356e1-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="356e1-119">-Name</span></span>
<span data-ttu-id="356e1-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="356e1-120">Resource name.</span></span>

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

### <span data-ttu-id="356e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356e1-121">CommonParameters</span></span>
<span data-ttu-id="356e1-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356e1-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="356e1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356e1-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="356e1-124">INPUTS</span></span>

### <span data-ttu-id="356e1-125">Brak</span><span class="sxs-lookup"><span data-stu-id="356e1-125">None</span></span>

## <span data-ttu-id="356e1-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="356e1-126">OUTPUTS</span></span>

### <span data-ttu-id="356e1-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="356e1-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="356e1-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="356e1-128">NOTES</span></span>

## <span data-ttu-id="356e1-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="356e1-129">RELATED LINKS</span></span>
