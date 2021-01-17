---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 6ab4babd894a3c639db6e41e6088653604072c7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378231"
---
# <span data-ttu-id="70986-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="70986-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="70986-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70986-102">SYNOPSIS</span></span>
<span data-ttu-id="70986-103">Importuje plik bazy danych do docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70986-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="70986-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70986-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="70986-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70986-105">DESCRIPTION</span></span>
<span data-ttu-id="70986-106">Importuje plik bazy danych do docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70986-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="70986-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70986-107">EXAMPLES</span></span>

### <span data-ttu-id="70986-108">Przykład 1: Importowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="70986-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="70986-109">To polecenie umożliwia zaimportowanie pliku bazy danych do bazy danych pamięci podręcznej usługi Redis Enterprise o nazwie moja pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="70986-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="70986-110">Przykład 2: Importowanie bazy danych (przy użyciu przykładowej nazwy pliku)</span><span class="sxs-lookup"><span data-stu-id="70986-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="70986-111">To polecenie umożliwia zaimportowanie pliku bazy danych do bazy danych pamięci podręcznej usługi Redis Enterprise o nazwie moja pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="70986-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="70986-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70986-112">PARAMETERS</span></span>

### <span data-ttu-id="70986-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70986-113">-AsJob</span></span>
<span data-ttu-id="70986-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="70986-114">Run the command as a job</span></span>

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

### <span data-ttu-id="70986-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="70986-115">-ClusterName</span></span>
<span data-ttu-id="70986-116">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="70986-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="70986-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70986-117">-DefaultProfile</span></span>
<span data-ttu-id="70986-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70986-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70986-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="70986-119">-NoWait</span></span>
<span data-ttu-id="70986-120">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="70986-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="70986-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70986-121">-PassThru</span></span>
<span data-ttu-id="70986-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="70986-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="70986-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70986-123">-ResourceGroupName</span></span>
<span data-ttu-id="70986-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70986-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="70986-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="70986-125">-SasUri</span></span>
<span data-ttu-id="70986-126">Identyfikator URI SAS dla docelowego obiektu BLOB do zaimportowania</span><span class="sxs-lookup"><span data-stu-id="70986-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="70986-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="70986-127">-SubscriptionId</span></span>
<span data-ttu-id="70986-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="70986-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="70986-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="70986-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="70986-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70986-130">-Confirm</span></span>
<span data-ttu-id="70986-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70986-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70986-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70986-132">-WhatIf</span></span>
<span data-ttu-id="70986-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70986-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70986-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70986-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70986-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70986-135">CommonParameters</span></span>
<span data-ttu-id="70986-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70986-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70986-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70986-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70986-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70986-138">INPUTS</span></span>

## <span data-ttu-id="70986-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70986-139">OUTPUTS</span></span>

### <span data-ttu-id="70986-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70986-140">System.Boolean</span></span>

## <span data-ttu-id="70986-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70986-141">NOTES</span></span>

<span data-ttu-id="70986-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="70986-142">ALIASES</span></span>

## <span data-ttu-id="70986-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70986-143">RELATED LINKS</span></span>

