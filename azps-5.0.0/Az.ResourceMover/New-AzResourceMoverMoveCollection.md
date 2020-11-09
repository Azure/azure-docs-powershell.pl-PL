---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317652"
---
# <span data-ttu-id="47460-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="47460-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="47460-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47460-102">SYNOPSIS</span></span>
<span data-ttu-id="47460-103">Tworzy lub aktualizuje kolekcję Przenieś.</span><span class="sxs-lookup"><span data-stu-id="47460-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="47460-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47460-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47460-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47460-105">DESCRIPTION</span></span>
<span data-ttu-id="47460-106">Tworzy lub aktualizuje kolekcję Przenieś.</span><span class="sxs-lookup"><span data-stu-id="47460-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="47460-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47460-107">EXAMPLES</span></span>

### <span data-ttu-id="47460-108">Przykład 1. Tworzenie nowej kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="47460-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="47460-109">Tworzenie nowej kolekcji Przenieś w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="47460-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="47460-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47460-110">PARAMETERS</span></span>

### <span data-ttu-id="47460-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47460-111">-DefaultProfile</span></span>
<span data-ttu-id="47460-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47460-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47460-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="47460-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="47460-114">Pobiera lub ustawia identyfikator podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="47460-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="47460-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="47460-115">-IdentityTenantId</span></span>
<span data-ttu-id="47460-116">Pobiera lub ustawia identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="47460-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="47460-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="47460-117">-IdentityType</span></span>
<span data-ttu-id="47460-118">Typ tożsamości używanej przez usługę przenoszenia regionów.</span><span class="sxs-lookup"><span data-stu-id="47460-118">The type of identity used for the region move service.</span></span>

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

### <span data-ttu-id="47460-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="47460-119">-Location</span></span>
<span data-ttu-id="47460-120">Lokalizacja geograficzna, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="47460-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="47460-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47460-121">-Name</span></span>
<span data-ttu-id="47460-122">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="47460-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="47460-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47460-123">-ResourceGroupName</span></span>
<span data-ttu-id="47460-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47460-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="47460-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="47460-125">-SourceRegion</span></span>
<span data-ttu-id="47460-126">Pobiera lub ustawia region źródłowy.</span><span class="sxs-lookup"><span data-stu-id="47460-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="47460-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="47460-127">-SubscriptionId</span></span>
<span data-ttu-id="47460-128">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="47460-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="47460-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="47460-129">-Tag</span></span>
<span data-ttu-id="47460-130">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="47460-130">Resource tags.</span></span>

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

### <span data-ttu-id="47460-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="47460-131">-TargetRegion</span></span>
<span data-ttu-id="47460-132">Pobiera lub ustawia region docelowy.</span><span class="sxs-lookup"><span data-stu-id="47460-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="47460-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47460-133">-Confirm</span></span>
<span data-ttu-id="47460-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47460-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47460-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47460-135">-WhatIf</span></span>
<span data-ttu-id="47460-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47460-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47460-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47460-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47460-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47460-138">CommonParameters</span></span>
<span data-ttu-id="47460-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47460-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47460-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47460-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47460-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47460-141">INPUTS</span></span>

## <span data-ttu-id="47460-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47460-142">OUTPUTS</span></span>

### <span data-ttu-id="47460-143">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="47460-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="47460-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47460-144">NOTES</span></span>

<span data-ttu-id="47460-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="47460-145">ALIASES</span></span>

## <span data-ttu-id="47460-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47460-146">RELATED LINKS</span></span>

