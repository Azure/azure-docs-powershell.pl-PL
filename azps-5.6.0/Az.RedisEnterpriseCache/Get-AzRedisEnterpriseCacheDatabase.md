---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9033082093d571fc60cd9b4c495688d11d87aea8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000801"
---
# <span data-ttu-id="fd0c8-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="fd0c8-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="fd0c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd0c8-102">SYNOPSIS</span></span>
<span data-ttu-id="fd0c8-103">Pobiera informacje o bazie danych w klastrze RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="fd0c8-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="fd0c8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd0c8-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fd0c8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd0c8-105">DESCRIPTION</span></span>
<span data-ttu-id="fd0c8-106">Pobiera informacje o bazie danych w klastrze RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="fd0c8-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="fd0c8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd0c8-107">EXAMPLES</span></span>

### <span data-ttu-id="fd0c8-108">Przykład 1. Uzyskiwanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="fd0c8-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="fd0c8-109">To polecenie pobiera bazę danych dla pamięci podręcznej Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="fd0c8-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="fd0c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd0c8-110">PARAMETERS</span></span>

### <span data-ttu-id="fd0c8-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fd0c8-111">-ClusterName</span></span>
<span data-ttu-id="fd0c8-112">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="fd0c8-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="fd0c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd0c8-113">-DefaultProfile</span></span>
<span data-ttu-id="fd0c8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd0c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd0c8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd0c8-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd0c8-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd0c8-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd0c8-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd0c8-117">-SubscriptionId</span></span>
<span data-ttu-id="fd0c8-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fd0c8-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd0c8-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="fd0c8-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fd0c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd0c8-120">CommonParameters</span></span>
<span data-ttu-id="fd0c8-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd0c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd0c8-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd0c8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd0c8-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd0c8-123">INPUTS</span></span>

## <span data-ttu-id="fd0c8-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd0c8-124">OUTPUTS</span></span>

### <span data-ttu-id="fd0c8-125">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="fd0c8-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="fd0c8-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd0c8-126">NOTES</span></span>

<span data-ttu-id="fd0c8-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fd0c8-127">ALIASES</span></span>

## <span data-ttu-id="fd0c8-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd0c8-128">RELATED LINKS</span></span>

