---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 3380835b4ca8e51c8ba0952ef3ef4bd973fadea3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952465"
---
# <span data-ttu-id="ee3ce-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="ee3ce-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="ee3ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3ce-103">Zwraca listę głównych użytkowników bazy danych danego klastra Kusto i bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="ee3ce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee3ce-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee3ce-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee3ce-105">DESCRIPTION</span></span>
<span data-ttu-id="ee3ce-106">Zwraca listę głównych użytkowników bazy danych danego klastra Kusto i bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="ee3ce-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee3ce-107">EXAMPLES</span></span>

### <span data-ttu-id="ee3ce-108">Przykład 1. Lista głównych podmiotów bazy danych danego klastru i bazy danych Kusto</span><span class="sxs-lookup"><span data-stu-id="ee3ce-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="ee3ce-109">Powyższe polecenie zwraca listę głównych użytkowników bazy danych danego klastra Kusto i bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="ee3ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee3ce-110">PARAMETERS</span></span>

### <span data-ttu-id="ee3ce-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ee3ce-111">-ClusterName</span></span>
<span data-ttu-id="ee3ce-112">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ee3ce-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee3ce-113">-DatabaseName</span></span>
<span data-ttu-id="ee3ce-114">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ee3ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3ce-115">-DefaultProfile</span></span>
<span data-ttu-id="ee3ce-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee3ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee3ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee3ce-118">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ee3ce-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee3ce-119">-SubscriptionId</span></span>
<span data-ttu-id="ee3ce-120">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ee3ce-121">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-121">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee3ce-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee3ce-122">-Confirm</span></span>
<span data-ttu-id="ee3ce-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee3ce-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee3ce-124">-WhatIf</span></span>
<span data-ttu-id="ee3ce-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee3ce-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee3ce-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3ce-127">CommonParameters</span></span>
<span data-ttu-id="ee3ce-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee3ce-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3ce-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee3ce-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3ce-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee3ce-130">INPUTS</span></span>

## <span data-ttu-id="ee3ce-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee3ce-131">OUTPUTS</span></span>

### <span data-ttu-id="ee3ce-132">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="ee3ce-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="ee3ce-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee3ce-133">NOTES</span></span>

<span data-ttu-id="ee3ce-134">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ee3ce-134">ALIASES</span></span>

## <span data-ttu-id="ee3ce-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee3ce-135">RELATED LINKS</span></span>

