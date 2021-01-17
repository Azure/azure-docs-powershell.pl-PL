---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 8f83b199aae030bc0ff8cb8290bb6b273e0c8cff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490198"
---
# <span data-ttu-id="ee5db-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="ee5db-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="ee5db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee5db-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5db-103">Zwraca listę podmiotów zabezpieczeń bazy danych w danym klastrze usługi Kusto i bazie danych.</span><span class="sxs-lookup"><span data-stu-id="ee5db-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="ee5db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee5db-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee5db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee5db-105">DESCRIPTION</span></span>
<span data-ttu-id="ee5db-106">Zwraca listę podmiotów zabezpieczeń bazy danych w danym klastrze usługi Kusto i bazie danych.</span><span class="sxs-lookup"><span data-stu-id="ee5db-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="ee5db-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee5db-107">EXAMPLES</span></span>

### <span data-ttu-id="ee5db-108">Przykład 1: Lista podmiotów zabezpieczeń bazy danych w danym klastrze Kusto i bazie danych</span><span class="sxs-lookup"><span data-stu-id="ee5db-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="ee5db-109">Powyższe polecenie zwraca listę podmiotów zabezpieczeń bazy danych danej Kusto klastra i bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ee5db-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="ee5db-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee5db-110">PARAMETERS</span></span>

### <span data-ttu-id="ee5db-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="ee5db-111">-ClusterName</span></span>
<span data-ttu-id="ee5db-112">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee5db-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ee5db-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee5db-113">-DatabaseName</span></span>
<span data-ttu-id="ee5db-114">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee5db-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ee5db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5db-115">-DefaultProfile</span></span>
<span data-ttu-id="ee5db-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee5db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee5db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5db-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee5db-118">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee5db-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ee5db-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ee5db-119">-SubscriptionId</span></span>
<span data-ttu-id="ee5db-120">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ee5db-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ee5db-121">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ee5db-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ee5db-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee5db-122">-Confirm</span></span>
<span data-ttu-id="ee5db-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee5db-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee5db-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee5db-124">-WhatIf</span></span>
<span data-ttu-id="ee5db-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee5db-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee5db-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee5db-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee5db-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5db-127">CommonParameters</span></span>
<span data-ttu-id="ee5db-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee5db-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5db-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee5db-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5db-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee5db-130">INPUTS</span></span>

## <span data-ttu-id="ee5db-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee5db-131">OUTPUTS</span></span>

### <span data-ttu-id="ee5db-132">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="ee5db-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="ee5db-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee5db-133">NOTES</span></span>

<span data-ttu-id="ee5db-134">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ee5db-134">ALIASES</span></span>

## <span data-ttu-id="ee5db-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee5db-135">RELATED LINKS</span></span>

