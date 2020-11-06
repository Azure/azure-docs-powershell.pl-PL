---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: bd366b636a29a08bea9124b3c3f4b9b423dc4deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526053"
---
# <span data-ttu-id="f724f-101">Get-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f724f-101">Get-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f724f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f724f-102">SYNOPSIS</span></span>
<span data-ttu-id="f724f-103">Pobiera zasady dostępu do sieci JIT</span><span class="sxs-lookup"><span data-stu-id="f724f-103">Gets the JIT network access policies</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f724f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f724f-104">SYNTAX</span></span>

### <span data-ttu-id="f724f-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f724f-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f724f-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="f724f-106">ResourceGroupScope</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f724f-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="f724f-107">ResourceGroupLevelResource</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f724f-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f724f-108">ResourceId</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f724f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f724f-109">DESCRIPTION</span></span>
<span data-ttu-id="f724f-110">Zasady dostępu do sieci (JIT) umożliwiają zdefiniowanie zasad, które umożliwią prostym użytkownikom tworzenie tymczasowego połączenia sieciowego z maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="f724f-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="f724f-111">Zasady określają, jakie porty, protokoły i źródłowe adresy IP mogą wymagać połączenia z maszyną wirtualną, a maksymalny czas trwania połączenia zostanie automatycznie zamknięty.</span><span class="sxs-lookup"><span data-stu-id="f724f-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="f724f-112">W zasadach możesz również zobaczyć żądanie połączenia wprowadzone przy użyciu tych zasad.</span><span class="sxs-lookup"><span data-stu-id="f724f-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="f724f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f724f-113">EXAMPLES</span></span>

### <span data-ttu-id="f724f-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f724f-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy
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

<span data-ttu-id="f724f-115">Uzyskiwanie wszystkich zasad dostępu do sieci JIT w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="f724f-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="f724f-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f724f-116">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1"
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

<span data-ttu-id="f724f-117">Uzyskiwanie wszystkich zasad dostępu do sieci JIT w grupie zasobów "myService1"</span><span class="sxs-lookup"><span data-stu-id="f724f-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="f724f-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f724f-118">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="f724f-119">Pobiera określone zasady dostępu do sieci JIT.</span><span class="sxs-lookup"><span data-stu-id="f724f-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="f724f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f724f-120">PARAMETERS</span></span>

### <span data-ttu-id="f724f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f724f-121">-DefaultProfile</span></span>
<span data-ttu-id="f724f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f724f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f724f-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f724f-123">-Location</span></span>
<span data-ttu-id="f724f-124">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="f724f-124">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f724f-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f724f-125">-Name</span></span>
<span data-ttu-id="f724f-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f724f-126">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f724f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f724f-127">-ResourceGroupName</span></span>
<span data-ttu-id="f724f-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f724f-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f724f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f724f-129">-ResourceId</span></span>
<span data-ttu-id="f724f-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f724f-130">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f724f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f724f-131">CommonParameters</span></span>
<span data-ttu-id="f724f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f724f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f724f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f724f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f724f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f724f-134">INPUTS</span></span>

### <span data-ttu-id="f724f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f724f-135">System.String</span></span>

## <span data-ttu-id="f724f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f724f-136">OUTPUTS</span></span>

### <span data-ttu-id="f724f-137">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f724f-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f724f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f724f-138">NOTES</span></span>

## <span data-ttu-id="f724f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f724f-139">RELATED LINKS</span></span>
