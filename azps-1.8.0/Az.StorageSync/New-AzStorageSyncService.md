---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: d2d18a908b53c9a8ab077671b7e2026516d40b17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707452"
---
# <span data-ttu-id="f9354-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f9354-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="f9354-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9354-102">SYNOPSIS</span></span>
<span data-ttu-id="f9354-103">To polecenie tworzy nową usługę synchronizacji magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9354-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="f9354-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9354-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9354-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9354-105">DESCRIPTION</span></span>
<span data-ttu-id="f9354-106">Usługa synchronizacji magazynu to zasób najwyższego poziomu w usłudze Azure File Sync. To polecenie tworzy nową usługę synchronizacji magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9354-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="f9354-107">Zalecamy utworzenie jako najmniej małej liczby usług synchronizacji magazynu, które są absolutnie niezbędne do rozróżnienia różnych grup serwerów w organizacji.</span><span class="sxs-lookup"><span data-stu-id="f9354-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="f9354-108">Usługa synchronizacji magazynu zawiera grupy synchronizacji, a także działa jako element docelowy, aby zarejestrować serwery.</span><span class="sxs-lookup"><span data-stu-id="f9354-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="f9354-109">Serwer może być zarejestrowany tylko w jednej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="f9354-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="f9354-110">Jeśli serwery muszą brać udział w synchronizowaniu tego samego zestawu plików, zarejestruj je w tej samej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="f9354-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="f9354-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9354-111">EXAMPLES</span></span>

### <span data-ttu-id="f9354-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9354-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="f9354-113">To polecenie spowoduje utworzenie usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="f9354-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="f9354-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9354-114">PARAMETERS</span></span>

### <span data-ttu-id="f9354-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9354-115">-DefaultProfile</span></span>
<span data-ttu-id="f9354-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9354-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9354-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f9354-117">-Location</span></span>
<span data-ttu-id="f9354-118">Lokalizacja usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="f9354-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="f9354-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9354-119">-Name</span></span>
<span data-ttu-id="f9354-120">Nazwa usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="f9354-120">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="f9354-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9354-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9354-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9354-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9354-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9354-123">-Tag</span></span>
<span data-ttu-id="f9354-124">Znaczniki usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="f9354-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9354-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9354-125">CommonParameters</span></span>
<span data-ttu-id="f9354-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9354-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9354-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9354-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9354-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9354-128">INPUTS</span></span>

### <span data-ttu-id="f9354-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f9354-129">System.String</span></span>

## <span data-ttu-id="f9354-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9354-130">OUTPUTS</span></span>

### <span data-ttu-id="f9354-131">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f9354-131">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="f9354-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9354-132">NOTES</span></span>

## <span data-ttu-id="f9354-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9354-133">RELATED LINKS</span></span>
