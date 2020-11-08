---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063411"
---
# <span data-ttu-id="05a3f-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="05a3f-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="05a3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="05a3f-103">Pobiera zasób CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="05a3f-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="05a3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05a3f-104">SYNTAX</span></span>

### <span data-ttu-id="05a3f-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="05a3f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05a3f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05a3f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05a3f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="05a3f-107">DESCRIPTION</span></span>
<span data-ttu-id="05a3f-108">Polecenie cmdlet **Get-AzCustomIpPrefix** pobiera co najmniej jeden CustomIpPrefixes z danym zestawem parametrów wejściowych</span><span class="sxs-lookup"><span data-stu-id="05a3f-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="05a3f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05a3f-109">EXAMPLES</span></span>

### <span data-ttu-id="05a3f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05a3f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="05a3f-111">To polecenie pobiera zasób CustomIpPrefix o nazwie myCustomIpPrefix w grupie zasobów myRg</span><span class="sxs-lookup"><span data-stu-id="05a3f-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="05a3f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05a3f-112">PARAMETERS</span></span>

### <span data-ttu-id="05a3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a3f-113">-DefaultProfile</span></span>
<span data-ttu-id="05a3f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05a3f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a3f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05a3f-115">-Name</span></span>
<span data-ttu-id="05a3f-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="05a3f-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="05a3f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05a3f-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a3f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05a3f-119">-ResourceId</span></span>
<span data-ttu-id="05a3f-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="05a3f-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a3f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a3f-121">CommonParameters</span></span>
<span data-ttu-id="05a3f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a3f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a3f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05a3f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a3f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05a3f-124">INPUTS</span></span>

### <span data-ttu-id="05a3f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="05a3f-125">System.String</span></span>

## <span data-ttu-id="05a3f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05a3f-126">OUTPUTS</span></span>

### <span data-ttu-id="05a3f-127">Microsoft. Azure. Commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="05a3f-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="05a3f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05a3f-128">NOTES</span></span>

## <span data-ttu-id="05a3f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05a3f-129">RELATED LINKS</span></span>

[<span data-ttu-id="05a3f-130">Nowe — AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="05a3f-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="05a3f-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="05a3f-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="05a3f-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="05a3f-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)