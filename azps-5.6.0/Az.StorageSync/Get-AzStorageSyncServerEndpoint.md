---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 81baab4f996d7a56b64f055f94a18c09b4305991
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973146"
---
# <span data-ttu-id="ece30-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece30-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="ece30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ece30-102">SYNOPSIS</span></span>
<span data-ttu-id="ece30-103">To polecenie wyświetla listę wszystkich punktów końcowych serwera w obrębie danej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ece30-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="ece30-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ece30-104">SYNTAX</span></span>

### <span data-ttu-id="ece30-105">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ece30-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ece30-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece30-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ece30-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece30-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ece30-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ece30-108">DESCRIPTION</span></span>
<span data-ttu-id="ece30-109">To polecenie wyświetla listę wszystkich punktów końcowych serwera w obrębie danej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ece30-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="ece30-110">Za jego pomocą można również wyświetlić listę atrybutów poszczególnych punktów końcowych serwera.</span><span class="sxs-lookup"><span data-stu-id="ece30-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="ece30-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ece30-111">EXAMPLES</span></span>

### <span data-ttu-id="ece30-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ece30-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="ece30-113">To polecenie pobiera wszystkie punkty końcowe serwera zawarte w określonej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ece30-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="ece30-114">Określanie wartości -ServerEndpointName w celu zwrócenia określonej wartości.</span><span class="sxs-lookup"><span data-stu-id="ece30-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="ece30-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ece30-115">PARAMETERS</span></span>

### <span data-ttu-id="ece30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece30-116">-DefaultProfile</span></span>
<span data-ttu-id="ece30-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ece30-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece30-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ece30-118">-Name</span></span>
<span data-ttu-id="ece30-119">Nazwa punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="ece30-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece30-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="ece30-120">-ParentObject</span></span>
<span data-ttu-id="ece30-121">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="ece30-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ece30-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ece30-122">-ParentResourceId</span></span>
<span data-ttu-id="ece30-123">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="ece30-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ece30-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece30-124">-ResourceGroupName</span></span>
<span data-ttu-id="ece30-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ece30-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ece30-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ece30-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="ece30-127">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ece30-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ece30-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ece30-128">-SyncGroupName</span></span>
<span data-ttu-id="ece30-129">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ece30-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece30-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece30-130">CommonParameters</span></span>
<span data-ttu-id="ece30-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece30-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece30-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece30-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece30-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ece30-133">INPUTS</span></span>

### <span data-ttu-id="ece30-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ece30-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="ece30-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ece30-135">System.String</span></span>

## <span data-ttu-id="ece30-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ece30-136">OUTPUTS</span></span>

### <span data-ttu-id="ece30-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece30-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="ece30-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ece30-138">NOTES</span></span>

## <span data-ttu-id="ece30-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ece30-139">RELATED LINKS</span></span>
