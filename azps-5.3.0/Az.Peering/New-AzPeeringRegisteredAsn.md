---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384755"
---
# <span data-ttu-id="769be-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="769be-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="769be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="769be-102">SYNOPSIS</span></span>
<span data-ttu-id="769be-103">Tworzenie zarejestrowanego konta ASN dla komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="769be-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="769be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="769be-104">SYNTAX</span></span>

### <span data-ttu-id="769be-105">ByResourceGroupAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="769be-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="769be-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="769be-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="769be-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="769be-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="769be-108">Opis</span><span class="sxs-lookup"><span data-stu-id="769be-108">DESCRIPTION</span></span>
<span data-ttu-id="769be-109">Utwórz zarejestrowane zawiadomienie o wysyłce dla obiektów równorzędnych.</span><span class="sxs-lookup"><span data-stu-id="769be-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="769be-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="769be-110">EXAMPLES</span></span>

### <span data-ttu-id="769be-111">Uzyskiwanie komunikacji równorzędnej i tworzenie zarejestrowanego konta ASN</span><span class="sxs-lookup"><span data-stu-id="769be-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="769be-112">Uzyskaj dostęp do sieci równorzędnej, do której chcesz dodać zarejestrowany ASN.</span><span class="sxs-lookup"><span data-stu-id="769be-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="769be-113">Następnie Przekaż to unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="769be-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="769be-114">Tworzenie zarejestrowanego konta ASN za pomocą resourceId równorzędnego</span><span class="sxs-lookup"><span data-stu-id="769be-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="769be-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="769be-115">PARAMETERS</span></span>

### <span data-ttu-id="769be-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="769be-116">-AsJob</span></span>
<span data-ttu-id="769be-117">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="769be-117">Run in the background.</span></span>

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

### <span data-ttu-id="769be-118">-ASN</span><span class="sxs-lookup"><span data-stu-id="769be-118">-Asn</span></span>
<span data-ttu-id="769be-119">Zarejestrowano ASN</span><span class="sxs-lookup"><span data-stu-id="769be-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="769be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769be-120">-DefaultProfile</span></span>
<span data-ttu-id="769be-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="769be-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="769be-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="769be-122">-InputObject</span></span>
<span data-ttu-id="769be-123">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="769be-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="769be-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="769be-124">-Name</span></span>
<span data-ttu-id="769be-125">Zarejestrowano ASN</span><span class="sxs-lookup"><span data-stu-id="769be-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="769be-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="769be-126">-PeeringName</span></span>
<span data-ttu-id="769be-127">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="769be-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="769be-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="769be-128">-ResourceGroupName</span></span>
<span data-ttu-id="769be-129">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="769be-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="769be-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="769be-130">-ResourceId</span></span>
<span data-ttu-id="769be-131">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="769be-131">The resource id string name.</span></span>

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

### <span data-ttu-id="769be-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="769be-132">-Confirm</span></span>
<span data-ttu-id="769be-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="769be-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="769be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="769be-134">-WhatIf</span></span>
<span data-ttu-id="769be-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="769be-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="769be-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="769be-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="769be-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769be-137">CommonParameters</span></span>
<span data-ttu-id="769be-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="769be-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769be-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="769be-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769be-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="769be-140">INPUTS</span></span>

### <span data-ttu-id="769be-141">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="769be-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="769be-142">System. String</span><span class="sxs-lookup"><span data-stu-id="769be-142">System.String</span></span>

## <span data-ttu-id="769be-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="769be-143">OUTPUTS</span></span>

### <span data-ttu-id="769be-144">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="769be-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="769be-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="769be-145">NOTES</span></span>

## <span data-ttu-id="769be-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="769be-146">RELATED LINKS</span></span>
