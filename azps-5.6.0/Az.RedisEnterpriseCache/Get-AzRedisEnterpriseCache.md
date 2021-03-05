---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: fd127005107586e31798d215d7f54888b26705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000833"
---
# <span data-ttu-id="6baa2-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="6baa2-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="6baa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6baa2-102">SYNOPSIS</span></span>
<span data-ttu-id="6baa2-103">Pobiera informacje o klastrze RedisEnterprise i skojarzonej z nim bazie danych.</span><span class="sxs-lookup"><span data-stu-id="6baa2-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="6baa2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6baa2-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6baa2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6baa2-105">DESCRIPTION</span></span>
<span data-ttu-id="6baa2-106">Pobiera informacje o klastrze RedisEnterprise i skojarzonej z nim bazie danych.</span><span class="sxs-lookup"><span data-stu-id="6baa2-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="6baa2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6baa2-107">EXAMPLES</span></span>

### <span data-ttu-id="6baa2-108">Przykład 1. Uzyskiwanie pamięci podręcznej Redis Enterprise Cache według nazwy</span><span class="sxs-lookup"><span data-stu-id="6baa2-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="6baa2-109">To polecenie pobiera pamięć podręczną Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="6baa2-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="6baa2-110">Przykład 2. Uzyskiwanie każdej pamięci podręcznej Redis Enterprise Cache w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6baa2-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="6baa2-111">To polecenie pobiera wszystkie funkcje Redis Enterprise Cache w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6baa2-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="6baa2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6baa2-112">PARAMETERS</span></span>

### <span data-ttu-id="6baa2-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6baa2-113">-ClusterName</span></span>
<span data-ttu-id="6baa2-114">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="6baa2-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6baa2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6baa2-115">-DefaultProfile</span></span>
<span data-ttu-id="6baa2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6baa2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6baa2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6baa2-117">-ResourceGroupName</span></span>
<span data-ttu-id="6baa2-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6baa2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="6baa2-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6baa2-119">-SubscriptionId</span></span>
<span data-ttu-id="6baa2-120">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6baa2-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6baa2-121">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="6baa2-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6baa2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6baa2-122">CommonParameters</span></span>
<span data-ttu-id="6baa2-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6baa2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6baa2-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6baa2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6baa2-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6baa2-125">INPUTS</span></span>

## <span data-ttu-id="6baa2-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6baa2-126">OUTPUTS</span></span>

### <span data-ttu-id="6baa2-127">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="6baa2-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="6baa2-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6baa2-128">NOTES</span></span>

<span data-ttu-id="6baa2-129">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6baa2-129">ALIASES</span></span>

## <span data-ttu-id="6baa2-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6baa2-130">RELATED LINKS</span></span>

