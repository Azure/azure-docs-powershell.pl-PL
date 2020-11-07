---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 23aab4561e8127c67be4d9f751b250bc3fb6d1a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871996"
---
# <span data-ttu-id="ccaaf-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ccaaf-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="ccaaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccaaf-102">SYNOPSIS</span></span>
<span data-ttu-id="ccaaf-103">To polecenie umożliwia wprowadzanie zmian w parametrach regulowanych w punkcie końcowym serwera.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="ccaaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccaaf-104">SYNTAX</span></span>

### <span data-ttu-id="ccaaf-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ccaaf-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaaf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccaaf-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaaf-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccaaf-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccaaf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ccaaf-108">DESCRIPTION</span></span>
<span data-ttu-id="ccaaf-109">To polecenie umożliwia wprowadzanie zmian w parametrach regulowanych w punkcie końcowym serwera.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="ccaaf-110">W przypadku wystąpienia warstw chmury i zasad warstw w chmurze można w dowolnej chwili zmienić.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="ccaaf-111">Po utworzeniu punktu końcowego serwera nie można zmienić kilku aspektów punktu końcowego serwera, takich jak ścieżka lokalna.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="ccaaf-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccaaf-112">EXAMPLES</span></span>

### <span data-ttu-id="ccaaf-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ccaaf-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="ccaaf-114">W tym przykładzie wykonywane są dwie akcje, które określają nowe zasady warstwy chmury w określonym punkcie końcowym serwera, które przekierowują serwer do poziomu wszystkich plików, do których nie uzyskano dostępu w ciągu 30 dni, a także wyłącza tryb transferu danych w trybie offline, który początkowo włączono na tym punkcie końcowym serwera podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="ccaaf-115">Usługa transferu danych w trybie offline jest używana w ramach współdziałania usług migracji zbiorczej, takich jak pole danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="ccaaf-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccaaf-116">PARAMETERS</span></span>

### <span data-ttu-id="ccaaf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccaaf-117">-AsJob</span></span>
<span data-ttu-id="ccaaf-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ccaaf-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccaaf-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="ccaaf-119">-CloudTiering</span></span>
<span data-ttu-id="ccaaf-120">Parametr warstwy chmury</span><span class="sxs-lookup"><span data-stu-id="ccaaf-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="ccaaf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccaaf-121">-DefaultProfile</span></span>
<span data-ttu-id="ccaaf-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccaaf-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ccaaf-123">-InputObject</span></span>
<span data-ttu-id="ccaaf-124">Obiekt do synchronizacji, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ccaaf-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ccaaf-125">-Name</span></span>
<span data-ttu-id="ccaaf-126">Nazwa ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="ccaaf-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="ccaaf-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="ccaaf-128">Parametr danych w chmurze</span><span class="sxs-lookup"><span data-stu-id="ccaaf-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="ccaaf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccaaf-129">-ResourceGroupName</span></span>
<span data-ttu-id="ccaaf-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ccaaf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccaaf-131">-ResourceId</span></span>
<span data-ttu-id="ccaaf-132">Identyfikator zasobu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ccaaf-132">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="ccaaf-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ccaaf-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="ccaaf-134">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ccaaf-135">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ccaaf-135">-SyncGroupName</span></span>
<span data-ttu-id="ccaaf-136">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-136">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ccaaf-137">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="ccaaf-137">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="ccaaf-138">Pliki warstw starsze niż dni</span><span class="sxs-lookup"><span data-stu-id="ccaaf-138">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="ccaaf-139">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="ccaaf-139">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="ccaaf-140">Parametr procent wolnego miejsca w woluminie</span><span class="sxs-lookup"><span data-stu-id="ccaaf-140">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="ccaaf-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ccaaf-141">-Confirm</span></span>
<span data-ttu-id="ccaaf-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccaaf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccaaf-143">-WhatIf</span></span>
<span data-ttu-id="ccaaf-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccaaf-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccaaf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccaaf-146">CommonParameters</span></span>
<span data-ttu-id="ccaaf-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccaaf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccaaf-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccaaf-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccaaf-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccaaf-149">INPUTS</span></span>

### <span data-ttu-id="ccaaf-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ccaaf-150">System.String</span></span>

### <span data-ttu-id="ccaaf-151">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ccaaf-151">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="ccaaf-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccaaf-152">OUTPUTS</span></span>

### <span data-ttu-id="ccaaf-153">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ccaaf-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="ccaaf-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccaaf-154">NOTES</span></span>

## <span data-ttu-id="ccaaf-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccaaf-155">RELATED LINKS</span></span>
