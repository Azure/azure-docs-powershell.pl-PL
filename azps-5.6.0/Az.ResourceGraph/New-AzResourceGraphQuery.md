---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: c20e7c63fac01459d3df9d417b0fcec6aed83d36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000138"
---
# <span data-ttu-id="56fc5-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="56fc5-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="56fc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="56fc5-103">Utwórz nowe zapytanie wykresu.</span><span class="sxs-lookup"><span data-stu-id="56fc5-103">Create a new graph query.</span></span>

## <span data-ttu-id="56fc5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56fc5-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56fc5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="56fc5-105">DESCRIPTION</span></span>
<span data-ttu-id="56fc5-106">Utwórz nowe zapytanie wykresu.</span><span class="sxs-lookup"><span data-stu-id="56fc5-106">Create a new graph query.</span></span>

## <span data-ttu-id="56fc5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56fc5-107">EXAMPLES</span></span>

### <span data-ttu-id="56fc5-108">Przykład 1. Tworzenie zapytania wykresu zasobu według parametru zapytania</span><span class="sxs-lookup"><span data-stu-id="56fc5-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="56fc5-109">To polecenie tworzy zapytanie wykresu zasobów według parametru zapytania.</span><span class="sxs-lookup"><span data-stu-id="56fc5-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="56fc5-110">Przykład 2. Tworzenie zapytania wykresu zasobu według parametru pliku</span><span class="sxs-lookup"><span data-stu-id="56fc5-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="56fc5-111">To polecenie tworzy zapytanie wykresu zasobów według parametru pliku.</span><span class="sxs-lookup"><span data-stu-id="56fc5-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="56fc5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56fc5-112">PARAMETERS</span></span>

### <span data-ttu-id="56fc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fc5-113">-DefaultProfile</span></span>
<span data-ttu-id="56fc5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56fc5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56fc5-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="56fc5-115">-Description</span></span>
<span data-ttu-id="56fc5-116">Opis zapytania wykresu.</span><span class="sxs-lookup"><span data-stu-id="56fc5-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="56fc5-117">— Plik</span><span class="sxs-lookup"><span data-stu-id="56fc5-117">-File</span></span>
<span data-ttu-id="56fc5-118">Zawartość pliku zostanie przekazana do parametru zapytania.</span><span class="sxs-lookup"><span data-stu-id="56fc5-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="56fc5-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="56fc5-119">-Location</span></span>
<span data-ttu-id="56fc5-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="56fc5-120">The location of the resource</span></span>

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

### <span data-ttu-id="56fc5-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="56fc5-121">-Name</span></span>
<span data-ttu-id="56fc5-122">Nazwa zasobu zapytanie programu Graph.</span><span class="sxs-lookup"><span data-stu-id="56fc5-122">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="56fc5-123">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="56fc5-123">-Query</span></span>
<span data-ttu-id="56fc5-124">Zapytanie KQL, które będzie grafem.</span><span class="sxs-lookup"><span data-stu-id="56fc5-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="56fc5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56fc5-125">-ResourceGroupName</span></span>
<span data-ttu-id="56fc5-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56fc5-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="56fc5-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56fc5-127">-SubscriptionId</span></span>
<span data-ttu-id="56fc5-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="56fc5-128">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="56fc5-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="56fc5-129">-Tag</span></span>
<span data-ttu-id="56fc5-130">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="56fc5-130">Resource tags</span></span>

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

### <span data-ttu-id="56fc5-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56fc5-131">-Confirm</span></span>
<span data-ttu-id="56fc5-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="56fc5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56fc5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56fc5-133">-WhatIf</span></span>
<span data-ttu-id="56fc5-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56fc5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56fc5-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="56fc5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56fc5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fc5-136">CommonParameters</span></span>
<span data-ttu-id="56fc5-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56fc5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fc5-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56fc5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fc5-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56fc5-139">INPUTS</span></span>

### <span data-ttu-id="56fc5-140">Microsoft.Azure.PowerShell.Cmdlet.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="56fc5-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="56fc5-141">Microsoft.Azure.PowerShell.Cmdlet.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="56fc5-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="56fc5-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56fc5-142">OUTPUTS</span></span>

### <span data-ttu-id="56fc5-143">Microsoft.Azure.PowerShell.Cmdlet.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="56fc5-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="56fc5-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56fc5-144">NOTES</span></span>

<span data-ttu-id="56fc5-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="56fc5-145">ALIASES</span></span>

## <span data-ttu-id="56fc5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56fc5-146">RELATED LINKS</span></span>

