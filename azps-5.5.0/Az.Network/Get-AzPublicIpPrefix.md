---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 567fdda7c4f95a1bcdecab172223608ec78ef1f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184698"
---
# <span data-ttu-id="9cd00-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cd00-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="9cd00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd00-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd00-103">Otrzymuje prefiks publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="9cd00-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="9cd00-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9cd00-104">SYNTAX</span></span>

### <span data-ttu-id="9cd00-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9cd00-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9cd00-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cd00-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cd00-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9cd00-107">DESCRIPTION</span></span>
<span data-ttu-id="9cd00-108">Polecenie **cmdlet Get-AzPublicIpPrefix** pobiera jeden lub więcej prefiksów IP publicznych w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cd00-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="9cd00-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9cd00-109">EXAMPLES</span></span>

### <span data-ttu-id="9cd00-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9cd00-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier":"Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="9cd00-111">To polecenie pobiera publiczny zasób prefiksu IP z zasobem myPublicIpPrefix1 w grupie zasobów myRg</span><span class="sxs-lookup"><span data-stu-id="9cd00-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="9cd00-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9cd00-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier": "Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="9cd00-113">To polecenie pobiera wszystkie publiczne zasoby prefiksu IP, których nazwy zaczynają się od elementu myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="9cd00-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="9cd00-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cd00-114">PARAMETERS</span></span>

### <span data-ttu-id="9cd00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd00-115">-DefaultProfile</span></span>
<span data-ttu-id="9cd00-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cd00-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9cd00-117">-Name</span></span>
<span data-ttu-id="9cd00-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9cd00-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9cd00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd00-119">-ResourceGroupName</span></span>
<span data-ttu-id="9cd00-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cd00-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9cd00-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cd00-121">-ResourceId</span></span>
<span data-ttu-id="9cd00-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9cd00-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd00-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd00-123">CommonParameters</span></span>
<span data-ttu-id="9cd00-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd00-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd00-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cd00-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd00-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cd00-126">INPUTS</span></span>

### <span data-ttu-id="9cd00-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9cd00-127">System.String</span></span>

## <span data-ttu-id="9cd00-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cd00-128">OUTPUTS</span></span>

### <span data-ttu-id="9cd00-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cd00-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="9cd00-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9cd00-130">NOTES</span></span>

## <span data-ttu-id="9cd00-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cd00-131">RELATED LINKS</span></span>

[<span data-ttu-id="9cd00-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cd00-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="9cd00-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cd00-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="9cd00-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9cd00-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
