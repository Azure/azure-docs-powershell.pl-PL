---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 317614d67138b185dc58334d398bb368fc85911e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999889"
---
# <span data-ttu-id="f493c-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f493c-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="f493c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f493c-102">SYNOPSIS</span></span>
<span data-ttu-id="f493c-103">Tworzy lub aktualizuje kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f493c-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="f493c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f493c-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f493c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f493c-105">DESCRIPTION</span></span>
<span data-ttu-id="f493c-106">Tworzy lub aktualizuje kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f493c-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="f493c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f493c-107">EXAMPLES</span></span>

### <span data-ttu-id="f493c-108">Przykład 1. Tworzenie nowej kolekcji Przenieś.</span><span class="sxs-lookup"><span data-stu-id="f493c-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name "PS-centralus-westcentralus-demoRMS"  -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceRegion "centralus" -TargetRegion "westcentralus" -Location "centraluseuap" -IdentityType "SystemAssigned"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"0200d92f-0000-3300-0000-6021e9ec0000" centraluseuap PS-centralus-westcentralus-demoRMs Microsoft.Migrate/moveCollections
```

<span data-ttu-id="f493c-109">Utwórz nową kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f493c-109">Create a new Move Collection.</span></span>

## <span data-ttu-id="f493c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f493c-110">PARAMETERS</span></span>

### <span data-ttu-id="f493c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f493c-111">-DefaultProfile</span></span>
<span data-ttu-id="f493c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f493c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="f493c-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="f493c-114">Pobiera lub ustawia identyfikator dyrektora.</span><span class="sxs-lookup"><span data-stu-id="f493c-114">Gets or sets the principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="f493c-115">-IdentityTenantId</span></span>
<span data-ttu-id="f493c-116">Pobiera lub ustawia identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="f493c-116">Gets or sets the tenant id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f493c-117">-IdentityType</span></span>
<span data-ttu-id="f493c-118">Typ tożsamości używany dla usługi przenoszenia zasobów.</span><span class="sxs-lookup"><span data-stu-id="f493c-118">The type of identity used for the resource mover service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f493c-119">-Location</span></span>
<span data-ttu-id="f493c-120">Lokalizacja geograficzna, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="f493c-120">The geo-location where the resource lives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f493c-121">-Name</span></span>
<span data-ttu-id="f493c-122">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f493c-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f493c-123">-ResourceGroupName</span></span>
<span data-ttu-id="f493c-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f493c-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f493c-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="f493c-125">-SourceRegion</span></span>
<span data-ttu-id="f493c-126">Pobiera lub ustawia region źródłowy.</span><span class="sxs-lookup"><span data-stu-id="f493c-126">Gets or sets the source region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f493c-127">-SubscriptionId</span></span>
<span data-ttu-id="f493c-128">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f493c-128">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="f493c-129">-Tag</span></span>
<span data-ttu-id="f493c-130">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="f493c-130">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-131">- TargetRegion</span><span class="sxs-lookup"><span data-stu-id="f493c-131">-TargetRegion</span></span>
<span data-ttu-id="f493c-132">Pobiera lub ustawia region docelowy.</span><span class="sxs-lookup"><span data-stu-id="f493c-132">Gets or sets the target region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f493c-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f493c-133">-Confirm</span></span>
<span data-ttu-id="f493c-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f493c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f493c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f493c-135">-WhatIf</span></span>
<span data-ttu-id="f493c-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f493c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f493c-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f493c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f493c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f493c-138">CommonParameters</span></span>
<span data-ttu-id="f493c-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f493c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f493c-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f493c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f493c-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f493c-141">INPUTS</span></span>

## <span data-ttu-id="f493c-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f493c-142">OUTPUTS</span></span>

### <span data-ttu-id="f493c-143">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f493c-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="f493c-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f493c-144">NOTES</span></span>

<span data-ttu-id="f493c-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f493c-145">ALIASES</span></span>

## <span data-ttu-id="f493c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f493c-146">RELATED LINKS</span></span>

