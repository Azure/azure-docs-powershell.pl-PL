---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: c76fd37e0a95c6ea5c39897c617602106979f94a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011386"
---
# <span data-ttu-id="fa071-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa071-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="fa071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa071-102">SYNOPSIS</span></span>
<span data-ttu-id="fa071-103">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="fa071-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="fa071-104">Dzięki temu określona ścieżka na serwerze może rozpocząć synchronizację plików z innymi punktami końcowymi w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fa071-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="fa071-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa071-105">SYNTAX</span></span>

### <span data-ttu-id="fa071-106">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fa071-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa071-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa071-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa071-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa071-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa071-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa071-109">DESCRIPTION</span></span>
<span data-ttu-id="fa071-110">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="fa071-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="fa071-111">Dzięki temu określona ścieżka na serwerze może rozpocząć synchronizację plików z innymi punktami końcowymi w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fa071-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="fa071-112">Jeśli w grupie synchronizacji znajdują się już pliki w innych punktach końcowych, a ta nowo dodana lokalizacja również zawiera pliki, proces uzgadniania spróbuje ustalić, czy pliki w rzeczywistości są takie same w tych samych folderach co w innych punktach końcowych.</span><span class="sxs-lookup"><span data-stu-id="fa071-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="fa071-113">Przestrzenie nazw będą scalać i uzgadniać pliki, aby zapobiec plikom konfliktów.</span><span class="sxs-lookup"><span data-stu-id="fa071-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="fa071-114">Jeśli istnieją pliki w innych punktach końcowych serwera, często lepszym rozwiązaniem jest rozpoczęcie od pustej lokalizacji na tym serwerze, aby pliki z chmury zeszły na serwer w procesie automatycznym nazywanym szybkim odzyskiwaniem po awarii.</span><span class="sxs-lookup"><span data-stu-id="fa071-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="fa071-115">Metadane przestrzeni nazw zostaną najpierw zsynchronizowane w dół, a następnie zostanie pobrany strumień danych każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="fa071-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="fa071-116">Jeśli użytkownik lub aplikacja zażąda pliku poza kolejnością pobierania, ten plik zostanie odwołany z priorytetem w celu spełnienia żądania dostępu.</span><span class="sxs-lookup"><span data-stu-id="fa071-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="fa071-117">Opcjonalnie możesz użyć określania warstw w chmurze dla tego punktu końcowego serwera, aby określić, czy ten punkt końcowy powinien stać się pamięcią podręczną pełnego zestawu plików z chmury.</span><span class="sxs-lookup"><span data-stu-id="fa071-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="fa071-118">W przypadku przechowywania warstw w chmurze pobieranie zawartości pliku zakończy się w punkcie zdefiniowanym przez zasady warstwy w chmurze, które można ustawić.</span><span class="sxs-lookup"><span data-stu-id="fa071-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="fa071-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa071-119">EXAMPLES</span></span>

### <span data-ttu-id="fa071-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa071-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="fa071-121">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze i wstawia go do grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fa071-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="fa071-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations references as endpoints in the sync group.</span><span class="sxs-lookup"><span data-stu-id="fa071-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="fa071-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa071-123">PARAMETERS</span></span>

### <span data-ttu-id="fa071-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fa071-124">-AsJob</span></span>
<span data-ttu-id="fa071-125">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fa071-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa071-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="fa071-126">-CloudTiering</span></span>
<span data-ttu-id="fa071-127">Parametr warstwy w chmurze</span><span class="sxs-lookup"><span data-stu-id="fa071-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="fa071-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa071-128">-DefaultProfile</span></span>
<span data-ttu-id="fa071-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa071-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa071-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fa071-130">-Name</span></span>
<span data-ttu-id="fa071-131">Nazwa serweraEndpoint.</span><span class="sxs-lookup"><span data-stu-id="fa071-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="fa071-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="fa071-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="fa071-133">Parametr danych iniekowany w chmurze</span><span class="sxs-lookup"><span data-stu-id="fa071-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="fa071-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="fa071-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="fa071-135">Parametr Uri udostępniania pliku danych w chmurze</span><span class="sxs-lookup"><span data-stu-id="fa071-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="fa071-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="fa071-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="fa071-137">Parametr trybu lokalnej pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="fa071-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="fa071-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="fa071-138">-localCacheMode</span></span>
<span data-ttu-id="fa071-139">Parametr trybu lokalnej pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="fa071-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="fa071-140">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="fa071-140">-ParentObject</span></span>
<span data-ttu-id="fa071-141">Obiekt SyncGroup, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="fa071-141">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="fa071-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fa071-142">-ParentResourceId</span></span>
<span data-ttu-id="fa071-143">Identyfikator zasobu nadrzędnego grupy synchronizacji</span><span class="sxs-lookup"><span data-stu-id="fa071-143">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="fa071-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa071-144">-ResourceGroupName</span></span>
<span data-ttu-id="fa071-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa071-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="fa071-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="fa071-146">-ServerLocalPath</span></span>
<span data-ttu-id="fa071-147">Parametr ścieżki lokalnej serwera</span><span class="sxs-lookup"><span data-stu-id="fa071-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="fa071-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="fa071-148">-ServerResourceId</span></span>
<span data-ttu-id="fa071-149">Zarejestrowany identyfikator zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="fa071-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="fa071-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fa071-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="fa071-151">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="fa071-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="fa071-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="fa071-152">-SyncGroupName</span></span>
<span data-ttu-id="fa071-153">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fa071-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="fa071-154">-TierFilesOlderDays</span><span class="sxs-lookup"><span data-stu-id="fa071-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="fa071-155">Parametr Pliki warstwy starsze niż dni</span><span class="sxs-lookup"><span data-stu-id="fa071-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="fa071-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="fa071-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="fa071-157">Parametr procentu wolnego miejsca (volume free space)</span><span class="sxs-lookup"><span data-stu-id="fa071-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="fa071-158">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa071-158">-Confirm</span></span>
<span data-ttu-id="fa071-159">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fa071-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa071-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa071-160">-WhatIf</span></span>
<span data-ttu-id="fa071-161">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa071-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa071-162">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fa071-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa071-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa071-163">CommonParameters</span></span>
<span data-ttu-id="fa071-164">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa071-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa071-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa071-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa071-166">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa071-166">INPUTS</span></span>

### <span data-ttu-id="fa071-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa071-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="fa071-168">System.String</span><span class="sxs-lookup"><span data-stu-id="fa071-168">System.String</span></span>

## <span data-ttu-id="fa071-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa071-169">OUTPUTS</span></span>

### <span data-ttu-id="fa071-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa071-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="fa071-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa071-171">NOTES</span></span>

## <span data-ttu-id="fa071-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa071-172">RELATED LINKS</span></span>
