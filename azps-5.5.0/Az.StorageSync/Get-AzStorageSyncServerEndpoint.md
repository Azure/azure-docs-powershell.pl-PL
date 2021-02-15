---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183091"
---
# <span data-ttu-id="3a609-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a609-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="3a609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a609-102">SYNOPSIS</span></span>
<span data-ttu-id="3a609-103">To polecenie wyświetla listę wszystkich punktów końcowych serwera w obrębie danej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="3a609-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="3a609-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a609-104">SYNTAX</span></span>

### <span data-ttu-id="3a609-105">StringParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3a609-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a609-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a609-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a609-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a609-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a609-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a609-108">DESCRIPTION</span></span>
<span data-ttu-id="3a609-109">To polecenie wyświetla listę wszystkich punktów końcowych serwera w obrębie danej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="3a609-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="3a609-110">Za jego pomocą można również wyświetlić listę atrybutów poszczególnych punktów końcowych serwera.</span><span class="sxs-lookup"><span data-stu-id="3a609-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="3a609-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a609-111">EXAMPLES</span></span>

### <span data-ttu-id="3a609-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a609-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="3a609-113">To polecenie pobiera wszystkie punkty końcowe serwera zawarte w określonej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="3a609-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="3a609-114">Określanie wartości -ServerEndpointName w celu zwrócenia określonej wartości.</span><span class="sxs-lookup"><span data-stu-id="3a609-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="3a609-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a609-115">PARAMETERS</span></span>

### <span data-ttu-id="3a609-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a609-116">-DefaultProfile</span></span>
<span data-ttu-id="3a609-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a609-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a609-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3a609-118">-Name</span></span>
<span data-ttu-id="3a609-119">Nazwa punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="3a609-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="3a609-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="3a609-120">-ParentObject</span></span>
<span data-ttu-id="3a609-121">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="3a609-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3a609-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3a609-122">-ParentResourceId</span></span>
<span data-ttu-id="3a609-123">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="3a609-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3a609-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a609-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a609-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a609-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="3a609-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3a609-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="3a609-127">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="3a609-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="3a609-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3a609-128">-SyncGroupName</span></span>
<span data-ttu-id="3a609-129">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="3a609-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="3a609-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a609-130">CommonParameters</span></span>
<span data-ttu-id="3a609-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a609-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a609-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a609-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a609-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a609-133">INPUTS</span></span>

### <span data-ttu-id="3a609-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3a609-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="3a609-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3a609-135">System.String</span></span>

## <span data-ttu-id="3a609-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a609-136">OUTPUTS</span></span>

### <span data-ttu-id="3a609-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a609-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="3a609-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a609-138">NOTES</span></span>

## <span data-ttu-id="3a609-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a609-139">RELATED LINKS</span></span>
