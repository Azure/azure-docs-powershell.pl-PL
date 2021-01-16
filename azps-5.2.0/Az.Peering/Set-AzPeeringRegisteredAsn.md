---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352165"
---
# <span data-ttu-id="d509b-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="d509b-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="d509b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d509b-102">SYNOPSIS</span></span>
<span data-ttu-id="d509b-103">Ustawia lub aktualizuje zarejestrowany ASN na podstawie nadrzędnego zasobu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="d509b-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="d509b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d509b-104">SYNTAX</span></span>

### <span data-ttu-id="d509b-105">ByResourceGroupAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d509b-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d509b-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d509b-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d509b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d509b-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d509b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d509b-108">DESCRIPTION</span></span>
<span data-ttu-id="d509b-109">Umożliwia zaktualizowanie zarejestrowanego konta ASN z nadrzędnego zasobu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="d509b-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="d509b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d509b-110">EXAMPLES</span></span>

### <span data-ttu-id="d509b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d509b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="d509b-112">Aktualizuje identyfikator ASN według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="d509b-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="d509b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d509b-113">PARAMETERS</span></span>

### <span data-ttu-id="d509b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d509b-114">-AsJob</span></span>
<span data-ttu-id="d509b-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="d509b-115">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d509b-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="d509b-116">-Asn</span></span>
<span data-ttu-id="d509b-117">Zarejestrowano ASN</span><span class="sxs-lookup"><span data-stu-id="d509b-117">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d509b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d509b-118">-DefaultProfile</span></span>
<span data-ttu-id="d509b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d509b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d509b-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d509b-120">-InputObject</span></span>
<span data-ttu-id="d509b-121">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="d509b-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d509b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d509b-122">-Name</span></span>
<span data-ttu-id="d509b-123">Zarejestrowano ASN</span><span class="sxs-lookup"><span data-stu-id="d509b-123">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d509b-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="d509b-124">-PeeringName</span></span>
<span data-ttu-id="d509b-125">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d509b-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="d509b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d509b-126">-ResourceGroupName</span></span>
<span data-ttu-id="d509b-127">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d509b-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="d509b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d509b-128">-ResourceId</span></span>
<span data-ttu-id="d509b-129">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="d509b-129">The resource id string name.</span></span>

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

### <span data-ttu-id="d509b-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d509b-130">-Confirm</span></span>
<span data-ttu-id="d509b-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d509b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d509b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d509b-132">-WhatIf</span></span>
<span data-ttu-id="d509b-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d509b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d509b-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d509b-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d509b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d509b-135">CommonParameters</span></span>
<span data-ttu-id="d509b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d509b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d509b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d509b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d509b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d509b-138">INPUTS</span></span>

### <span data-ttu-id="d509b-139">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="d509b-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="d509b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d509b-140">System.String</span></span>

## <span data-ttu-id="d509b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d509b-141">OUTPUTS</span></span>

### <span data-ttu-id="d509b-142">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="d509b-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="d509b-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d509b-143">NOTES</span></span>

## <span data-ttu-id="d509b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d509b-144">RELATED LINKS</span></span>
