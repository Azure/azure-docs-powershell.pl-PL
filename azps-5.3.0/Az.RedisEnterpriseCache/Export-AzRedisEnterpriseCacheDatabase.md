---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490686"
---
# <span data-ttu-id="a4b0d-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="a4b0d-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="a4b0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b0d-103">Eksportuje plik bazy danych z docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="a4b0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4b0d-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a4b0d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4b0d-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b0d-106">Eksportuje plik bazy danych z docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="a4b0d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4b0d-107">EXAMPLES</span></span>

### <span data-ttu-id="a4b0d-108">Przykład 1: Eksportowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="a4b0d-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="a4b0d-109">To polecenie eksportuje bazę danych pamięci podręcznej usługi Redis Enterprise o nazwie moja pamięć podręczna do pliku bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="a4b0d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4b0d-110">PARAMETERS</span></span>

### <span data-ttu-id="a4b0d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4b0d-111">-AsJob</span></span>
<span data-ttu-id="a4b0d-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="a4b0d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a4b0d-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="a4b0d-113">-ClusterName</span></span>
<span data-ttu-id="a4b0d-114">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="a4b0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b0d-115">-DefaultProfile</span></span>
<span data-ttu-id="a4b0d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4b0d-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a4b0d-117">-NoWait</span></span>
<span data-ttu-id="a4b0d-118">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="a4b0d-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a4b0d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4b0d-119">-PassThru</span></span>
<span data-ttu-id="a4b0d-120">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a4b0d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b0d-121">-ResourceGroupName</span></span>
<span data-ttu-id="a4b0d-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4b0d-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="a4b0d-123">-SasUri</span></span>
<span data-ttu-id="a4b0d-124">Identyfikator URI SAS dla katalogu docelowego do wyeksportowania</span><span class="sxs-lookup"><span data-stu-id="a4b0d-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="a4b0d-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a4b0d-125">-SubscriptionId</span></span>
<span data-ttu-id="a4b0d-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a4b0d-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a4b0d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4b0d-128">-Confirm</span></span>
<span data-ttu-id="a4b0d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4b0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b0d-130">-WhatIf</span></span>
<span data-ttu-id="a4b0d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4b0d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4b0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b0d-133">CommonParameters</span></span>
<span data-ttu-id="a4b0d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b0d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4b0d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b0d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4b0d-136">INPUTS</span></span>

## <span data-ttu-id="a4b0d-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4b0d-137">OUTPUTS</span></span>

### <span data-ttu-id="a4b0d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4b0d-138">System.Boolean</span></span>

## <span data-ttu-id="a4b0d-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4b0d-139">NOTES</span></span>

<span data-ttu-id="a4b0d-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a4b0d-140">ALIASES</span></span>

## <span data-ttu-id="a4b0d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4b0d-141">RELATED LINKS</span></span>

