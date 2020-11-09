---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318211"
---
# <span data-ttu-id="96d5d-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d5d-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="96d5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="96d5d-103">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="96d5d-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="96d5d-104">Spowoduje to włączenie określonej ścieżki na serwerze w celu zsynchronizowania plików z innymi punktami końcowymi w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="96d5d-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="96d5d-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96d5d-105">SYNTAX</span></span>

### <span data-ttu-id="96d5d-106">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96d5d-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96d5d-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96d5d-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96d5d-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="96d5d-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96d5d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="96d5d-109">DESCRIPTION</span></span>
<span data-ttu-id="96d5d-110">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="96d5d-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="96d5d-111">Spowoduje to włączenie określonej ścieżki na serwerze w celu zsynchronizowania plików z innymi punktami końcowymi w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="96d5d-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="96d5d-112">Jeśli w grupie synchronizacja istnieją już pliki w innych punktach końcowych, a nowo dodana lokalizacja również zawiera pliki, proces uzgadniania będzie próbował ustalić, czy pliki są w rzeczywistości te same w tych samych folderach, co w przypadku innych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="96d5d-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="96d5d-113">Obszary nazw będą scalać i uzgadniać, aby zapobiec konfliktom plików.</span><span class="sxs-lookup"><span data-stu-id="96d5d-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="96d5d-114">Jeśli na innych punktach końcowych serwera znajdują się jakieś pliki, często lepiej rozpoczynać się od pustej lokalizacji na tym serwerze, aby pliki z chmury były wyświetlane na serwerze w procesie automatycznym zwanym funkcją szybkiego odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="96d5d-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="96d5d-115">Metadane przestrzeni nazw zostaną najpierw zsynchronizowane, a następnie zostanie pobrany strumień danych każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="96d5d-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="96d5d-116">Jeśli użytkownik lub aplikacja zażądała przeładowania pliku, zostanie on przypomniany przy użyciu priorytetu w celu spełnienia żądania dostępu.</span><span class="sxs-lookup"><span data-stu-id="96d5d-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="96d5d-117">Możesz opcjonalnie użyć warstw chmury w tym punkcie końcowym serwera, aby określić, czy ten punkt końcowy ma zostać buforem pełnego zestawu plików z chmury.</span><span class="sxs-lookup"><span data-stu-id="96d5d-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="96d5d-118">Jeśli jest używana warstwa chmury, pobieranie zawartości pliku zostanie zatrzymane w punkcie zdefiniowanym przez zasady warstwy chmury, które można ustawić.</span><span class="sxs-lookup"><span data-stu-id="96d5d-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="96d5d-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96d5d-119">EXAMPLES</span></span>

### <span data-ttu-id="96d5d-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96d5d-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="96d5d-121">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze i wstawia go do grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="96d5d-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="96d5d-122">W ten sposób jest on częścią topologii innych punktów końcowych, a metadane plików i zawartość będą od razu rozpoczynać synchronizację między wszystkimi lokalizacjami, do których odwołuje się punkty końcowe, w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="96d5d-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="96d5d-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96d5d-123">PARAMETERS</span></span>

### <span data-ttu-id="96d5d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96d5d-124">-AsJob</span></span>
<span data-ttu-id="96d5d-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="96d5d-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96d5d-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="96d5d-126">-CloudTiering</span></span>
<span data-ttu-id="96d5d-127">Parametr warstwy chmury</span><span class="sxs-lookup"><span data-stu-id="96d5d-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="96d5d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d5d-128">-DefaultProfile</span></span>
<span data-ttu-id="96d5d-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96d5d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96d5d-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="96d5d-130">-Name</span></span>
<span data-ttu-id="96d5d-131">Nazwa ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="96d5d-131">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="96d5d-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="96d5d-133">Parametr danych w chmurze</span><span class="sxs-lookup"><span data-stu-id="96d5d-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="96d5d-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="96d5d-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="96d5d-135">Parametr URI udziału pliku danych w chmurze</span><span class="sxs-lookup"><span data-stu-id="96d5d-135">Cloud Seeded Data File Share Uri Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="96d5d-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="96d5d-137">Parametr tryb lokalnej pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="96d5d-137">Local cache mode Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="96d5d-138">-localCacheMode</span></span>
<span data-ttu-id="96d5d-139">Parametr tryb lokalnej pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="96d5d-139">Local cache mode Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-140">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="96d5d-140">-ParentObject</span></span>
<span data-ttu-id="96d5d-141">Obiekt do synchronizacji, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="96d5d-141">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="96d5d-142">-ParentResourceId</span></span>
<span data-ttu-id="96d5d-143">Identyfikator zasobu nadrzędnego w obiekcie resync</span><span class="sxs-lookup"><span data-stu-id="96d5d-143">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d5d-144">-ResourceGroupName</span></span>
<span data-ttu-id="96d5d-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="96d5d-145">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="96d5d-146">-ServerLocalPath</span></span>
<span data-ttu-id="96d5d-147">Parametr ścieżka lokalna serwera</span><span class="sxs-lookup"><span data-stu-id="96d5d-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="96d5d-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="96d5d-148">-ServerResourceId</span></span>
<span data-ttu-id="96d5d-149">Identyfikator zasobu RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="96d5d-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="96d5d-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="96d5d-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="96d5d-151">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="96d5d-151">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="96d5d-152">-SyncGroupName</span></span>
<span data-ttu-id="96d5d-153">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="96d5d-153">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="96d5d-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="96d5d-155">Pliki warstw starsze niż dni</span><span class="sxs-lookup"><span data-stu-id="96d5d-155">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="96d5d-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="96d5d-157">Parametr procent wolnego miejsca w woluminie</span><span class="sxs-lookup"><span data-stu-id="96d5d-157">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d5d-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96d5d-158">-Confirm</span></span>
<span data-ttu-id="96d5d-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96d5d-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96d5d-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96d5d-160">-WhatIf</span></span>
<span data-ttu-id="96d5d-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96d5d-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96d5d-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="96d5d-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96d5d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d5d-163">CommonParameters</span></span>
<span data-ttu-id="96d5d-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d5d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d5d-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d5d-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d5d-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96d5d-166">INPUTS</span></span>

### <span data-ttu-id="96d5d-167">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96d5d-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="96d5d-168">System. String</span><span class="sxs-lookup"><span data-stu-id="96d5d-168">System.String</span></span>

## <span data-ttu-id="96d5d-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96d5d-169">OUTPUTS</span></span>

### <span data-ttu-id="96d5d-170">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d5d-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="96d5d-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96d5d-171">NOTES</span></span>

## <span data-ttu-id="96d5d-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96d5d-172">RELATED LINKS</span></span>
