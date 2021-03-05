---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: e96b4360247937ace5a0e2894f3bfac19fc1da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011409"
---
# <span data-ttu-id="ee827-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ee827-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="ee827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee827-102">SYNOPSIS</span></span>
<span data-ttu-id="ee827-103">To polecenie tworzy nową grupę synchronizacji w ramach określonej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="ee827-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="ee827-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee827-104">SYNTAX</span></span>

### <span data-ttu-id="ee827-105">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ee827-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee827-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee827-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee827-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee827-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee827-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee827-108">DESCRIPTION</span></span>
<span data-ttu-id="ee827-109">To polecenie tworzy nową grupę synchronizacji w ramach określonej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="ee827-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="ee827-110">Grupa synchronizacji opisuje topologię lokalizacji, określanych mianem punktów końcowych, które będą synchronizować wszystkie pliki przechowywane w jednym z punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="ee827-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="ee827-111">Grupa synchronizacji zawiera punkty końcowe chmury, które odwołują się do udziałów plików platformy Azure, oraz zawiera punkty końcowe serwera, które odwołują się do określonej ścieżki lokalnej na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="ee827-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="ee827-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee827-112">EXAMPLES</span></span>

### <span data-ttu-id="ee827-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee827-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="ee827-114">To polecenie tworzy nową grupę synchronizacji w ramach określonej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="ee827-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="ee827-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee827-115">PARAMETERS</span></span>

### <span data-ttu-id="ee827-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee827-116">-DefaultProfile</span></span>
<span data-ttu-id="ee827-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee827-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee827-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ee827-118">-Name</span></span>
<span data-ttu-id="ee827-119">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ee827-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ee827-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="ee827-120">-ParentObject</span></span>
<span data-ttu-id="ee827-121">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="ee827-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ee827-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ee827-122">-ParentResourceId</span></span>
<span data-ttu-id="ee827-123">Identyfikator zasobu nadrzędnego usługi StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ee827-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="ee827-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee827-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee827-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee827-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee827-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ee827-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="ee827-127">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ee827-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ee827-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee827-128">-Confirm</span></span>
<span data-ttu-id="ee827-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ee827-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee827-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee827-130">-WhatIf</span></span>
<span data-ttu-id="ee827-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee827-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee827-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ee827-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee827-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee827-133">CommonParameters</span></span>
<span data-ttu-id="ee827-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee827-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee827-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee827-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee827-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee827-136">INPUTS</span></span>

### <span data-ttu-id="ee827-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ee827-137">System.String</span></span>

### <span data-ttu-id="ee827-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ee827-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ee827-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee827-139">OUTPUTS</span></span>

### <span data-ttu-id="ee827-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ee827-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="ee827-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee827-141">NOTES</span></span>

## <span data-ttu-id="ee827-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee827-142">RELATED LINKS</span></span>
