---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384750"
---
# <span data-ttu-id="baa08-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="baa08-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="baa08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="baa08-102">SYNOPSIS</span></span>
<span data-ttu-id="baa08-103">Tworzenie zarejestrowanych prefiksów dla obiektów równorzędnych.</span><span class="sxs-lookup"><span data-stu-id="baa08-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="baa08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="baa08-104">SYNTAX</span></span>

### <span data-ttu-id="baa08-105">ByResourceGroupAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="baa08-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa08-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="baa08-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa08-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="baa08-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baa08-108">Opis</span><span class="sxs-lookup"><span data-stu-id="baa08-108">DESCRIPTION</span></span>
<span data-ttu-id="baa08-109">Tworzenie zarejestrowanych prefiksów dla obiektów równorzędnych.</span><span class="sxs-lookup"><span data-stu-id="baa08-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="baa08-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="baa08-110">EXAMPLES</span></span>

### <span data-ttu-id="baa08-111">Uzyskiwanie komunikacji równorzędnej i tworzenie zarejestrowanego prefiksu</span><span class="sxs-lookup"><span data-stu-id="baa08-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="baa08-112">Pobierz komunikację z innymi użytkownikami, w przypadku których chcesz dodać zarejestrowany prefiks.</span><span class="sxs-lookup"><span data-stu-id="baa08-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="baa08-113">Następnie Przekaż to unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="baa08-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="baa08-114">Tworzenie zarejestrowanego konta ASN za pomocą resourceId równorzędnego</span><span class="sxs-lookup"><span data-stu-id="baa08-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="baa08-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="baa08-115">PARAMETERS</span></span>

### <span data-ttu-id="baa08-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baa08-116">-AsJob</span></span>
<span data-ttu-id="baa08-117">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="baa08-117">Run in the background.</span></span>

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

### <span data-ttu-id="baa08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa08-118">-DefaultProfile</span></span>
<span data-ttu-id="baa08-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="baa08-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baa08-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="baa08-120">-InputObject</span></span>
<span data-ttu-id="baa08-121">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="baa08-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="baa08-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="baa08-122">-Name</span></span>
<span data-ttu-id="baa08-123">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="baa08-123">The name of prefix.</span></span>

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

### <span data-ttu-id="baa08-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="baa08-124">-PeeringName</span></span>
<span data-ttu-id="baa08-125">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="baa08-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="baa08-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="baa08-126">-Prefix</span></span>
<span data-ttu-id="baa08-127">Prefiks IPv4 sesji</span><span class="sxs-lookup"><span data-stu-id="baa08-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="baa08-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa08-128">-ResourceGroupName</span></span>
<span data-ttu-id="baa08-129">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="baa08-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="baa08-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="baa08-130">-ResourceId</span></span>
<span data-ttu-id="baa08-131">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="baa08-131">The resource id string name.</span></span>

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

### <span data-ttu-id="baa08-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="baa08-132">-Confirm</span></span>
<span data-ttu-id="baa08-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baa08-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baa08-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baa08-134">-WhatIf</span></span>
<span data-ttu-id="baa08-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baa08-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baa08-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="baa08-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baa08-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa08-137">CommonParameters</span></span>
<span data-ttu-id="baa08-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baa08-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa08-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baa08-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa08-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baa08-140">INPUTS</span></span>

### <span data-ttu-id="baa08-141">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="baa08-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="baa08-142">System. String</span><span class="sxs-lookup"><span data-stu-id="baa08-142">System.String</span></span>

## <span data-ttu-id="baa08-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="baa08-143">OUTPUTS</span></span>

### <span data-ttu-id="baa08-144">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="baa08-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="baa08-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="baa08-145">NOTES</span></span>

## <span data-ttu-id="baa08-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="baa08-146">RELATED LINKS</span></span>
