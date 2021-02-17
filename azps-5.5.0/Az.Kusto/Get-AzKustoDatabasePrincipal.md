---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 8f83b199aae030bc0ff8cb8290bb6b273e0c8cff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185226"
---
# <span data-ttu-id="70957-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="70957-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="70957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70957-102">SYNOPSIS</span></span>
<span data-ttu-id="70957-103">Zwraca listę głównych użytkowników bazy danych danego klastra Kusto i bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70957-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="70957-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="70957-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70957-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="70957-105">DESCRIPTION</span></span>
<span data-ttu-id="70957-106">Zwraca listę głównych użytkowników bazy danych danego klastra Kusto i bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70957-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="70957-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="70957-107">EXAMPLES</span></span>

### <span data-ttu-id="70957-108">Przykład 1. Lista głównych użytkowników bazy danych danego klastra Kusto i bazy danych</span><span class="sxs-lookup"><span data-stu-id="70957-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="70957-109">Powyższe polecenie zwraca listę głównych użytkowników bazy danych danego klastra Kusto i bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70957-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="70957-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70957-110">PARAMETERS</span></span>

### <span data-ttu-id="70957-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="70957-111">-ClusterName</span></span>
<span data-ttu-id="70957-112">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="70957-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="70957-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70957-113">-DatabaseName</span></span>
<span data-ttu-id="70957-114">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="70957-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="70957-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70957-115">-DefaultProfile</span></span>
<span data-ttu-id="70957-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="70957-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70957-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70957-117">-ResourceGroupName</span></span>
<span data-ttu-id="70957-118">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="70957-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="70957-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70957-119">-SubscriptionId</span></span>
<span data-ttu-id="70957-120">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="70957-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="70957-121">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="70957-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="70957-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70957-122">-Confirm</span></span>
<span data-ttu-id="70957-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="70957-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70957-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70957-124">-WhatIf</span></span>
<span data-ttu-id="70957-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70957-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70957-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="70957-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70957-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70957-127">CommonParameters</span></span>
<span data-ttu-id="70957-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70957-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70957-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70957-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70957-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70957-130">INPUTS</span></span>

## <span data-ttu-id="70957-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70957-131">OUTPUTS</span></span>

### <span data-ttu-id="70957-132">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="70957-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="70957-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="70957-133">NOTES</span></span>

<span data-ttu-id="70957-134">ALIASY</span><span class="sxs-lookup"><span data-stu-id="70957-134">ALIASES</span></span>

## <span data-ttu-id="70957-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70957-135">RELATED LINKS</span></span>

