---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: c21ea8d0dedef5afda6c8f40eedf949b915f0367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052089"
---
# <span data-ttu-id="6e7ef-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e7ef-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="6e7ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="6e7ef-103">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="6e7ef-104">Spowoduje to włączenie określonej ścieżki na serwerze w celu zsynchronizowania plików z innymi punktami końcowymi w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="6e7ef-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e7ef-105">SYNTAX</span></span>

### <span data-ttu-id="6e7ef-106">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6e7ef-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7ef-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e7ef-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7ef-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e7ef-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e7ef-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6e7ef-109">DESCRIPTION</span></span>
<span data-ttu-id="6e7ef-110">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="6e7ef-111">Spowoduje to włączenie określonej ścieżki na serwerze w celu zsynchronizowania plików z innymi punktami końcowymi w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="6e7ef-112">Jeśli w grupie synchronizacja istnieją już pliki w innych punktach końcowych, a nowo dodana lokalizacja również zawiera pliki, proces uzgadniania będzie próbował ustalić, czy pliki są w rzeczywistości te same w tych samych folderach, co w przypadku innych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="6e7ef-113">Obszary nazw będą scalać i uzgadniać, aby zapobiec konfliktom plików.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="6e7ef-114">Jeśli na innych punktach końcowych serwera znajdują się jakieś pliki, często lepiej rozpoczynać się od pustej lokalizacji na tym serwerze, aby pliki z chmury były wyświetlane na serwerze w procesie automatycznym zwanym funkcją szybkiego odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="6e7ef-115">Metadane przestrzeni nazw zostaną najpierw zsynchronizowane, a następnie zostanie pobrany strumień danych każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="6e7ef-116">Jeśli użytkownik lub aplikacja zażądała przeładowania pliku, zostanie on przypomniany przy użyciu priorytetu w celu spełnienia żądania dostępu.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="6e7ef-117">Możesz opcjonalnie użyć warstw chmury w tym punkcie końcowym serwera, aby określić, czy ten punkt końcowy ma zostać buforem pełnego zestawu plików z chmury.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="6e7ef-118">Jeśli jest używana warstwa chmury, pobieranie zawartości pliku zostanie zatrzymane w punkcie zdefiniowanym przez zasady warstwy chmury, które można ustawić.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="6e7ef-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e7ef-119">EXAMPLES</span></span>

### <span data-ttu-id="6e7ef-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e7ef-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="6e7ef-121">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze i wstawia go do grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="6e7ef-122">W ten sposób jest on częścią topologii innych punktów końcowych, a metadane plików i zawartość będą od razu rozpoczynać synchronizację między wszystkimi lokalizacjami, do których odwołuje się punkty końcowe, w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="6e7ef-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e7ef-123">PARAMETERS</span></span>

### <span data-ttu-id="6e7ef-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e7ef-124">-AsJob</span></span>
<span data-ttu-id="6e7ef-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6e7ef-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e7ef-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="6e7ef-126">-CloudTiering</span></span>
<span data-ttu-id="6e7ef-127">Parametr warstwy chmury</span><span class="sxs-lookup"><span data-stu-id="6e7ef-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="6e7ef-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e7ef-128">-DefaultProfile</span></span>
<span data-ttu-id="6e7ef-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e7ef-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e7ef-130">-Name</span></span>
<span data-ttu-id="6e7ef-131">Nazwa ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="6e7ef-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="6e7ef-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="6e7ef-133">Parametr danych w chmurze</span><span class="sxs-lookup"><span data-stu-id="6e7ef-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="6e7ef-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="6e7ef-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="6e7ef-135">Parametr URI udziału pliku danych w chmurze</span><span class="sxs-lookup"><span data-stu-id="6e7ef-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="6e7ef-136">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6e7ef-136">-ParentObject</span></span>
<span data-ttu-id="6e7ef-137">Obiekt do synchronizacji, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-137">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="6e7ef-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6e7ef-138">-ParentResourceId</span></span>
<span data-ttu-id="6e7ef-139">Identyfikator zasobu nadrzędnego w obiekcie resync</span><span class="sxs-lookup"><span data-stu-id="6e7ef-139">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="6e7ef-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e7ef-140">-ResourceGroupName</span></span>
<span data-ttu-id="6e7ef-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="6e7ef-142">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="6e7ef-142">-ServerLocalPath</span></span>
<span data-ttu-id="6e7ef-143">Parametr ścieżka lokalna serwera</span><span class="sxs-lookup"><span data-stu-id="6e7ef-143">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="6e7ef-144">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="6e7ef-144">-ServerResourceId</span></span>
<span data-ttu-id="6e7ef-145">Identyfikator zasobu RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="6e7ef-145">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="6e7ef-146">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6e7ef-146">-StorageSyncServiceName</span></span>
<span data-ttu-id="6e7ef-147">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-147">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6e7ef-148">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6e7ef-148">-SyncGroupName</span></span>
<span data-ttu-id="6e7ef-149">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-149">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="6e7ef-150">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="6e7ef-150">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="6e7ef-151">Pliki warstw starsze niż dni</span><span class="sxs-lookup"><span data-stu-id="6e7ef-151">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="6e7ef-152">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="6e7ef-152">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="6e7ef-153">Parametr procent wolnego miejsca w woluminie</span><span class="sxs-lookup"><span data-stu-id="6e7ef-153">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="6e7ef-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e7ef-154">-Confirm</span></span>
<span data-ttu-id="6e7ef-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e7ef-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e7ef-156">-WhatIf</span></span>
<span data-ttu-id="6e7ef-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e7ef-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e7ef-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e7ef-159">CommonParameters</span></span>
<span data-ttu-id="6e7ef-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e7ef-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e7ef-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e7ef-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e7ef-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e7ef-162">INPUTS</span></span>

### <span data-ttu-id="6e7ef-163">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6e7ef-163">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="6e7ef-164">System. String</span><span class="sxs-lookup"><span data-stu-id="6e7ef-164">System.String</span></span>

## <span data-ttu-id="6e7ef-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e7ef-165">OUTPUTS</span></span>

### <span data-ttu-id="6e7ef-166">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e7ef-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="6e7ef-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e7ef-167">NOTES</span></span>

## <span data-ttu-id="6e7ef-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e7ef-168">RELATED LINKS</span></span>
