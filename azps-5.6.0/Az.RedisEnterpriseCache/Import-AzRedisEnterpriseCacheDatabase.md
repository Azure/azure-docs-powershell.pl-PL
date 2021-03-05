---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: b7258c552d14a9c7cdeafae5c23908321b0705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000778"
---
# <span data-ttu-id="1947b-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="1947b-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="1947b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1947b-102">SYNOPSIS</span></span>
<span data-ttu-id="1947b-103">Importuje plik bazy danych do docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1947b-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="1947b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1947b-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1947b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1947b-105">DESCRIPTION</span></span>
<span data-ttu-id="1947b-106">Importuje plik bazy danych do docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1947b-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="1947b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1947b-107">EXAMPLES</span></span>

### <span data-ttu-id="1947b-108">Przykład 1. Importowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="1947b-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="1947b-109">To polecenie importuje plik bazy danych do bazy danych programu Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="1947b-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="1947b-110">Przykład 2. Importowanie bazy danych (przy użyciu przykładowej nazwy pliku)</span><span class="sxs-lookup"><span data-stu-id="1947b-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="1947b-111">To polecenie importuje plik bazy danych do bazy danych programu Redis Enterprise Cache o nazwie MyCache.</span><span class="sxs-lookup"><span data-stu-id="1947b-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="1947b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1947b-112">PARAMETERS</span></span>

### <span data-ttu-id="1947b-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1947b-113">-AsJob</span></span>
<span data-ttu-id="1947b-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1947b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1947b-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1947b-115">-ClusterName</span></span>
<span data-ttu-id="1947b-116">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1947b-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="1947b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1947b-117">-DefaultProfile</span></span>
<span data-ttu-id="1947b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1947b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1947b-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1947b-119">-NoWait</span></span>
<span data-ttu-id="1947b-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1947b-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1947b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1947b-121">-PassThru</span></span>
<span data-ttu-id="1947b-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="1947b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1947b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1947b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1947b-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1947b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="1947b-125">- SasUri</span><span class="sxs-lookup"><span data-stu-id="1947b-125">-SasUri</span></span>
<span data-ttu-id="1947b-126">Sas Uri for the target blob to import from</span><span class="sxs-lookup"><span data-stu-id="1947b-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="1947b-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1947b-127">-SubscriptionId</span></span>
<span data-ttu-id="1947b-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1947b-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1947b-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="1947b-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1947b-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1947b-130">-Confirm</span></span>
<span data-ttu-id="1947b-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1947b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1947b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1947b-132">-WhatIf</span></span>
<span data-ttu-id="1947b-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1947b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1947b-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1947b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1947b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1947b-135">CommonParameters</span></span>
<span data-ttu-id="1947b-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1947b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1947b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1947b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1947b-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1947b-138">INPUTS</span></span>

## <span data-ttu-id="1947b-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1947b-139">OUTPUTS</span></span>

### <span data-ttu-id="1947b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1947b-140">System.Boolean</span></span>

## <span data-ttu-id="1947b-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1947b-141">NOTES</span></span>

<span data-ttu-id="1947b-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1947b-142">ALIASES</span></span>

## <span data-ttu-id="1947b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1947b-143">RELATED LINKS</span></span>

