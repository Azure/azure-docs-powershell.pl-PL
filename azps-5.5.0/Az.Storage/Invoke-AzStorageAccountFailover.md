---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198490"
---
# <span data-ttu-id="11bfb-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="11bfb-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="11bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="11bfb-103">Wywoływanie trybu failover konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="11bfb-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="11bfb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11bfb-104">SYNTAX</span></span>

### <span data-ttu-id="11bfb-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="11bfb-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11bfb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="11bfb-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11bfb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="11bfb-107">DESCRIPTION</span></span>
<span data-ttu-id="11bfb-108">Wywoływanie trybu failover konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="11bfb-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="11bfb-109">Żądanie trybu failover może zostać wyzwolone dla konta magazynu w przypadku problemów z dostępnością.</span><span class="sxs-lookup"><span data-stu-id="11bfb-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="11bfb-110">Tryb failover występuje z klasteru podstawowego konta magazynu do klasteru pomocniczego dla kont RA-GRS.</span><span class="sxs-lookup"><span data-stu-id="11bfb-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="11bfb-111">Po trybie failover klaster pomocniczy stanie się klasterem podstawowym.</span><span class="sxs-lookup"><span data-stu-id="11bfb-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="11bfb-112">Przed zainicjowaniem trybu failover należy zrozumieć następujący wpływ na Twoje konto magazynu: 1.1.</span><span class="sxs-lookup"><span data-stu-id="11bfb-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="11bfb-113">Sprawdź czas ostatniej synchronizacji przy użyciu funkcji POBIERZ statystykę usługi obiektów blob ( , GET Table Service Stats ( i https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) GET Queue Service Stats ( dla Twojego https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) konta).</span><span class="sxs-lookup"><span data-stu-id="11bfb-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="11bfb-114">To są dane, które możesz utracić podczas inicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="11bfb-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="11bfb-115">2. Po zakończeniu trybu failover typ konta magazynu zostanie przekonwertowany na lokalnie nadmiarowy magazyn(LRS).</span><span class="sxs-lookup"><span data-stu-id="11bfb-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="11bfb-116">Możesz przekonwertować swoje konto na magazyn nadmiarowy geograficznie (GRS).</span><span class="sxs-lookup"><span data-stu-id="11bfb-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="11bfb-117">3.Po ponownej włączeniu usługi GRS dla konta magazynu firma Microsoft zreplikuje dane do nowego regionu pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="11bfb-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="11bfb-118">Czas replikacji zależy od ilości danych do replikowania.</span><span class="sxs-lookup"><span data-stu-id="11bfb-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="11bfb-119">Pamiętaj, że występują opłaty za przepustowość dla bootstrapa.</span><span class="sxs-lookup"><span data-stu-id="11bfb-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="11bfb-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="11bfb-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="11bfb-121">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11bfb-121">EXAMPLES</span></span>

### <span data-ttu-id="11bfb-122">Przykład 1. Wywoływanie trybu failover konta magazynu</span><span class="sxs-lookup"><span data-stu-id="11bfb-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="11bfb-123">To polecenie sprawdza czas ostatniej synchronizacji konta magazynu, a następnie wywołuje jego tryb failover, a po trybu failover klaster pomocniczy stanie się podstawowy.</span><span class="sxs-lookup"><span data-stu-id="11bfb-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="11bfb-124">Ponieważ trybu failover trwa długo, zaproponuj uruchomienie go w zaplecza z parametrem -Asjob, a następnie poczekaj na ukończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="11bfb-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="11bfb-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11bfb-125">PARAMETERS</span></span>

### <span data-ttu-id="11bfb-126">— AsJob</span><span class="sxs-lookup"><span data-stu-id="11bfb-126">-AsJob</span></span>
<span data-ttu-id="11bfb-127">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="11bfb-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11bfb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11bfb-128">-DefaultProfile</span></span>
<span data-ttu-id="11bfb-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11bfb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11bfb-130">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="11bfb-130">-Force</span></span>
<span data-ttu-id="11bfb-131">Wymuszanie trybu failover konta</span><span class="sxs-lookup"><span data-stu-id="11bfb-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="11bfb-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11bfb-132">-InputObject</span></span>
<span data-ttu-id="11bfb-133">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="11bfb-133">Storage account object</span></span>

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

### <span data-ttu-id="11bfb-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11bfb-134">-Name</span></span>
<span data-ttu-id="11bfb-135">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="11bfb-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="11bfb-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11bfb-136">-ResourceGroupName</span></span>
<span data-ttu-id="11bfb-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11bfb-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="11bfb-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11bfb-138">-Confirm</span></span>
<span data-ttu-id="11bfb-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11bfb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11bfb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11bfb-140">-WhatIf</span></span>
<span data-ttu-id="11bfb-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11bfb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11bfb-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11bfb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11bfb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bfb-143">CommonParameters</span></span>
<span data-ttu-id="11bfb-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11bfb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bfb-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11bfb-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bfb-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11bfb-146">INPUTS</span></span>

### <span data-ttu-id="11bfb-147">System.String</span><span class="sxs-lookup"><span data-stu-id="11bfb-147">System.String</span></span>

## <span data-ttu-id="11bfb-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11bfb-148">OUTPUTS</span></span>

### <span data-ttu-id="11bfb-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11bfb-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="11bfb-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11bfb-150">NOTES</span></span>

## <span data-ttu-id="11bfb-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11bfb-151">RELATED LINKS</span></span>
