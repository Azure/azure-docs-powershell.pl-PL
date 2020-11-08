---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222748"
---
# <span data-ttu-id="ef5da-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef5da-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="ef5da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef5da-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5da-103">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="ef5da-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="ef5da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef5da-104">SYNTAX</span></span>

### <span data-ttu-id="ef5da-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ef5da-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef5da-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5da-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef5da-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5da-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef5da-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ef5da-108">DESCRIPTION</span></span>
<span data-ttu-id="ef5da-109">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="ef5da-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="ef5da-110">Grupa synchronizacji służy do opisywania topologii lokalizacji, które są nazywane punktami końcowymi, co spowoduje zsynchronizowanie wszystkich plików przechowywanych w jednym z punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="ef5da-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="ef5da-111">Grupa synchronizacji zawiera punkty końcowe chmury, które odwołują się do udziałów plików platformy Azure, a także zawiera punkty końcowe serwera, które odwołują się do określonej ścieżki lokalnej na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="ef5da-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="ef5da-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef5da-112">EXAMPLES</span></span>

### <span data-ttu-id="ef5da-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef5da-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="ef5da-114">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="ef5da-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="ef5da-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef5da-115">PARAMETERS</span></span>

### <span data-ttu-id="ef5da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5da-116">-DefaultProfile</span></span>
<span data-ttu-id="ef5da-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef5da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef5da-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef5da-118">-Name</span></span>
<span data-ttu-id="ef5da-119">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="ef5da-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ef5da-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="ef5da-120">-ParentObject</span></span>
<span data-ttu-id="ef5da-121">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="ef5da-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ef5da-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ef5da-122">-ParentResourceId</span></span>
<span data-ttu-id="ef5da-123">Identyfikator zasobu nadrzędnego StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ef5da-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="ef5da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5da-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef5da-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef5da-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef5da-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ef5da-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="ef5da-127">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ef5da-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ef5da-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef5da-128">-Confirm</span></span>
<span data-ttu-id="ef5da-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef5da-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef5da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef5da-130">-WhatIf</span></span>
<span data-ttu-id="ef5da-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef5da-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef5da-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef5da-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef5da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5da-133">CommonParameters</span></span>
<span data-ttu-id="ef5da-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef5da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5da-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef5da-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5da-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef5da-136">INPUTS</span></span>

### <span data-ttu-id="ef5da-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ef5da-137">System.String</span></span>

### <span data-ttu-id="ef5da-138">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ef5da-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ef5da-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef5da-139">OUTPUTS</span></span>

### <span data-ttu-id="ef5da-140">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef5da-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="ef5da-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef5da-141">NOTES</span></span>

## <span data-ttu-id="ef5da-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef5da-142">RELATED LINKS</span></span>
