---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 3576cfb8185898ea7bb0fa2052a18b651d1d5cc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000842"
---
# <span data-ttu-id="ef7ae-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="ef7ae-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="ef7ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7ae-103">Eksportuje plik bazy danych z docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="ef7ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ef7ae-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ef7ae-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ef7ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7ae-106">Eksportuje plik bazy danych z docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="ef7ae-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ef7ae-107">EXAMPLES</span></span>

### <span data-ttu-id="ef7ae-108">Przykład 1. Eksportowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="ef7ae-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="ef7ae-109">To polecenie eksportuje bazę danych redis Enterprise Cache o nazwie MyCache do pliku bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="ef7ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef7ae-110">PARAMETERS</span></span>

### <span data-ttu-id="ef7ae-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ef7ae-111">-AsJob</span></span>
<span data-ttu-id="ef7ae-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ef7ae-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ef7ae-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ef7ae-113">-ClusterName</span></span>
<span data-ttu-id="ef7ae-114">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="ef7ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7ae-115">-DefaultProfile</span></span>
<span data-ttu-id="ef7ae-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef7ae-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ef7ae-117">-NoWait</span></span>
<span data-ttu-id="ef7ae-118">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ef7ae-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ef7ae-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef7ae-119">-PassThru</span></span>
<span data-ttu-id="ef7ae-120">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ef7ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef7ae-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef7ae-123">- SasUri</span><span class="sxs-lookup"><span data-stu-id="ef7ae-123">-SasUri</span></span>
<span data-ttu-id="ef7ae-124">Sas Uri dla katalogu docelowego do wyeksportowania do</span><span class="sxs-lookup"><span data-stu-id="ef7ae-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="ef7ae-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef7ae-125">-SubscriptionId</span></span>
<span data-ttu-id="ef7ae-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef7ae-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef7ae-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef7ae-128">-Confirm</span></span>
<span data-ttu-id="ef7ae-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef7ae-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7ae-130">-WhatIf</span></span>
<span data-ttu-id="ef7ae-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef7ae-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef7ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7ae-133">CommonParameters</span></span>
<span data-ttu-id="ef7ae-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7ae-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef7ae-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7ae-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef7ae-136">INPUTS</span></span>

## <span data-ttu-id="ef7ae-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef7ae-137">OUTPUTS</span></span>

### <span data-ttu-id="ef7ae-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef7ae-138">System.Boolean</span></span>

## <span data-ttu-id="ef7ae-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ef7ae-139">NOTES</span></span>

<span data-ttu-id="ef7ae-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ef7ae-140">ALIASES</span></span>

## <span data-ttu-id="ef7ae-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef7ae-141">RELATED LINKS</span></span>

