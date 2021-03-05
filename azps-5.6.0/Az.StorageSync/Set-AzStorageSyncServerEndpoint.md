---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 65df82b189442a32738e445a1b48093c18816bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974001"
---
# <span data-ttu-id="a942d-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a942d-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="a942d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a942d-102">SYNOPSIS</span></span>
<span data-ttu-id="a942d-103">To polecenie umożliwia zmiany parametrów dostosowywanych punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="a942d-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="a942d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a942d-104">SYNTAX</span></span>

### <span data-ttu-id="a942d-105">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a942d-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a942d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a942d-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a942d-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a942d-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a942d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a942d-108">DESCRIPTION</span></span>
<span data-ttu-id="a942d-109">To polecenie umożliwia zmiany parametrów dostosowywanych punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="a942d-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="a942d-110">Na przykład zasady warstwowania chmury i warstwy w chmurze można zmienić w dowolnym momencie.</span><span class="sxs-lookup"><span data-stu-id="a942d-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="a942d-111">Po utworzeniu punktu końcowego serwera nie można zmienić kilku aspektów punktu końcowego serwera, takich jak ścieżka lokalna.</span><span class="sxs-lookup"><span data-stu-id="a942d-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="a942d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a942d-112">EXAMPLES</span></span>

### <span data-ttu-id="a942d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a942d-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="a942d-114">W tym przykładzie wykonuje dwie akcje, ustawia nowe zasady warstwy w chmurze dla określonego punktu końcowego serwera, co powoduje kierowanie serwera do warstw wszystkich plików, do których nie uzyskano dostępu w ciągu ostatnich 30 dni, oraz wyłącza tryb przesyłania danych w trybie offline, który był początkowo włączony w tym punkcie końcowym serwera podczas jego tworzenia.</span><span class="sxs-lookup"><span data-stu-id="a942d-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="a942d-115">Transfer danych w trybie offline jest używany w ramach współdziałania z usługami migracji zbiorczej, takimi jak usługa Azure Data Box.</span><span class="sxs-lookup"><span data-stu-id="a942d-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="a942d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a942d-116">PARAMETERS</span></span>

### <span data-ttu-id="a942d-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a942d-117">-AsJob</span></span>
<span data-ttu-id="a942d-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a942d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a942d-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="a942d-119">-CloudTiering</span></span>
<span data-ttu-id="a942d-120">Parametr warstwy w chmurze</span><span class="sxs-lookup"><span data-stu-id="a942d-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="a942d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a942d-121">-DefaultProfile</span></span>
<span data-ttu-id="a942d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a942d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a942d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a942d-123">-InputObject</span></span>
<span data-ttu-id="a942d-124">Obiekt SyncGroup, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="a942d-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a942d-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a942d-125">-Name</span></span>
<span data-ttu-id="a942d-126">Nazwa serweraEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a942d-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a942d-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="a942d-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="a942d-128">Parametr danych iniekowany w chmurze</span><span class="sxs-lookup"><span data-stu-id="a942d-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="a942d-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="a942d-129">-localCacheMode</span></span>
<span data-ttu-id="a942d-130">Parametr trybu lokalnej pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="a942d-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="a942d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a942d-131">-ResourceGroupName</span></span>
<span data-ttu-id="a942d-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a942d-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="a942d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a942d-133">-ResourceId</span></span>
<span data-ttu-id="a942d-134">Identyfikator zasobu Programu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a942d-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a942d-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a942d-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="a942d-136">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="a942d-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a942d-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a942d-137">-SyncGroupName</span></span>
<span data-ttu-id="a942d-138">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a942d-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="a942d-139">-TierFilesOlderDays</span><span class="sxs-lookup"><span data-stu-id="a942d-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="a942d-140">Parametr Pliki warstwy starsze niż dni</span><span class="sxs-lookup"><span data-stu-id="a942d-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="a942d-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="a942d-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="a942d-142">Parametr procentu wolnego miejsca (volume free space)</span><span class="sxs-lookup"><span data-stu-id="a942d-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="a942d-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a942d-143">-Confirm</span></span>
<span data-ttu-id="a942d-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a942d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a942d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a942d-145">-WhatIf</span></span>
<span data-ttu-id="a942d-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a942d-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a942d-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a942d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a942d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a942d-148">CommonParameters</span></span>
<span data-ttu-id="a942d-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a942d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a942d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a942d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a942d-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a942d-151">INPUTS</span></span>

### <span data-ttu-id="a942d-152">System.String</span><span class="sxs-lookup"><span data-stu-id="a942d-152">System.String</span></span>

### <span data-ttu-id="a942d-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a942d-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="a942d-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a942d-154">OUTPUTS</span></span>

### <span data-ttu-id="a942d-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a942d-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="a942d-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a942d-156">NOTES</span></span>

## <span data-ttu-id="a942d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a942d-157">RELATED LINKS</span></span>
