---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223256"
---
# <span data-ttu-id="c91a5-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="c91a5-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="c91a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c91a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c91a5-103">Tworzenie zarejestrowanych prefiksów dla obiektów równorzędnych.</span><span class="sxs-lookup"><span data-stu-id="c91a5-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="c91a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c91a5-104">SYNTAX</span></span>

### <span data-ttu-id="c91a5-105">ByResourceGroupAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c91a5-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c91a5-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="c91a5-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c91a5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c91a5-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c91a5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c91a5-108">DESCRIPTION</span></span>
<span data-ttu-id="c91a5-109">Tworzenie zarejestrowanych prefiksów dla obiektów równorzędnych.</span><span class="sxs-lookup"><span data-stu-id="c91a5-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="c91a5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c91a5-110">EXAMPLES</span></span>

### <span data-ttu-id="c91a5-111">Uzyskiwanie komunikacji równorzędnej i tworzenie zarejestrowanego prefiksu</span><span class="sxs-lookup"><span data-stu-id="c91a5-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="c91a5-112">Pobierz komunikację z innymi użytkownikami, w przypadku których chcesz dodać zarejestrowany prefiks.</span><span class="sxs-lookup"><span data-stu-id="c91a5-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="c91a5-113">Następnie Przekaż to unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="c91a5-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="c91a5-114">Tworzenie zarejestrowanego konta ASN za pomocą resourceId równorzędnego</span><span class="sxs-lookup"><span data-stu-id="c91a5-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="c91a5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c91a5-115">PARAMETERS</span></span>

### <span data-ttu-id="c91a5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c91a5-116">-AsJob</span></span>
<span data-ttu-id="c91a5-117">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="c91a5-117">Run in the background.</span></span>

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

### <span data-ttu-id="c91a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c91a5-118">-DefaultProfile</span></span>
<span data-ttu-id="c91a5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c91a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c91a5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c91a5-120">-InputObject</span></span>
<span data-ttu-id="c91a5-121">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c91a5-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="c91a5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c91a5-122">-Name</span></span>
<span data-ttu-id="c91a5-123">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="c91a5-123">The name of prefix.</span></span>

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

### <span data-ttu-id="c91a5-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="c91a5-124">-PeeringName</span></span>
<span data-ttu-id="c91a5-125">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="c91a5-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c91a5-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="c91a5-126">-Prefix</span></span>
<span data-ttu-id="c91a5-127">Prefiks IPv4 sesji</span><span class="sxs-lookup"><span data-stu-id="c91a5-127">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c91a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c91a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="c91a5-129">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c91a5-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="c91a5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c91a5-130">-ResourceId</span></span>
<span data-ttu-id="c91a5-131">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="c91a5-131">The resource id string name.</span></span>

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

### <span data-ttu-id="c91a5-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c91a5-132">-Confirm</span></span>
<span data-ttu-id="c91a5-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c91a5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c91a5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c91a5-134">-WhatIf</span></span>
<span data-ttu-id="c91a5-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c91a5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c91a5-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c91a5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c91a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c91a5-137">CommonParameters</span></span>
<span data-ttu-id="c91a5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c91a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c91a5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c91a5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c91a5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c91a5-140">INPUTS</span></span>

### <span data-ttu-id="c91a5-141">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="c91a5-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="c91a5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c91a5-142">System.String</span></span>

## <span data-ttu-id="c91a5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c91a5-143">OUTPUTS</span></span>

### <span data-ttu-id="c91a5-144">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="c91a5-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="c91a5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c91a5-145">NOTES</span></span>

## <span data-ttu-id="c91a5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c91a5-146">RELATED LINKS</span></span>
