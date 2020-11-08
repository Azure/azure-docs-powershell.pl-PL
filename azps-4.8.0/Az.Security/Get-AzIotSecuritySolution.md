---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222954"
---
# <span data-ttu-id="8f69e-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="8f69e-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="8f69e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f69e-102">SYNOPSIS</span></span>
<span data-ttu-id="8f69e-103">Uzyskaj rozwiązanie dotyczące zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="8f69e-103">Get IoT security solution</span></span>

## <span data-ttu-id="8f69e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f69e-104">SYNTAX</span></span>

### <span data-ttu-id="8f69e-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8f69e-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f69e-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="8f69e-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f69e-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="8f69e-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f69e-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="8f69e-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f69e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8f69e-109">DESCRIPTION</span></span>
<span data-ttu-id="8f69e-110">Polecenie cmdlet Get-AzIotSecuritySolution zwraca co najmniej jedno rozwiązanie w ramach zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="8f69e-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="8f69e-111">Rozwiązanie zabezpieczeń IoT gromadzi dane i zdarzenia zabezpieczeń z urządzeń IoT oraz centrum IoT, aby ułatwić zapobieganie i wykrywanie zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="8f69e-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="8f69e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f69e-112">EXAMPLES</span></span>

### <span data-ttu-id="8f69e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f69e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="8f69e-114">Uzyskaj rozwiązanie "The sample" w grupie zasobów "Moja zasobów"</span><span class="sxs-lookup"><span data-stu-id="8f69e-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="8f69e-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8f69e-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="8f69e-116">Pobierz listę wszystkich rozwiązań zabezpieczeń w grupie zasobów "Moja zasobów"</span><span class="sxs-lookup"><span data-stu-id="8f69e-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="8f69e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f69e-117">PARAMETERS</span></span>

### <span data-ttu-id="8f69e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f69e-118">-DefaultProfile</span></span>
<span data-ttu-id="8f69e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f69e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f69e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8f69e-120">-Name</span></span>
<span data-ttu-id="8f69e-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8f69e-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f69e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f69e-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f69e-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f69e-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f69e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f69e-124">-ResourceId</span></span>
<span data-ttu-id="8f69e-125">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="8f69e-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8f69e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f69e-126">CommonParameters</span></span>
<span data-ttu-id="8f69e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f69e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f69e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f69e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f69e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f69e-129">INPUTS</span></span>

### <span data-ttu-id="8f69e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8f69e-130">System.String</span></span>

## <span data-ttu-id="8f69e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f69e-131">OUTPUTS</span></span>

### <span data-ttu-id="8f69e-132">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="8f69e-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="8f69e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f69e-133">NOTES</span></span>

## <span data-ttu-id="8f69e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f69e-134">RELATED LINKS</span></span>
