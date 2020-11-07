---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 03b4ea18bc40f8ddd3a2dc2605427013c45d7506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707436"
---
# <span data-ttu-id="4143b-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4143b-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="4143b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4143b-102">SYNOPSIS</span></span>
<span data-ttu-id="4143b-103">To polecenie umożliwia wprowadzanie zmian w parametrach regulowanych w punkcie końcowym serwera.</span><span class="sxs-lookup"><span data-stu-id="4143b-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="4143b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4143b-104">SYNTAX</span></span>

### <span data-ttu-id="4143b-105">ObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4143b-105">ObjectParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4143b-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4143b-106">StringParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4143b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4143b-107">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4143b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4143b-108">DESCRIPTION</span></span>
<span data-ttu-id="4143b-109">To polecenie umożliwia wprowadzanie zmian w parametrach regulowanych w punkcie końcowym serwera.</span><span class="sxs-lookup"><span data-stu-id="4143b-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="4143b-110">W przypadku wystąpienia warstw chmury i zasad warstw w chmurze można w dowolnej chwili zmienić.</span><span class="sxs-lookup"><span data-stu-id="4143b-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="4143b-111">Po utworzeniu punktu końcowego serwera nie można zmienić kilku aspektów punktu końcowego serwera, takich jak ścieżka lokalna.</span><span class="sxs-lookup"><span data-stu-id="4143b-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="4143b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4143b-112">EXAMPLES</span></span>

### <span data-ttu-id="4143b-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4143b-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="4143b-114">W tym przykładzie wykonywane są dwie akcje, które określają nowe zasady warstwy chmury w określonym punkcie końcowym serwera, które przekierowują serwer do poziomu wszystkich plików, do których nie uzyskano dostępu w ciągu 30 dni, a także wyłącza tryb transferu danych w trybie offline, który początkowo włączono na tym punkcie końcowym serwera podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="4143b-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="4143b-115">Usługa transferu danych w trybie offline jest używana w ramach współdziałania usług migracji zbiorczej, takich jak pole danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4143b-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="4143b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4143b-116">PARAMETERS</span></span>

### <span data-ttu-id="4143b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4143b-117">-AsJob</span></span>
<span data-ttu-id="4143b-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4143b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4143b-119">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="4143b-119">-OfflineDataTransfer</span></span>
<span data-ttu-id="4143b-120">Parametr danych w chmurze</span><span class="sxs-lookup"><span data-stu-id="4143b-120">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="4143b-121">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="4143b-121">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="4143b-122">Parametr URI udziału pliku danych w chmurze</span><span class="sxs-lookup"><span data-stu-id="4143b-122">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="4143b-123">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="4143b-123">-CloudTiering</span></span>
<span data-ttu-id="4143b-124">Parametr warstwy chmury</span><span class="sxs-lookup"><span data-stu-id="4143b-124">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="4143b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4143b-125">-DefaultProfile</span></span>
<span data-ttu-id="4143b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4143b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4143b-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4143b-127">-InputObject</span></span>
<span data-ttu-id="4143b-128">Obiekt do synchronizacji, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="4143b-128">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="4143b-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4143b-129">-Name</span></span>
<span data-ttu-id="4143b-130">Nazwa ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4143b-130">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="4143b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4143b-131">-ResourceGroupName</span></span>
<span data-ttu-id="4143b-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4143b-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="4143b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4143b-133">-ResourceId</span></span>
<span data-ttu-id="4143b-134">Identyfikator zasobu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4143b-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="4143b-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4143b-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="4143b-136">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4143b-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4143b-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4143b-137">-SyncGroupName</span></span>
<span data-ttu-id="4143b-138">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="4143b-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4143b-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="4143b-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="4143b-140">Pliki warstw starsze niż dni</span><span class="sxs-lookup"><span data-stu-id="4143b-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="4143b-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="4143b-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="4143b-142">Parametr procent wolnego miejsca w woluminie</span><span class="sxs-lookup"><span data-stu-id="4143b-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="4143b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4143b-143">CommonParameters</span></span>
<span data-ttu-id="4143b-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4143b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4143b-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4143b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4143b-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4143b-146">INPUTS</span></span>

### <span data-ttu-id="4143b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4143b-147">System.String</span></span>

### <span data-ttu-id="4143b-148">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4143b-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4143b-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4143b-149">OUTPUTS</span></span>

### <span data-ttu-id="4143b-150">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4143b-150">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4143b-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4143b-151">NOTES</span></span>

## <span data-ttu-id="4143b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4143b-152">RELATED LINKS</span></span>
