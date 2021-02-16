---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203095"
---
# <span data-ttu-id="4f2d9-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f2d9-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="4f2d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="4f2d9-103">Pobiera zasób CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f2d9-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="4f2d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4f2d9-104">SYNTAX</span></span>

### <span data-ttu-id="4f2d9-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4f2d9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f2d9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f2d9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f2d9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4f2d9-107">DESCRIPTION</span></span>
<span data-ttu-id="4f2d9-108">Polecenie **cmdlet Get-AzCustomIpPrefix** pobiera co najmniej jedno polecenie CustomIpPrefixs z zestawem parametrów wejściowych</span><span class="sxs-lookup"><span data-stu-id="4f2d9-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="4f2d9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4f2d9-109">EXAMPLES</span></span>

### <span data-ttu-id="4f2d9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4f2d9-110">Example 1</span></span>
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

<span data-ttu-id="4f2d9-111">To polecenie pobiera zasób CustomIpPrefix o nazwie myCustomIpPrefix w grupie zasobów myRg</span><span class="sxs-lookup"><span data-stu-id="4f2d9-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="4f2d9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f2d9-112">PARAMETERS</span></span>

### <span data-ttu-id="4f2d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f2d9-113">-DefaultProfile</span></span>
<span data-ttu-id="4f2d9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f2d9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f2d9-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4f2d9-115">-Name</span></span>
<span data-ttu-id="4f2d9-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4f2d9-116">The resource name.</span></span>

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

### <span data-ttu-id="4f2d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f2d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="4f2d9-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4f2d9-118">The resource group name.</span></span>

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

### <span data-ttu-id="4f2d9-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f2d9-119">-ResourceId</span></span>
<span data-ttu-id="4f2d9-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="4f2d9-120">The resource id.</span></span>

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

### <span data-ttu-id="4f2d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f2d9-121">CommonParameters</span></span>
<span data-ttu-id="4f2d9-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f2d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f2d9-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f2d9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f2d9-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f2d9-124">INPUTS</span></span>

### <span data-ttu-id="4f2d9-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4f2d9-125">System.String</span></span>

## <span data-ttu-id="4f2d9-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f2d9-126">OUTPUTS</span></span>

### <span data-ttu-id="4f2d9-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f2d9-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="4f2d9-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4f2d9-128">NOTES</span></span>

## <span data-ttu-id="4f2d9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f2d9-129">RELATED LINKS</span></span>

[<span data-ttu-id="4f2d9-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f2d9-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="4f2d9-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f2d9-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="4f2d9-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f2d9-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)