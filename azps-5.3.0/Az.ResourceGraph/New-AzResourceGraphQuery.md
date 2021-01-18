---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: 853c06c6179f25065efba71b2d148c36e2d74ef4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498473"
---
# <span data-ttu-id="79261-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="79261-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="79261-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79261-102">SYNOPSIS</span></span>
<span data-ttu-id="79261-103">Tworzenie nowej kwerendy wykresu.</span><span class="sxs-lookup"><span data-stu-id="79261-103">Create a new graph query.</span></span>

## <span data-ttu-id="79261-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79261-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79261-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79261-105">DESCRIPTION</span></span>
<span data-ttu-id="79261-106">Tworzenie nowej kwerendy wykresu.</span><span class="sxs-lookup"><span data-stu-id="79261-106">Create a new graph query.</span></span>

## <span data-ttu-id="79261-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79261-107">EXAMPLES</span></span>

### <span data-ttu-id="79261-108">Przykład 1. Tworzenie zapytania dotyczącego wykresu zasobu według parametru zapytania</span><span class="sxs-lookup"><span data-stu-id="79261-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="79261-109">To polecenie tworzy zapytanie wykresu zasobu według parametru zapytania.</span><span class="sxs-lookup"><span data-stu-id="79261-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="79261-110">Przykład 2: Tworzenie zapytania dotyczącego wykresu zasobów według parametru pliku</span><span class="sxs-lookup"><span data-stu-id="79261-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="79261-111">To polecenie tworzy zapytanie wykresu zasobu według parametru pliku.</span><span class="sxs-lookup"><span data-stu-id="79261-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="79261-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79261-112">PARAMETERS</span></span>

### <span data-ttu-id="79261-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79261-113">-DefaultProfile</span></span>
<span data-ttu-id="79261-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79261-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79261-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="79261-115">-Description</span></span>
<span data-ttu-id="79261-116">Opis zapytania dotyczącego wykresu.</span><span class="sxs-lookup"><span data-stu-id="79261-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="79261-117">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="79261-117">-File</span></span>
<span data-ttu-id="79261-118">Zawartość pliku zostanie przekazana do parametru zapytania.</span><span class="sxs-lookup"><span data-stu-id="79261-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="79261-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="79261-119">-Location</span></span>
<span data-ttu-id="79261-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="79261-120">The location of the resource</span></span>

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

### <span data-ttu-id="79261-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79261-121">-Name</span></span>
<span data-ttu-id="79261-122">Nazwa zasobu kwerendy wykresu.</span><span class="sxs-lookup"><span data-stu-id="79261-122">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="79261-123">-Query</span><span class="sxs-lookup"><span data-stu-id="79261-123">-Query</span></span>
<span data-ttu-id="79261-124">Kwerenda Keyword, która będzie wykresem.</span><span class="sxs-lookup"><span data-stu-id="79261-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="79261-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79261-125">-ResourceGroupName</span></span>
<span data-ttu-id="79261-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79261-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="79261-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="79261-127">-SubscriptionId</span></span>
<span data-ttu-id="79261-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79261-128">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="79261-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="79261-129">-Tag</span></span>
<span data-ttu-id="79261-130">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="79261-130">Resource tags</span></span>

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

### <span data-ttu-id="79261-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79261-131">-Confirm</span></span>
<span data-ttu-id="79261-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79261-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79261-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79261-133">-WhatIf</span></span>
<span data-ttu-id="79261-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79261-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79261-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79261-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79261-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79261-136">CommonParameters</span></span>
<span data-ttu-id="79261-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79261-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79261-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79261-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79261-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79261-139">INPUTS</span></span>

### <span data-ttu-id="79261-140">Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="79261-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="79261-141">Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="79261-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="79261-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79261-142">OUTPUTS</span></span>

### <span data-ttu-id="79261-143">Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="79261-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="79261-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79261-144">NOTES</span></span>

<span data-ttu-id="79261-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="79261-145">ALIASES</span></span>

## <span data-ttu-id="79261-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79261-146">RELATED LINKS</span></span>

