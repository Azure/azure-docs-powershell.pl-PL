---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499965"
---
# <span data-ttu-id="c0222-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="c0222-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="c0222-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0222-102">SYNOPSIS</span></span>
<span data-ttu-id="c0222-103">Tworzenie kwerendy o pojedynczej grafie przy użyciu jej ResourceName.</span><span class="sxs-lookup"><span data-stu-id="c0222-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="c0222-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0222-104">SYNTAX</span></span>

### <span data-ttu-id="c0222-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c0222-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0222-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c0222-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c0222-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c0222-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0222-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c0222-108">DESCRIPTION</span></span>
<span data-ttu-id="c0222-109">Tworzenie kwerendy o pojedynczej grafie przy użyciu jej ResourceName.</span><span class="sxs-lookup"><span data-stu-id="c0222-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="c0222-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0222-110">EXAMPLES</span></span>

### <span data-ttu-id="c0222-111">Przykład 1: pobieranie wszystkich kwerend wykresu zasobów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="c0222-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="c0222-112">To polecenie pobiera całą kwerendę dotyczącą wykresu zasobów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0222-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="c0222-113">Przykład 2: pobieranie zapytania dotyczącego wykresu zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="c0222-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="c0222-114">To polecenie pobiera zapytanie wykresu zasobu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="c0222-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="c0222-115">Przykład 2: pobieranie zapytania dotyczącego wykresu zasobów przez objecy</span><span class="sxs-lookup"><span data-stu-id="c0222-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="c0222-116">To polecenie pobiera zapytanie wykresu zasobu według obiektu.</span><span class="sxs-lookup"><span data-stu-id="c0222-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="c0222-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0222-117">PARAMETERS</span></span>

### <span data-ttu-id="c0222-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0222-118">-DefaultProfile</span></span>
<span data-ttu-id="c0222-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0222-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0222-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c0222-120">-InputObject</span></span>
<span data-ttu-id="c0222-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c0222-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0222-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0222-122">-Name</span></span>
<span data-ttu-id="c0222-123">Nazwa zasobu kwerendy wykresu.</span><span class="sxs-lookup"><span data-stu-id="c0222-123">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0222-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0222-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0222-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0222-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0222-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c0222-126">-SubscriptionId</span></span>
<span data-ttu-id="c0222-127">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c0222-127">The Azure subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0222-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0222-128">CommonParameters</span></span>
<span data-ttu-id="c0222-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0222-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0222-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0222-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0222-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0222-131">INPUTS</span></span>

### <span data-ttu-id="c0222-132">Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="c0222-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="c0222-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0222-133">OUTPUTS</span></span>

### <span data-ttu-id="c0222-134">Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="c0222-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="c0222-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0222-135">NOTES</span></span>

<span data-ttu-id="c0222-136">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c0222-136">ALIASES</span></span>

<span data-ttu-id="c0222-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0222-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c0222-138">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c0222-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c0222-139">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c0222-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c0222-140">INPUTobject <IResourceGraphIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="c0222-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c0222-141">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c0222-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c0222-142">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0222-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c0222-143">`[ResourceName <String>]`: Nazwa zasobu kwerendy wykresu.</span><span class="sxs-lookup"><span data-stu-id="c0222-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="c0222-144">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c0222-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="c0222-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0222-145">RELATED LINKS</span></span>

