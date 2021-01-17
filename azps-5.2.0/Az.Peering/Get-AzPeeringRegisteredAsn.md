---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337537"
---
# <span data-ttu-id="b85a4-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b85a4-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b85a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b85a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b85a4-103">Pobiera zarejestrowany ASN na serwer routingu programu Exchange.</span><span class="sxs-lookup"><span data-stu-id="b85a4-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="b85a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b85a4-104">SYNTAX</span></span>

### <span data-ttu-id="b85a4-105">ByResourceGroupAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b85a4-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b85a4-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="b85a4-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b85a4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b85a4-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b85a4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b85a4-108">DESCRIPTION</span></span>
<span data-ttu-id="b85a4-109">Uzyskaj lub wystaw zarejestrowany ASN.</span><span class="sxs-lookup"><span data-stu-id="b85a4-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="b85a4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b85a4-110">EXAMPLES</span></span>

### <span data-ttu-id="b85a4-111">Lista zarejestrowanych WPW dla komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="b85a4-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="b85a4-112">Lista zarejestrowanych ASN.</span><span class="sxs-lookup"><span data-stu-id="b85a4-112">Lists registered asn.</span></span>

### <span data-ttu-id="b85a4-113">Pobiera zarejestrowany ASN na potrzeby komunikacji równorzędnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="b85a4-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="b85a4-114">Pobiera zarejestrowany ASN równorzędny.</span><span class="sxs-lookup"><span data-stu-id="b85a4-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="b85a4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b85a4-115">PARAMETERS</span></span>

### <span data-ttu-id="b85a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85a4-116">-DefaultProfile</span></span>
<span data-ttu-id="b85a4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b85a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b85a4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b85a4-118">-InputObject</span></span>
<span data-ttu-id="b85a4-119">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b85a4-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b85a4-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b85a4-120">-Name</span></span>
<span data-ttu-id="b85a4-121">Nazwa zarejestrowanego konta ASN</span><span class="sxs-lookup"><span data-stu-id="b85a4-121">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85a4-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b85a4-122">-PeeringName</span></span>
<span data-ttu-id="b85a4-123">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b85a4-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="b85a4-125">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b85a4-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b85a4-126">-ResourceId</span></span>
<span data-ttu-id="b85a4-127">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="b85a4-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85a4-128">CommonParameters</span></span>
<span data-ttu-id="b85a4-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b85a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85a4-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b85a4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85a4-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b85a4-131">INPUTS</span></span>

### <span data-ttu-id="b85a4-132">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="b85a4-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="b85a4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b85a4-133">System.String</span></span>

## <span data-ttu-id="b85a4-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b85a4-134">OUTPUTS</span></span>

### <span data-ttu-id="b85a4-135">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b85a4-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b85a4-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b85a4-136">NOTES</span></span>

## <span data-ttu-id="b85a4-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b85a4-137">RELATED LINKS</span></span>
