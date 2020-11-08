---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219708"
---
# <span data-ttu-id="c689d-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c689d-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="c689d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c689d-102">SYNOPSIS</span></span>
<span data-ttu-id="c689d-103">To polecenie wyświetla listę wszystkich punktów końcowych serwera w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c689d-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="c689d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c689d-104">SYNTAX</span></span>

### <span data-ttu-id="c689d-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c689d-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c689d-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c689d-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c689d-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c689d-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c689d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c689d-108">DESCRIPTION</span></span>
<span data-ttu-id="c689d-109">To polecenie wyświetla listę wszystkich punktów końcowych serwera w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c689d-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="c689d-110">Można go również użyć w celu wymuszenia listy atrybutów każdego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="c689d-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="c689d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c689d-111">EXAMPLES</span></span>

### <span data-ttu-id="c689d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c689d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="c689d-113">To polecenie pobiera wszystkie punkty końcowe serwera zawarte w określonej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c689d-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="c689d-114">Określ — ServerEndpointName, aby zwrócić określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="c689d-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="c689d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c689d-115">PARAMETERS</span></span>

### <span data-ttu-id="c689d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c689d-116">-DefaultProfile</span></span>
<span data-ttu-id="c689d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c689d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c689d-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c689d-118">-Name</span></span>
<span data-ttu-id="c689d-119">Nazwa punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="c689d-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="c689d-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="c689d-120">-ParentObject</span></span>
<span data-ttu-id="c689d-121">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="c689d-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c689d-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c689d-122">-ParentResourceId</span></span>
<span data-ttu-id="c689d-123">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="c689d-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c689d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c689d-124">-ResourceGroupName</span></span>
<span data-ttu-id="c689d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c689d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c689d-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c689d-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="c689d-127">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="c689d-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c689d-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c689d-128">-SyncGroupName</span></span>
<span data-ttu-id="c689d-129">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="c689d-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="c689d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c689d-130">CommonParameters</span></span>
<span data-ttu-id="c689d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c689d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c689d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c689d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c689d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c689d-133">INPUTS</span></span>

### <span data-ttu-id="c689d-134">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c689d-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="c689d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c689d-135">System.String</span></span>

## <span data-ttu-id="c689d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c689d-136">OUTPUTS</span></span>

### <span data-ttu-id="c689d-137">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c689d-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="c689d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c689d-138">NOTES</span></span>

## <span data-ttu-id="c689d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c689d-139">RELATED LINKS</span></span>
