---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: 34e3033d1f5ce76d6d6c42aaacd5ced690b5d47c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707468"
---
# <span data-ttu-id="2d17b-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2d17b-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="2d17b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d17b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d17b-103">To polecenie wyświetla listę wszystkich grup synchronizacji w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d17b-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="2d17b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d17b-104">SYNTAX</span></span>

### <span data-ttu-id="2d17b-105">ObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2d17b-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d17b-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d17b-106">StringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d17b-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d17b-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d17b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2d17b-108">DESCRIPTION</span></span>
<span data-ttu-id="2d17b-109">To polecenie wyświetla listę wszystkich grup synchronizacji w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d17b-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="2d17b-110">Można go również użyć w celu wymuszenia listy atrybutów każdej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2d17b-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="2d17b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d17b-111">EXAMPLES</span></span>

### <span data-ttu-id="2d17b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d17b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="2d17b-113">To polecenie pobiera wszystkie grupy synchronizacji zawarte w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d17b-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="2d17b-114">Podaj nazwę, aby zwrócić określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="2d17b-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="2d17b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d17b-115">PARAMETERS</span></span>

### <span data-ttu-id="2d17b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d17b-116">-DefaultProfile</span></span>
<span data-ttu-id="2d17b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d17b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d17b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d17b-118">-Name</span></span>
<span data-ttu-id="2d17b-119">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="2d17b-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="2d17b-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="2d17b-120">-ParentObject</span></span>
<span data-ttu-id="2d17b-121">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="2d17b-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="2d17b-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2d17b-122">-ParentResourceId</span></span>
<span data-ttu-id="2d17b-123">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="2d17b-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="2d17b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d17b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d17b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d17b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="2d17b-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="2d17b-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="2d17b-127">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="2d17b-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="2d17b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d17b-128">CommonParameters</span></span>
<span data-ttu-id="2d17b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d17b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d17b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d17b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d17b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d17b-131">INPUTS</span></span>

### <span data-ttu-id="2d17b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2d17b-132">System.String</span></span>

### <span data-ttu-id="2d17b-133">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2d17b-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="2d17b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d17b-134">OUTPUTS</span></span>

### <span data-ttu-id="2d17b-135">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2d17b-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="2d17b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d17b-136">NOTES</span></span>

## <span data-ttu-id="2d17b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d17b-137">RELATED LINKS</span></span>
