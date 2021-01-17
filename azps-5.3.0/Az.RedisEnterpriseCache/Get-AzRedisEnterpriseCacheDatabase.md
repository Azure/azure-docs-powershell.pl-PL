---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490678"
---
# <span data-ttu-id="a025e-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="a025e-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="a025e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a025e-102">SYNOPSIS</span></span>
<span data-ttu-id="a025e-103">Pobiera informacje o bazie danych w klastrze programu RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="a025e-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="a025e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a025e-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a025e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a025e-105">DESCRIPTION</span></span>
<span data-ttu-id="a025e-106">Pobiera informacje o bazie danych w klastrze programu RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="a025e-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="a025e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a025e-107">EXAMPLES</span></span>

### <span data-ttu-id="a025e-108">Przykład 1: Uzyskaj bazę danych</span><span class="sxs-lookup"><span data-stu-id="a025e-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="a025e-109">To polecenie pobiera bazę danych w pamięci podręcznej Redis Enterprise o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="a025e-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="a025e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a025e-110">PARAMETERS</span></span>

### <span data-ttu-id="a025e-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="a025e-111">-ClusterName</span></span>
<span data-ttu-id="a025e-112">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="a025e-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="a025e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a025e-113">-DefaultProfile</span></span>
<span data-ttu-id="a025e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a025e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a025e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a025e-115">-ResourceGroupName</span></span>
<span data-ttu-id="a025e-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a025e-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="a025e-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a025e-117">-SubscriptionId</span></span>
<span data-ttu-id="a025e-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a025e-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a025e-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a025e-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a025e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a025e-120">CommonParameters</span></span>
<span data-ttu-id="a025e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a025e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a025e-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a025e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a025e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a025e-123">INPUTS</span></span>

## <span data-ttu-id="a025e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a025e-124">OUTPUTS</span></span>

### <span data-ttu-id="a025e-125">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. IDatabase</span><span class="sxs-lookup"><span data-stu-id="a025e-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="a025e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a025e-126">NOTES</span></span>

<span data-ttu-id="a025e-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a025e-127">ALIASES</span></span>

## <span data-ttu-id="a025e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a025e-128">RELATED LINKS</span></span>

