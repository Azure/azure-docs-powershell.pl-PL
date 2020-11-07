---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 34f4dc1933e755167333d12d4566838ea47c26b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707454"
---
# <span data-ttu-id="22d93-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="22d93-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="22d93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22d93-102">SYNOPSIS</span></span>
<span data-ttu-id="22d93-103">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="22d93-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="22d93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22d93-104">SYNTAX</span></span>

### <span data-ttu-id="22d93-105">ObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22d93-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d93-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d93-106">StringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d93-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d93-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22d93-108">Opis</span><span class="sxs-lookup"><span data-stu-id="22d93-108">DESCRIPTION</span></span>
<span data-ttu-id="22d93-109">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="22d93-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="22d93-110">Grupa synchronizacji służy do opisywania topologii lokalizacji, które są nazywane punktami końcowymi, co spowoduje zsynchronizowanie wszystkich plików przechowywanych w jednym z punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="22d93-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="22d93-111">Grupa synchronizacji zawiera punkty końcowe chmury, które odwołują się do udziałów plików platformy Azure, a także zawiera punkty końcowe serwera, które odwołują się do określonej ścieżki lokalnej na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="22d93-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="22d93-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22d93-112">EXAMPLES</span></span>

### <span data-ttu-id="22d93-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22d93-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="22d93-114">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="22d93-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="22d93-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22d93-115">PARAMETERS</span></span>

### <span data-ttu-id="22d93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d93-116">-DefaultProfile</span></span>
<span data-ttu-id="22d93-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22d93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d93-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22d93-118">-Name</span></span>
<span data-ttu-id="22d93-119">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="22d93-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d93-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="22d93-120">-ParentObject</span></span>
<span data-ttu-id="22d93-121">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="22d93-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="22d93-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="22d93-122">-ParentResourceId</span></span>
<span data-ttu-id="22d93-123">Identyfikator zasobu nadrzędnego StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="22d93-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="22d93-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d93-124">-ResourceGroupName</span></span>
<span data-ttu-id="22d93-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22d93-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="22d93-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="22d93-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="22d93-127">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="22d93-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="22d93-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d93-128">CommonParameters</span></span>
<span data-ttu-id="22d93-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d93-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d93-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d93-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d93-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22d93-131">INPUTS</span></span>

### <span data-ttu-id="22d93-132">System. String</span><span class="sxs-lookup"><span data-stu-id="22d93-132">System.String</span></span>

### <span data-ttu-id="22d93-133">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="22d93-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="22d93-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22d93-134">OUTPUTS</span></span>

### <span data-ttu-id="22d93-135">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="22d93-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="22d93-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22d93-136">NOTES</span></span>

## <span data-ttu-id="22d93-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22d93-137">RELATED LINKS</span></span>
