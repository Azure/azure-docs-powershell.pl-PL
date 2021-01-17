---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490677"
---
# <span data-ttu-id="e2098-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="e2098-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="e2098-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2098-102">SYNOPSIS</span></span>
<span data-ttu-id="e2098-103">Pobiera informacje o klastrze RedisEnterprise i skojarzonej z nim bazie danych.</span><span class="sxs-lookup"><span data-stu-id="e2098-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="e2098-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2098-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e2098-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2098-105">DESCRIPTION</span></span>
<span data-ttu-id="e2098-106">Pobiera informacje o klastrze RedisEnterprise i skojarzonej z nim bazie danych.</span><span class="sxs-lookup"><span data-stu-id="e2098-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="e2098-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2098-107">EXAMPLES</span></span>

### <span data-ttu-id="e2098-108">Przykład 1: uzyskiwanie Redis pamięci podręcznej przedsiębiorstwa według nazwy</span><span class="sxs-lookup"><span data-stu-id="e2098-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="e2098-109">To polecenie pobiera pamięć podręczną Redis Enterprise.</span><span class="sxs-lookup"><span data-stu-id="e2098-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="e2098-110">Przykład 2: pobieranie wszystkich Redis pamięci podręcznej przedsiębiorstwa w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e2098-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="e2098-111">To polecenie pobiera każdą Redisą pamięć podręczną przedsiębiorstwa w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2098-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="e2098-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2098-112">PARAMETERS</span></span>

### <span data-ttu-id="e2098-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="e2098-113">-ClusterName</span></span>
<span data-ttu-id="e2098-114">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="e2098-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="e2098-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2098-115">-DefaultProfile</span></span>
<span data-ttu-id="e2098-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2098-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2098-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2098-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2098-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2098-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2098-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e2098-119">-SubscriptionId</span></span>
<span data-ttu-id="e2098-120">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e2098-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2098-121">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="e2098-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e2098-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2098-122">CommonParameters</span></span>
<span data-ttu-id="e2098-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2098-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2098-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2098-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2098-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2098-125">INPUTS</span></span>

## <span data-ttu-id="e2098-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2098-126">OUTPUTS</span></span>

### <span data-ttu-id="e2098-127">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="e2098-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="e2098-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2098-128">NOTES</span></span>

<span data-ttu-id="e2098-129">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e2098-129">ALIASES</span></span>

## <span data-ttu-id="e2098-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2098-130">RELATED LINKS</span></span>

