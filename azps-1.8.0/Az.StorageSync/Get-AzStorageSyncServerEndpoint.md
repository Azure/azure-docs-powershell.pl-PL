---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b71da416d7609f05d4716090dc8f09bf0ec0b084
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707466"
---
# <span data-ttu-id="2e4d8-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e4d8-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="2e4d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e4d8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4d8-103">To polecenie wyświetla listę wszystkich punktów końcowych serwera w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="2e4d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e4d8-104">SYNTAX</span></span>

### <span data-ttu-id="2e4d8-105">ObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e4d8-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e4d8-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e4d8-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e4d8-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e4d8-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e4d8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2e4d8-108">DESCRIPTION</span></span>
<span data-ttu-id="2e4d8-109">To polecenie wyświetla listę wszystkich punktów końcowych serwera w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="2e4d8-110">Można go również użyć w celu wymuszenia listy atrybutów każdego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="2e4d8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e4d8-111">EXAMPLES</span></span>

### <span data-ttu-id="2e4d8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e4d8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="2e4d8-113">To polecenie pobiera wszystkie punkty końcowe serwera zawarte w określonej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="2e4d8-114">Określ — ServerEndpointName, aby zwrócić określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="2e4d8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e4d8-115">PARAMETERS</span></span>

### <span data-ttu-id="2e4d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4d8-116">-DefaultProfile</span></span>
<span data-ttu-id="2e4d8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e4d8-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e4d8-118">-Name</span></span>
<span data-ttu-id="2e4d8-119">Nazwa punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="2e4d8-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="2e4d8-120">-ParentObject</span></span>
<span data-ttu-id="2e4d8-121">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="2e4d8-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e4d8-122">-ParentResourceId</span></span>
<span data-ttu-id="2e4d8-123">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="2e4d8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e4d8-124">-ResourceGroupName</span></span>
<span data-ttu-id="2e4d8-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="2e4d8-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="2e4d8-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="2e4d8-127">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="2e4d8-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2e4d8-128">-SyncGroupName</span></span>
<span data-ttu-id="2e4d8-129">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="2e4d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4d8-130">CommonParameters</span></span>
<span data-ttu-id="2e4d8-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e4d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4d8-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e4d8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4d8-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e4d8-133">INPUTS</span></span>

### <span data-ttu-id="2e4d8-134">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2e4d8-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="2e4d8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2e4d8-135">System.String</span></span>

## <span data-ttu-id="2e4d8-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e4d8-136">OUTPUTS</span></span>

### <span data-ttu-id="2e4d8-137">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e4d8-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="2e4d8-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e4d8-138">NOTES</span></span>

## <span data-ttu-id="2e4d8-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e4d8-139">RELATED LINKS</span></span>
