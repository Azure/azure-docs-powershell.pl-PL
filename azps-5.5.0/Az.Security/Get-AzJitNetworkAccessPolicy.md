---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: e82c540b946408671c424a1f86d3266a7e6d6906
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176338"
---
# <span data-ttu-id="10216-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="10216-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="10216-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10216-102">SYNOPSIS</span></span>
<span data-ttu-id="10216-103">Pobiera zasady dostępu sieciowego JIT</span><span class="sxs-lookup"><span data-stu-id="10216-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="10216-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10216-104">SYNTAX</span></span>

### <span data-ttu-id="10216-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="10216-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10216-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="10216-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10216-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="10216-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10216-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="10216-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10216-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="10216-109">DESCRIPTION</span></span>
<span data-ttu-id="10216-110">Zasady dostępu sieciowego just In Time (JIT) umożliwiają definiowanie zasad, które umożliwią prostym użytkownikom utworzenie tymczasowego połączenia sieciowego z maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="10216-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="10216-111">Zasady określają, jakie porty, protokoły i źródłowe adresy IP mogą żądać połączenia z maszyną WIRTUALNEj oraz maksymalny czas trwania przed automatycznem zamknięciem połączenia.</span><span class="sxs-lookup"><span data-stu-id="10216-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="10216-112">W zasadach możesz również zobaczyć żądanie połączenia, które zostało wprowadzone przy użyciu tych zasad.</span><span class="sxs-lookup"><span data-stu-id="10216-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="10216-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10216-113">EXAMPLES</span></span>

### <span data-ttu-id="10216-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10216-114">Example 1</span></span>
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

<span data-ttu-id="10216-115">Uzyskiwanie dostępu do wszystkich zaszeeń dostępu sieciowego JIT w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10216-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="10216-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="10216-116">Example 2</span></span>
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

<span data-ttu-id="10216-117">Pobierz wszystkie grupę zasobów "myService1" do wszystkich zasad dostępu sieciowego JIT</span><span class="sxs-lookup"><span data-stu-id="10216-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="10216-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="10216-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="10216-119">Pobiera określone zasady dostępu do sieci JIT</span><span class="sxs-lookup"><span data-stu-id="10216-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="10216-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10216-120">PARAMETERS</span></span>

### <span data-ttu-id="10216-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10216-121">-DefaultProfile</span></span>
<span data-ttu-id="10216-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10216-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10216-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="10216-123">-Location</span></span>
<span data-ttu-id="10216-124">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="10216-124">Location.</span></span>

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

### <span data-ttu-id="10216-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="10216-125">-Name</span></span>
<span data-ttu-id="10216-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="10216-126">Resource name.</span></span>

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

### <span data-ttu-id="10216-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10216-127">-ResourceGroupName</span></span>
<span data-ttu-id="10216-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10216-128">Resource group name.</span></span>

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

### <span data-ttu-id="10216-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10216-129">-ResourceId</span></span>
<span data-ttu-id="10216-130">Identyfikator zasobu zasobu jit Network Access Policy.</span><span class="sxs-lookup"><span data-stu-id="10216-130">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="10216-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10216-131">CommonParameters</span></span>
<span data-ttu-id="10216-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10216-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10216-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10216-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10216-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10216-134">INPUTS</span></span>

### <span data-ttu-id="10216-135">System.String</span><span class="sxs-lookup"><span data-stu-id="10216-135">System.String</span></span>

## <span data-ttu-id="10216-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10216-136">OUTPUTS</span></span>

### <span data-ttu-id="10216-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="10216-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="10216-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10216-138">NOTES</span></span>

## <span data-ttu-id="10216-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10216-139">RELATED LINKS</span></span>
