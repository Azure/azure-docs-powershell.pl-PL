---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504297"
---
# <span data-ttu-id="61eb7-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="61eb7-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="61eb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="61eb7-103">Pobiera lub wyświetla zarejestrowany prefiks dla komunikacji.</span><span class="sxs-lookup"><span data-stu-id="61eb7-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="61eb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61eb7-104">SYNTAX</span></span>

### <span data-ttu-id="61eb7-105">ByResourceGroupAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="61eb7-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61eb7-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="61eb7-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61eb7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="61eb7-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61eb7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="61eb7-108">DESCRIPTION</span></span>
<span data-ttu-id="61eb7-109">Pobiera lub wyświetla zarejestrowany prefiks dla komunikacji.</span><span class="sxs-lookup"><span data-stu-id="61eb7-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="61eb7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61eb7-110">EXAMPLES</span></span>

### <span data-ttu-id="61eb7-111">Lista zarejestrowanych WPW dla komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="61eb7-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="61eb7-112">Lista zarejestrowanych ASN.</span><span class="sxs-lookup"><span data-stu-id="61eb7-112">Lists registered asn.</span></span>

### <span data-ttu-id="61eb7-113">Pobiera zarejestrowany ASN na potrzeby komunikacji równorzędnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="61eb7-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="61eb7-114">Pobiera zarejestrowany ASN równorzędny.</span><span class="sxs-lookup"><span data-stu-id="61eb7-114">Gets registered peering asn.</span></span>

<span data-ttu-id="61eb7-115">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="61eb7-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="61eb7-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61eb7-116">PARAMETERS</span></span>

### <span data-ttu-id="61eb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61eb7-117">-DefaultProfile</span></span>
<span data-ttu-id="61eb7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61eb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61eb7-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="61eb7-119">-InputObject</span></span>
<span data-ttu-id="61eb7-120">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="61eb7-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="61eb7-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61eb7-121">-Name</span></span>
<span data-ttu-id="61eb7-122">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="61eb7-122">The name of prefix.</span></span>

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

### <span data-ttu-id="61eb7-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="61eb7-123">-PeeringName</span></span>
<span data-ttu-id="61eb7-124">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="61eb7-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="61eb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61eb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="61eb7-126">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61eb7-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="61eb7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61eb7-127">-ResourceId</span></span>
<span data-ttu-id="61eb7-128">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="61eb7-128">The resource id string name.</span></span>

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

### <span data-ttu-id="61eb7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61eb7-129">CommonParameters</span></span>
<span data-ttu-id="61eb7-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61eb7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61eb7-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61eb7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61eb7-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61eb7-132">INPUTS</span></span>

### <span data-ttu-id="61eb7-133">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="61eb7-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="61eb7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="61eb7-134">System.String</span></span>

## <span data-ttu-id="61eb7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61eb7-135">OUTPUTS</span></span>

### <span data-ttu-id="61eb7-136">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="61eb7-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="61eb7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61eb7-137">NOTES</span></span>

## <span data-ttu-id="61eb7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61eb7-138">RELATED LINKS</span></span>
