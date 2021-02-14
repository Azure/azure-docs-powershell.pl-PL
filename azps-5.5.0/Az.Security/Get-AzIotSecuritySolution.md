---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176362"
---
# <span data-ttu-id="af856-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="af856-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="af856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af856-102">SYNOPSIS</span></span>
<span data-ttu-id="af856-103">Uzyskaj rozwiązanie zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="af856-103">Get IoT security solution</span></span>

## <span data-ttu-id="af856-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="af856-104">SYNTAX</span></span>

### <span data-ttu-id="af856-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="af856-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af856-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="af856-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af856-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="af856-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af856-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="af856-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af856-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="af856-109">DESCRIPTION</span></span>
<span data-ttu-id="af856-110">Polecenie Get-AzIotSecuritySolution zwraca co najmniej jedno rozwiązanie zabezpieczeń iot.</span><span class="sxs-lookup"><span data-stu-id="af856-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="af856-111">Rozwiązanie zabezpieczeń IoT zbiera dane zabezpieczeń i zdarzenia z urządzeń iot i centrum iot, aby chronić zagrożenia i je wykrywać.</span><span class="sxs-lookup"><span data-stu-id="af856-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="af856-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="af856-112">EXAMPLES</span></span>

### <span data-ttu-id="af856-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af856-113">Example 1</span></span>
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

<span data-ttu-id="af856-114">Uzyskiwanie rozwiązania "MySample" w grupie zasobów "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="af856-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="af856-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="af856-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="af856-116">Uzyskiwanie listy wszystkich rozwiązań zabezpieczeń w grupie zasobów "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="af856-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="af856-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af856-117">PARAMETERS</span></span>

### <span data-ttu-id="af856-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af856-118">-DefaultProfile</span></span>
<span data-ttu-id="af856-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="af856-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af856-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="af856-120">-Name</span></span>
<span data-ttu-id="af856-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="af856-121">Resource name.</span></span>

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

### <span data-ttu-id="af856-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af856-122">-ResourceGroupName</span></span>
<span data-ttu-id="af856-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="af856-123">Resource group name.</span></span>

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

### <span data-ttu-id="af856-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af856-124">-ResourceId</span></span>
<span data-ttu-id="af856-125">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="af856-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="af856-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af856-126">CommonParameters</span></span>
<span data-ttu-id="af856-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af856-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af856-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af856-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af856-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af856-129">INPUTS</span></span>

### <span data-ttu-id="af856-130">System.String</span><span class="sxs-lookup"><span data-stu-id="af856-130">System.String</span></span>

## <span data-ttu-id="af856-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af856-131">OUTPUTS</span></span>

### <span data-ttu-id="af856-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="af856-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="af856-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="af856-133">NOTES</span></span>

## <span data-ttu-id="af856-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af856-134">RELATED LINKS</span></span>
