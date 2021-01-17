---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491193"
---
# <span data-ttu-id="8b1e4-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8b1e4-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="8b1e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b1e4-102">SYNOPSIS</span></span>
<span data-ttu-id="8b1e4-103">To polecenie tworzy nową usługę synchronizacji magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="8b1e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b1e4-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b1e4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b1e4-105">DESCRIPTION</span></span>
<span data-ttu-id="8b1e4-106">Usługa synchronizacji magazynu to zasób najwyższego poziomu w usłudze Azure File Sync. To polecenie tworzy nową usługę synchronizacji magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="8b1e4-107">Zalecamy utworzenie jako najmniej małej liczby usług synchronizacji magazynu, które są absolutnie niezbędne do rozróżnienia różnych grup serwerów w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="8b1e4-108">Usługa synchronizacji magazynu zawiera grupy synchronizacji, a także działa jako element docelowy, aby zarejestrować serwery.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="8b1e4-109">Serwer może być zarejestrowany tylko w jednej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="8b1e4-110">Jeśli serwery muszą brać udział w synchronizowaniu tego samego zestawu plików, zarejestruj je w tej samej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="8b1e4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b1e4-111">EXAMPLES</span></span>

### <span data-ttu-id="8b1e4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b1e4-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="8b1e4-113">To polecenie spowoduje utworzenie usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="8b1e4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b1e4-114">PARAMETERS</span></span>

### <span data-ttu-id="8b1e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b1e4-115">-DefaultProfile</span></span>
<span data-ttu-id="8b1e4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b1e4-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8b1e4-117">-Location</span></span>
<span data-ttu-id="8b1e4-118">Lokalizacja usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-118">Storage Sync Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b1e4-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="8b1e4-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="8b1e4-120">Usługa synchronizacji magazynu IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="8b1e4-120">Storage Sync Service IncomingTrafficPolicy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b1e4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b1e4-121">-Name</span></span>
<span data-ttu-id="8b1e4-122">Nazwa usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-122">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b1e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b1e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b1e4-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b1e4-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b1e4-125">-Tag</span></span>
<span data-ttu-id="8b1e4-126">Znaczniki usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-126">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b1e4-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b1e4-127">-Confirm</span></span>
<span data-ttu-id="8b1e4-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b1e4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b1e4-129">-WhatIf</span></span>
<span data-ttu-id="8b1e4-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b1e4-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b1e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b1e4-132">CommonParameters</span></span>
<span data-ttu-id="8b1e4-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b1e4-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b1e4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b1e4-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b1e4-135">INPUTS</span></span>

### <span data-ttu-id="8b1e4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8b1e4-136">System.String</span></span>

## <span data-ttu-id="8b1e4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b1e4-137">OUTPUTS</span></span>

### <span data-ttu-id="8b1e4-138">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8b1e4-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="8b1e4-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b1e4-139">NOTES</span></span>

## <span data-ttu-id="8b1e4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b1e4-140">RELATED LINKS</span></span>
