---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490674"
---
# <span data-ttu-id="618c3-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="618c3-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="618c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="618c3-102">SYNOPSIS</span></span>
<span data-ttu-id="618c3-103">Pobiera klucze dostępu do bazy danych programu RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="618c3-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="618c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="618c3-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="618c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="618c3-105">DESCRIPTION</span></span>
<span data-ttu-id="618c3-106">Pobiera klucze dostępu do bazy danych programu RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="618c3-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="618c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="618c3-107">EXAMPLES</span></span>

### <span data-ttu-id="618c3-108">Przykład 1: uzyskiwanie kluczy dostępu do bazy danych</span><span class="sxs-lookup"><span data-stu-id="618c3-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="618c3-109">To polecenie uzyskuje klucze dostępu Secret używane do uwierzytelniania połączeń z bazą danych pamięci podręcznej usługi Redis Enterprise o nazwie moja pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="618c3-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="618c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="618c3-110">PARAMETERS</span></span>

### <span data-ttu-id="618c3-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="618c3-111">-ClusterName</span></span>
<span data-ttu-id="618c3-112">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="618c3-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="618c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618c3-113">-DefaultProfile</span></span>
<span data-ttu-id="618c3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="618c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="618c3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="618c3-115">-ResourceGroupName</span></span>
<span data-ttu-id="618c3-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="618c3-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="618c3-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="618c3-117">-SubscriptionId</span></span>
<span data-ttu-id="618c3-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="618c3-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="618c3-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="618c3-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="618c3-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="618c3-120">-Confirm</span></span>
<span data-ttu-id="618c3-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="618c3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="618c3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="618c3-122">-WhatIf</span></span>
<span data-ttu-id="618c3-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="618c3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="618c3-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="618c3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="618c3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618c3-125">CommonParameters</span></span>
<span data-ttu-id="618c3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="618c3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618c3-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="618c3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618c3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="618c3-128">INPUTS</span></span>

## <span data-ttu-id="618c3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="618c3-129">OUTPUTS</span></span>

### <span data-ttu-id="618c3-130">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="618c3-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="618c3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="618c3-131">NOTES</span></span>

<span data-ttu-id="618c3-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="618c3-132">ALIASES</span></span>

## <span data-ttu-id="618c3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="618c3-133">RELATED LINKS</span></span>

