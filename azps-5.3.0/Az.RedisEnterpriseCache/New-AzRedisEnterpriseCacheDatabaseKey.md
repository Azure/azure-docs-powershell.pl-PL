---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ab5985a7302834f4f7184a43ac2f5ebf795a3d83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490673"
---
# <span data-ttu-id="ea839-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="ea839-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="ea839-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea839-102">SYNOPSIS</span></span>
<span data-ttu-id="ea839-103">Generuje klucze dostępu bazy danych RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ea839-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="ea839-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea839-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea839-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea839-105">DESCRIPTION</span></span>
<span data-ttu-id="ea839-106">Generuje klucze dostępu bazy danych RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ea839-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="ea839-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea839-107">EXAMPLES</span></span>

### <span data-ttu-id="ea839-108">Przykład 1: ponowne generowanie podstawowego klucza dostępu</span><span class="sxs-lookup"><span data-stu-id="ea839-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="ea839-109">To polecenie generuje podstawowy klucz tajny (Primary Secret Access) służący do uwierzytelniania połączeń z bazą danych pamięci podręcznej usługi Redis Enterprise o nazwie moja pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="ea839-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="ea839-110">Przykład 2: ponowne generowanie pomocniczego klucza dostępu</span><span class="sxs-lookup"><span data-stu-id="ea839-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="ea839-111">To polecenie powoduje wygenerowanie pomocniczego klucza tajnego dostępu do uwierzytelniania połączeń z bazą danych pamięci podręcznej usługi Redis Enterprise o nazwie moja pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="ea839-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="ea839-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea839-112">PARAMETERS</span></span>

### <span data-ttu-id="ea839-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea839-113">-AsJob</span></span>
<span data-ttu-id="ea839-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ea839-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ea839-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="ea839-115">-ClusterName</span></span>
<span data-ttu-id="ea839-116">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ea839-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="ea839-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea839-117">-DefaultProfile</span></span>
<span data-ttu-id="ea839-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea839-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea839-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ea839-119">-KeyType</span></span>
<span data-ttu-id="ea839-120">Kod dostępu do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="ea839-120">Which access key to regenerate.</span></span>

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

### <span data-ttu-id="ea839-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ea839-121">-NoWait</span></span>
<span data-ttu-id="ea839-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ea839-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ea839-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea839-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea839-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea839-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea839-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ea839-125">-SubscriptionId</span></span>
<span data-ttu-id="ea839-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea839-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ea839-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ea839-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ea839-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea839-128">-Confirm</span></span>
<span data-ttu-id="ea839-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea839-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea839-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea839-130">-WhatIf</span></span>
<span data-ttu-id="ea839-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea839-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea839-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea839-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea839-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea839-133">CommonParameters</span></span>
<span data-ttu-id="ea839-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea839-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea839-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea839-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea839-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea839-136">INPUTS</span></span>

## <span data-ttu-id="ea839-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea839-137">OUTPUTS</span></span>

### <span data-ttu-id="ea839-138">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="ea839-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="ea839-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea839-139">NOTES</span></span>

<span data-ttu-id="ea839-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ea839-140">ALIASES</span></span>

## <span data-ttu-id="ea839-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea839-141">RELATED LINKS</span></span>

