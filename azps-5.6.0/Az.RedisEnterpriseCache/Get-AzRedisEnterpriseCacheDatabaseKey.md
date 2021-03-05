---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ff635c55600c6528ecad537b74a843e2d1da830e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000794"
---
# <span data-ttu-id="d14e5-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="d14e5-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="d14e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d14e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d14e5-103">Pobiera klucze dostępu dla bazy danych RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d14e5-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="d14e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d14e5-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d14e5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d14e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d14e5-106">Pobiera klucze dostępu dla bazy danych RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d14e5-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="d14e5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d14e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d14e5-108">Przykład 1. Uzyskiwanie kluczy dostępu do bazy danych</span><span class="sxs-lookup"><span data-stu-id="d14e5-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="d14e5-109">To polecenie pobiera klucze dostępu tajnego używane do uwierzytelniania połączeń z bazą danych programu Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="d14e5-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="d14e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d14e5-110">PARAMETERS</span></span>

### <span data-ttu-id="d14e5-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d14e5-111">-ClusterName</span></span>
<span data-ttu-id="d14e5-112">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d14e5-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="d14e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14e5-113">-DefaultProfile</span></span>
<span data-ttu-id="d14e5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d14e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d14e5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d14e5-115">-ResourceGroupName</span></span>
<span data-ttu-id="d14e5-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d14e5-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="d14e5-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d14e5-117">-SubscriptionId</span></span>
<span data-ttu-id="d14e5-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d14e5-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d14e5-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d14e5-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d14e5-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d14e5-120">-Confirm</span></span>
<span data-ttu-id="d14e5-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d14e5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d14e5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d14e5-122">-WhatIf</span></span>
<span data-ttu-id="d14e5-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d14e5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d14e5-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d14e5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d14e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14e5-125">CommonParameters</span></span>
<span data-ttu-id="d14e5-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d14e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14e5-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d14e5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14e5-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d14e5-128">INPUTS</span></span>

## <span data-ttu-id="d14e5-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d14e5-129">OUTPUTS</span></span>

### <span data-ttu-id="d14e5-130">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d14e5-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="d14e5-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d14e5-131">NOTES</span></span>

<span data-ttu-id="d14e5-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d14e5-132">ALIASES</span></span>

## <span data-ttu-id="d14e5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d14e5-133">RELATED LINKS</span></span>

