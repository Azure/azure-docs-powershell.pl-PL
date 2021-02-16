---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ab5985a7302834f4f7184a43ac2f5ebf795a3d83
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201962"
---
# <span data-ttu-id="cf797-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="cf797-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="cf797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf797-102">SYNOPSIS</span></span>
<span data-ttu-id="cf797-103">Ponownie generuje klucze dostępu bazy danych RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="cf797-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="cf797-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf797-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf797-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf797-105">DESCRIPTION</span></span>
<span data-ttu-id="cf797-106">Ponownie generuje klucze dostępu bazy danych RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="cf797-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="cf797-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf797-107">EXAMPLES</span></span>

### <span data-ttu-id="cf797-108">Przykład 1. Ponowne generowanie klucza dostępu podstawowego</span><span class="sxs-lookup"><span data-stu-id="cf797-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="cf797-109">To polecenie ponownie generuje podstawowy tajny klucz dostępu używany do uwierzytelniania połączeń z bazą danych pamięci podręcznej Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="cf797-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="cf797-110">Przykład 2. Ponowne generowanie pomocniczego klucza dostępu</span><span class="sxs-lookup"><span data-stu-id="cf797-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="cf797-111">To polecenie ponownie generuje dodatkowy tajny klucz dostępu używany do uwierzytelniania połączeń z bazą danych programu Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="cf797-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="cf797-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf797-112">PARAMETERS</span></span>

### <span data-ttu-id="cf797-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cf797-113">-AsJob</span></span>
<span data-ttu-id="cf797-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="cf797-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf797-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cf797-115">-ClusterName</span></span>
<span data-ttu-id="cf797-116">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="cf797-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="cf797-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf797-117">-DefaultProfile</span></span>
<span data-ttu-id="cf797-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf797-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf797-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="cf797-119">-KeyType</span></span>
<span data-ttu-id="cf797-120">Który klucz dostępu do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="cf797-120">Which access key to regenerate.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.AccessKeyType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf797-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cf797-121">-NoWait</span></span>
<span data-ttu-id="cf797-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="cf797-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf797-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf797-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf797-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf797-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="cf797-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf797-125">-SubscriptionId</span></span>
<span data-ttu-id="cf797-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf797-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf797-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="cf797-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf797-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf797-128">-Confirm</span></span>
<span data-ttu-id="cf797-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf797-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf797-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf797-130">-WhatIf</span></span>
<span data-ttu-id="cf797-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf797-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf797-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cf797-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf797-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf797-133">CommonParameters</span></span>
<span data-ttu-id="cf797-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf797-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf797-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf797-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf797-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf797-136">INPUTS</span></span>

## <span data-ttu-id="cf797-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf797-137">OUTPUTS</span></span>

### <span data-ttu-id="cf797-138">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="cf797-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="cf797-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf797-139">NOTES</span></span>

<span data-ttu-id="cf797-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cf797-140">ALIASES</span></span>

## <span data-ttu-id="cf797-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf797-141">RELATED LINKS</span></span>

