---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 980b680130ca319612bbbf28e787ebd99c4bf8bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972522"
---
# <span data-ttu-id="0388f-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0388f-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="0388f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0388f-102">SYNOPSIS</span></span>
<span data-ttu-id="0388f-103">Pobiera zasady dostępu sieciowego JIT</span><span class="sxs-lookup"><span data-stu-id="0388f-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="0388f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0388f-104">SYNTAX</span></span>

### <span data-ttu-id="0388f-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0388f-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0388f-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="0388f-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0388f-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="0388f-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0388f-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0388f-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0388f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="0388f-109">DESCRIPTION</span></span>
<span data-ttu-id="0388f-110">Zasady dostępu sieciowego "Just In Time" (JIT) umożliwiają definiowanie zasad, które umożliwią prostym użytkownikom utworzenie tymczasowego połączenia sieciowego z maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="0388f-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="0388f-111">Zasady określają, jakie porty, protokoły i źródłowe adresy IP mogą żądać połączenia z maszyną WIRTUALNEj oraz maksymalny czas trwania przed automatycznem zamknięciem połączenia.</span><span class="sxs-lookup"><span data-stu-id="0388f-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="0388f-112">W zasadach możesz również zobaczyć żądanie połączenia, które zostało wprowadzone przy użyciu tych zasad.</span><span class="sxs-lookup"><span data-stu-id="0388f-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="0388f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0388f-113">EXAMPLES</span></span>

### <span data-ttu-id="0388f-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0388f-114">Example 1</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="0388f-115">Uzyskiwanie dostępu do wszystkich zaszeeń dostępu sieciowego JIT w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0388f-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="0388f-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0388f-116">Example 2</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="0388f-117">Pobierz wszystkie grupę zasobów "myService1" do wszystkich zasad dostępu sieciowego JIT</span><span class="sxs-lookup"><span data-stu-id="0388f-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="0388f-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0388f-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="0388f-119">Pobiera określone zasady dostępu do sieci JIT</span><span class="sxs-lookup"><span data-stu-id="0388f-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="0388f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0388f-120">PARAMETERS</span></span>

### <span data-ttu-id="0388f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0388f-121">-DefaultProfile</span></span>
<span data-ttu-id="0388f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0388f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0388f-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0388f-123">-Location</span></span>
<span data-ttu-id="0388f-124">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="0388f-124">Location.</span></span>

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

### <span data-ttu-id="0388f-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0388f-125">-Name</span></span>
<span data-ttu-id="0388f-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0388f-126">Resource name.</span></span>

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

### <span data-ttu-id="0388f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0388f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0388f-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0388f-128">Resource group name.</span></span>

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

### <span data-ttu-id="0388f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0388f-129">-ResourceId</span></span>
<span data-ttu-id="0388f-130">Identyfikator zasobu zasobu jit Network Access Policy.</span><span class="sxs-lookup"><span data-stu-id="0388f-130">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="0388f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0388f-131">CommonParameters</span></span>
<span data-ttu-id="0388f-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0388f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0388f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0388f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0388f-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0388f-134">INPUTS</span></span>

### <span data-ttu-id="0388f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0388f-135">System.String</span></span>

## <span data-ttu-id="0388f-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0388f-136">OUTPUTS</span></span>

### <span data-ttu-id="0388f-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0388f-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="0388f-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0388f-138">NOTES</span></span>

## <span data-ttu-id="0388f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0388f-139">RELATED LINKS</span></span>
