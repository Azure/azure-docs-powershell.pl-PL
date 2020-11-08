---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220218"
---
# <span data-ttu-id="ee771-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ee771-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="ee771-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee771-102">SYNOPSIS</span></span>
<span data-ttu-id="ee771-103">To polecenie ustawia usługę synchronizacji magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee771-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="ee771-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee771-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee771-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee771-105">DESCRIPTION</span></span>
<span data-ttu-id="ee771-106">Usługa synchronizacji magazynu to zasób najwyższego poziomu w usłudze Azure File Sync. To polecenie ustawia usługę synchronizacji magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee771-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="ee771-107">Zalecamy utworzenie jako najmniej małej liczby usług synchronizacji magazynu, które są absolutnie niezbędne do rozróżnienia różnych grup serwerów w organizacji.</span><span class="sxs-lookup"><span data-stu-id="ee771-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="ee771-108">Usługa synchronizacji magazynu zawiera grupy synchronizacji, a także działa jako element docelowy, aby zarejestrować serwery.</span><span class="sxs-lookup"><span data-stu-id="ee771-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="ee771-109">Serwer może być zarejestrowany tylko w jednej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="ee771-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="ee771-110">Jeśli serwery muszą brać udział w synchronizowaniu tego samego zestawu plików, zarejestruj je w tej samej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="ee771-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="ee771-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee771-111">EXAMPLES</span></span>

### <span data-ttu-id="ee771-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee771-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="ee771-113">To polecenie spowoduje ustawienie usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="ee771-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="ee771-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee771-114">PARAMETERS</span></span>

### <span data-ttu-id="ee771-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee771-115">-DefaultProfile</span></span>
<span data-ttu-id="ee771-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee771-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="ee771-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ee771-117">-Name</span></span>
<span data-ttu-id="ee771-118">Nazwa usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="ee771-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="ee771-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee771-119">-ResourceGroupName</span></span>
<span data-ttu-id="ee771-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee771-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee771-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="ee771-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="ee771-122">Usługa synchronizacji magazynu IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="ee771-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="ee771-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee771-123">-Tag</span></span>
<span data-ttu-id="ee771-124">Znaczniki usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="ee771-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="ee771-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee771-125">-Confirm</span></span>
<span data-ttu-id="ee771-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee771-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee771-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee771-127">-WhatIf</span></span>
<span data-ttu-id="ee771-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee771-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee771-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee771-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee771-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee771-130">CommonParameters</span></span>
<span data-ttu-id="ee771-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee771-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee771-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee771-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee771-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee771-133">INPUTS</span></span>

### <span data-ttu-id="ee771-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ee771-134">System.String</span></span>

## <span data-ttu-id="ee771-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee771-135">OUTPUTS</span></span>

### <span data-ttu-id="ee771-136">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ee771-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ee771-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee771-137">NOTES</span></span>

## <span data-ttu-id="ee771-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee771-138">RELATED LINKS</span></span>
