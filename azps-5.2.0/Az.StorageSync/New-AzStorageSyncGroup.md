---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366662"
---
# <span data-ttu-id="60dbd-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="60dbd-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="60dbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="60dbd-103">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="60dbd-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="60dbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60dbd-104">SYNTAX</span></span>

### <span data-ttu-id="60dbd-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60dbd-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60dbd-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60dbd-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60dbd-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="60dbd-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60dbd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="60dbd-108">DESCRIPTION</span></span>
<span data-ttu-id="60dbd-109">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="60dbd-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="60dbd-110">Grupa synchronizacji służy do opisywania topologii lokalizacji, które są nazywane punktami końcowymi, co spowoduje zsynchronizowanie wszystkich plików przechowywanych w jednym z punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="60dbd-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="60dbd-111">Grupa synchronizacji zawiera punkty końcowe chmury, które odwołują się do udziałów plików platformy Azure, a także zawiera punkty końcowe serwera, które odwołują się do określonej ścieżki lokalnej na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="60dbd-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="60dbd-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60dbd-112">EXAMPLES</span></span>

### <span data-ttu-id="60dbd-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60dbd-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="60dbd-114">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="60dbd-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="60dbd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60dbd-115">PARAMETERS</span></span>

### <span data-ttu-id="60dbd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60dbd-116">-DefaultProfile</span></span>
<span data-ttu-id="60dbd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60dbd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60dbd-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60dbd-118">-Name</span></span>
<span data-ttu-id="60dbd-119">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="60dbd-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="60dbd-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="60dbd-120">-ParentObject</span></span>
<span data-ttu-id="60dbd-121">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="60dbd-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="60dbd-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="60dbd-122">-ParentResourceId</span></span>
<span data-ttu-id="60dbd-123">Identyfikator zasobu nadrzędnego StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="60dbd-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="60dbd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60dbd-124">-ResourceGroupName</span></span>
<span data-ttu-id="60dbd-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="60dbd-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="60dbd-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="60dbd-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="60dbd-127">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="60dbd-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="60dbd-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60dbd-128">-Confirm</span></span>
<span data-ttu-id="60dbd-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60dbd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60dbd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60dbd-130">-WhatIf</span></span>
<span data-ttu-id="60dbd-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60dbd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60dbd-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60dbd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60dbd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60dbd-133">CommonParameters</span></span>
<span data-ttu-id="60dbd-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60dbd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60dbd-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60dbd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60dbd-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60dbd-136">INPUTS</span></span>

### <span data-ttu-id="60dbd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="60dbd-137">System.String</span></span>

### <span data-ttu-id="60dbd-138">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="60dbd-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="60dbd-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60dbd-139">OUTPUTS</span></span>

### <span data-ttu-id="60dbd-140">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="60dbd-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="60dbd-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60dbd-141">NOTES</span></span>

## <span data-ttu-id="60dbd-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60dbd-142">RELATED LINKS</span></span>
