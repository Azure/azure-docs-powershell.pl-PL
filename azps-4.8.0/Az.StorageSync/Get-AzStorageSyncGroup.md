---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219711"
---
# <span data-ttu-id="6c8b3-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6c8b3-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="6c8b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8b3-103">To polecenie wyświetla listę wszystkich grup synchronizacji w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="6c8b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c8b3-104">SYNTAX</span></span>

### <span data-ttu-id="6c8b3-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c8b3-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c8b3-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8b3-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c8b3-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8b3-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c8b3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6c8b3-108">DESCRIPTION</span></span>
<span data-ttu-id="6c8b3-109">To polecenie wyświetla listę wszystkich grup synchronizacji w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="6c8b3-110">Można go również użyć w celu wymuszenia listy atrybutów każdej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="6c8b3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c8b3-111">EXAMPLES</span></span>

### <span data-ttu-id="6c8b3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c8b3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="6c8b3-113">To polecenie pobiera wszystkie grupy synchronizacji zawarte w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="6c8b3-114">Podaj nazwę, aby zwrócić określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="6c8b3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c8b3-115">PARAMETERS</span></span>

### <span data-ttu-id="6c8b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8b3-116">-DefaultProfile</span></span>
<span data-ttu-id="6c8b3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c8b3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c8b3-118">-Name</span></span>
<span data-ttu-id="6c8b3-119">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="6c8b3-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6c8b3-120">-ParentObject</span></span>
<span data-ttu-id="6c8b3-121">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="6c8b3-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6c8b3-122">-ParentResourceId</span></span>
<span data-ttu-id="6c8b3-123">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="6c8b3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c8b3-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c8b3-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6c8b3-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6c8b3-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="6c8b3-127">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6c8b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8b3-128">CommonParameters</span></span>
<span data-ttu-id="6c8b3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8b3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c8b3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8b3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c8b3-131">INPUTS</span></span>

### <span data-ttu-id="6c8b3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6c8b3-132">System.String</span></span>

### <span data-ttu-id="6c8b3-133">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="6c8b3-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="6c8b3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c8b3-134">OUTPUTS</span></span>

### <span data-ttu-id="6c8b3-135">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6c8b3-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="6c8b3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c8b3-136">NOTES</span></span>

## <span data-ttu-id="6c8b3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c8b3-137">RELATED LINKS</span></span>
