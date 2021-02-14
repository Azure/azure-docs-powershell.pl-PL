---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183779"
---
# <span data-ttu-id="f2d94-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="f2d94-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="f2d94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2d94-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d94-103">Pobiera informacje o bazie danych w klastrze RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="f2d94-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="f2d94-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2d94-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f2d94-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2d94-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d94-106">Pobiera informacje o bazie danych w klastrze RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="f2d94-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="f2d94-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2d94-107">EXAMPLES</span></span>

### <span data-ttu-id="f2d94-108">Przykład 1. Uzyskiwanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="f2d94-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="f2d94-109">To polecenie pobiera bazę danych dla pamięci podręcznej Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="f2d94-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="f2d94-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2d94-110">PARAMETERS</span></span>

### <span data-ttu-id="f2d94-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f2d94-111">-ClusterName</span></span>
<span data-ttu-id="f2d94-112">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="f2d94-112">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d94-113">-DefaultProfile</span></span>
<span data-ttu-id="f2d94-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d94-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2d94-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d94-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2d94-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2d94-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2d94-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2d94-117">-SubscriptionId</span></span>
<span data-ttu-id="f2d94-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d94-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f2d94-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="f2d94-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f2d94-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d94-120">CommonParameters</span></span>
<span data-ttu-id="f2d94-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d94-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d94-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2d94-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d94-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2d94-123">INPUTS</span></span>

## <span data-ttu-id="f2d94-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2d94-124">OUTPUTS</span></span>

### <span data-ttu-id="f2d94-125">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="f2d94-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="f2d94-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2d94-126">NOTES</span></span>

<span data-ttu-id="f2d94-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f2d94-127">ALIASES</span></span>

## <span data-ttu-id="f2d94-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2d94-128">RELATED LINKS</span></span>

