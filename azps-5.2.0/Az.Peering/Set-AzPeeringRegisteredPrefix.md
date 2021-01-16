---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352153"
---
# <span data-ttu-id="e5e47-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e5e47-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e5e47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5e47-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e47-103">Ustawia lub aktualizuje zarejestrowany prefiks na podstawie nadrzędnego zasobu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="e5e47-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="e5e47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5e47-104">SYNTAX</span></span>

### <span data-ttu-id="e5e47-105">ByResourceGroupAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e5e47-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e47-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5e47-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e47-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e47-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5e47-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e5e47-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e47-109">Umożliwia zaktualizowanie zarejestrowanego prefiksu z poziomu nadrzędnego zasobu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="e5e47-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="e5e47-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5e47-110">EXAMPLES</span></span>

### <span data-ttu-id="e5e47-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5e47-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="e5e47-112">Umożliwia zaktualizowanie prefiksu przez identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e5e47-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="e5e47-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5e47-113">PARAMETERS</span></span>

### <span data-ttu-id="e5e47-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5e47-114">-AsJob</span></span>
<span data-ttu-id="e5e47-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="e5e47-115">Run in the background.</span></span>

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

### <span data-ttu-id="e5e47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e47-116">-DefaultProfile</span></span>
<span data-ttu-id="e5e47-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e47-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5e47-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5e47-118">-InputObject</span></span>
<span data-ttu-id="e5e47-119">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e5e47-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e47-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e5e47-120">-Name</span></span>
<span data-ttu-id="e5e47-121">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="e5e47-121">The name of prefix.</span></span>

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

### <span data-ttu-id="e5e47-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="e5e47-122">-PeeringName</span></span>
<span data-ttu-id="e5e47-123">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e5e47-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e5e47-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="e5e47-124">-Prefix</span></span>
<span data-ttu-id="e5e47-125">Prefiks IPv4 sesji</span><span class="sxs-lookup"><span data-stu-id="e5e47-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="e5e47-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e47-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5e47-127">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e5e47-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e5e47-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e47-128">-ResourceId</span></span>
<span data-ttu-id="e5e47-129">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="e5e47-129">The resource id string name.</span></span>

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

### <span data-ttu-id="e5e47-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5e47-130">-Confirm</span></span>
<span data-ttu-id="e5e47-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5e47-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5e47-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e47-132">-WhatIf</span></span>
<span data-ttu-id="e5e47-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5e47-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5e47-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5e47-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5e47-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e47-135">CommonParameters</span></span>
<span data-ttu-id="e5e47-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e47-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e47-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5e47-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e47-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5e47-138">INPUTS</span></span>

### <span data-ttu-id="e5e47-139">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e5e47-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="e5e47-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e47-140">System.String</span></span>

## <span data-ttu-id="e5e47-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5e47-141">OUTPUTS</span></span>

### <span data-ttu-id="e5e47-142">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e5e47-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e5e47-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5e47-143">NOTES</span></span>

## <span data-ttu-id="e5e47-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5e47-144">RELATED LINKS</span></span>
