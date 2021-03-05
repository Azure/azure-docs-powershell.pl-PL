---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: 53ee755daeb0e483b98c9e8449720acce6e38233
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973162"
---
# <span data-ttu-id="4dbf9-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4dbf9-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="4dbf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dbf9-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbf9-103">To polecenie zawiera listę wszystkich grup synchronizacji w ramach danej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="4dbf9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4dbf9-104">SYNTAX</span></span>

### <span data-ttu-id="4dbf9-105">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4dbf9-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dbf9-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dbf9-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dbf9-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dbf9-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dbf9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4dbf9-108">DESCRIPTION</span></span>
<span data-ttu-id="4dbf9-109">To polecenie zawiera listę wszystkich grup synchronizacji w ramach danej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="4dbf9-110">Za jego pomocą można również wyświetlić listę atrybutów poszczególnych grup synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="4dbf9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4dbf9-111">EXAMPLES</span></span>

### <span data-ttu-id="4dbf9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4dbf9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="4dbf9-113">To polecenie pobiera wszystkie grupy synchronizacji zawarte w określonej usłudze synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="4dbf9-114">Specify -Name to return a specific one.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="4dbf9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dbf9-115">PARAMETERS</span></span>

### <span data-ttu-id="4dbf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dbf9-116">-DefaultProfile</span></span>
<span data-ttu-id="4dbf9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dbf9-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4dbf9-118">-Name</span></span>
<span data-ttu-id="4dbf9-119">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbf9-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="4dbf9-120">-ParentObject</span></span>
<span data-ttu-id="4dbf9-121">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbf9-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4dbf9-122">-ParentResourceId</span></span>
<span data-ttu-id="4dbf9-123">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbf9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbf9-124">-ResourceGroupName</span></span>
<span data-ttu-id="4dbf9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbf9-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4dbf9-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="4dbf9-127">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbf9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbf9-128">CommonParameters</span></span>
<span data-ttu-id="4dbf9-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dbf9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbf9-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dbf9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbf9-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dbf9-131">INPUTS</span></span>

### <span data-ttu-id="4dbf9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4dbf9-132">System.String</span></span>

### <span data-ttu-id="4dbf9-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="4dbf9-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="4dbf9-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dbf9-134">OUTPUTS</span></span>

### <span data-ttu-id="4dbf9-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4dbf9-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="4dbf9-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4dbf9-136">NOTES</span></span>

## <span data-ttu-id="4dbf9-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dbf9-137">RELATED LINKS</span></span>
