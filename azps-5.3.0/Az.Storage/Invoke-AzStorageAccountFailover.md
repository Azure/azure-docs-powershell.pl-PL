---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376224"
---
# <span data-ttu-id="0aa74-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="0aa74-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="0aa74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0aa74-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa74-103">Wywołuje tryb failover konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0aa74-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="0aa74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0aa74-104">SYNTAX</span></span>

### <span data-ttu-id="0aa74-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0aa74-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa74-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="0aa74-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa74-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0aa74-107">DESCRIPTION</span></span>
<span data-ttu-id="0aa74-108">Wywołuje tryb failover konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0aa74-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="0aa74-109">Żądanie przejęcia awaryjnego można wyzwolić dla konta magazynu w przypadku problemów z dostępnością.</span><span class="sxs-lookup"><span data-stu-id="0aa74-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="0aa74-110">Przejście do trybu failover jest wykonywane z podstawowego klastra konta magazynu w klastrze pomocniczym dla kont RA-GRS.</span><span class="sxs-lookup"><span data-stu-id="0aa74-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="0aa74-111">Klaster pomocniczy stanie się podstawowym po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="0aa74-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="0aa74-112">Przed rozpoczęciem pracy awaryjnej zapoznaj się z następującym wpływem na konto magazynu: 1,1.</span><span class="sxs-lookup"><span data-stu-id="0aa74-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="0aa74-113">Sprawdź czas ostatniej synchronizacji, korzystając z funkcji Pobierz statystykę usługi BLOB (Aby uzyskać statystykę https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) dotyczącą usługi tabeli ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) i uzyskać statystykę usługi kolejkowania) ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) dla Twojego konta.</span><span class="sxs-lookup"><span data-stu-id="0aa74-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="0aa74-114">W przypadku inicjowania pracy awaryjnej możesz utracić dane, które mogą zostać utracone.</span><span class="sxs-lookup"><span data-stu-id="0aa74-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="0aa74-115">2. po przełączeniu do trybu failover typ konta magazynu zostanie przekonwertowany na lokalnie nadmiarowy magazyn (LRS).</span><span class="sxs-lookup"><span data-stu-id="0aa74-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="0aa74-116">Możesz przekonwertować swoje konto, aby używać magazynu geograficznie nadmiarowego (GRS).</span><span class="sxs-lookup"><span data-stu-id="0aa74-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="0aa74-117">3. po ponownym włączeniu GRS dla konta magazynu firma Microsoft będzie replikować dane do nowego regionu pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="0aa74-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="0aa74-118">Czas replikacji zależy od ilości danych do zreplikowania.</span><span class="sxs-lookup"><span data-stu-id="0aa74-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="0aa74-119">Pamiętaj, że w przypadku ładowania początkowego są dostępne opłaty za przepustowość.</span><span class="sxs-lookup"><span data-stu-id="0aa74-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="0aa74-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="0aa74-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="0aa74-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0aa74-121">EXAMPLES</span></span>

### <span data-ttu-id="0aa74-122">Przykład 1: wywoływanie trybu failover dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="0aa74-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="0aa74-123">To polecenie umożliwia sprawdzenie ostatniej synchronizacji konta magazynu w celu przełączenia jej do trybu failover, a klaster pomocniczy stanie się podstawowym po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="0aa74-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="0aa74-124">Ponieważ praca awaryjna zabiera dużo czasu, zaleca się jej uruchomienie w parametrze wewnętrznej bazy danych with AsJob, a następnie zaczekanie na zakończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="0aa74-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="0aa74-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0aa74-125">PARAMETERS</span></span>

### <span data-ttu-id="0aa74-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0aa74-126">-AsJob</span></span>
<span data-ttu-id="0aa74-127">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0aa74-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0aa74-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa74-128">-DefaultProfile</span></span>
<span data-ttu-id="0aa74-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa74-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa74-130">-Force</span><span class="sxs-lookup"><span data-stu-id="0aa74-130">-Force</span></span>
<span data-ttu-id="0aa74-131">Wymuś przejęcie konta w trybie failover</span><span class="sxs-lookup"><span data-stu-id="0aa74-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="0aa74-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0aa74-132">-InputObject</span></span>
<span data-ttu-id="0aa74-133">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="0aa74-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa74-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0aa74-134">-Name</span></span>
<span data-ttu-id="0aa74-135">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0aa74-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa74-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa74-136">-ResourceGroupName</span></span>
<span data-ttu-id="0aa74-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0aa74-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa74-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0aa74-138">-Confirm</span></span>
<span data-ttu-id="0aa74-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aa74-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aa74-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa74-140">-WhatIf</span></span>
<span data-ttu-id="0aa74-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aa74-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa74-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0aa74-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aa74-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa74-143">CommonParameters</span></span>
<span data-ttu-id="0aa74-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aa74-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa74-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aa74-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa74-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0aa74-146">INPUTS</span></span>

### <span data-ttu-id="0aa74-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0aa74-147">System.String</span></span>

## <span data-ttu-id="0aa74-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0aa74-148">OUTPUTS</span></span>

### <span data-ttu-id="0aa74-149">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0aa74-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0aa74-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0aa74-150">NOTES</span></span>

## <span data-ttu-id="0aa74-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0aa74-151">RELATED LINKS</span></span>
