---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: 58bae669af1fb9a06f4caa95070225f12d1a78aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709587"
---
# <span data-ttu-id="22025-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="22025-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="22025-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22025-102">SYNOPSIS</span></span>
<span data-ttu-id="22025-103">Pobiera grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="22025-103">Gets an application security group.</span></span>

## <span data-ttu-id="22025-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22025-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22025-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22025-105">DESCRIPTION</span></span>
<span data-ttu-id="22025-106">Polecenie cmdlet **Get-AzApplicationSecurityGroup** pobiera grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="22025-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="22025-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22025-107">EXAMPLES</span></span>

### <span data-ttu-id="22025-108">Przykład 1: pobieranie wszystkich grup zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="22025-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="22025-109">Powyższe polecenie zwraca wszystkie grupy zabezpieczeń aplikacji w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="22025-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="22025-110">Przykład 2: pobieranie grup zabezpieczeń aplikacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="22025-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="22025-111">Powyższe polecenie zwraca wszystkie grupy zabezpieczeń aplikacji należące do grupy moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="22025-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="22025-112">Przykład 3: pobieranie określonej grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="22025-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="22025-113">Powyższe polecenie zwraca grupę zabezpieczeń aplikacji MyApplicationSecurityGroup pod grupą zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="22025-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="22025-114">Przykład 4: pobieranie grup zabezpieczeń aplikacji przy użyciu filtrowania.</span><span class="sxs-lookup"><span data-stu-id="22025-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="22025-115">Powyższe polecenie zwraca wszystkie grupy zabezpieczeń aplikacji rozpoczynające się od "MyApplicationSecurityGroup".</span><span class="sxs-lookup"><span data-stu-id="22025-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="22025-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22025-116">PARAMETERS</span></span>

### <span data-ttu-id="22025-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22025-117">-DefaultProfile</span></span>
<span data-ttu-id="22025-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22025-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22025-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22025-119">-Name</span></span>
<span data-ttu-id="22025-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="22025-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="22025-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22025-121">-ResourceGroupName</span></span>
<span data-ttu-id="22025-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22025-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="22025-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22025-123">CommonParameters</span></span>
<span data-ttu-id="22025-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22025-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22025-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22025-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22025-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22025-126">INPUTS</span></span>

### <span data-ttu-id="22025-127">System. String</span><span class="sxs-lookup"><span data-stu-id="22025-127">System.String</span></span>

## <span data-ttu-id="22025-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22025-128">OUTPUTS</span></span>

### <span data-ttu-id="22025-129">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="22025-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="22025-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22025-130">NOTES</span></span>

## <span data-ttu-id="22025-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22025-131">RELATED LINKS</span></span>

[<span data-ttu-id="22025-132">Nowe — AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="22025-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="22025-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="22025-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="22025-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="22025-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="22025-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22025-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)