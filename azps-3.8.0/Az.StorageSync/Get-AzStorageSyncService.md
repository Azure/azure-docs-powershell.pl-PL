---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894941"
---
# <span data-ttu-id="dcce1-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dcce1-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="dcce1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcce1-102">SYNOPSIS</span></span>
<span data-ttu-id="dcce1-103">To polecenie wyświetla listę wszystkich usług synchronizacji magazynu w danym zakresie grupy abonament/Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcce1-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="dcce1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcce1-104">SYNTAX</span></span>

### <span data-ttu-id="dcce1-105">ParentStringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dcce1-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcce1-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcce1-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcce1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dcce1-107">DESCRIPTION</span></span>
<span data-ttu-id="dcce1-108">To polecenie wyświetla listę wszystkich usług synchronizacji magazynu w danym zakresie grupy abonament/Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcce1-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="dcce1-109">Można go również użyć w celu przejrzenia atrybutów każdej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="dcce1-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="dcce1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcce1-110">EXAMPLES</span></span>

### <span data-ttu-id="dcce1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dcce1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="dcce1-112">To polecenie wyświetla listę wszystkich zasobów usługi synchronizacji magazynu w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcce1-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="dcce1-113">Można go również użyć w celu przejrzenia atrybutów każdej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="dcce1-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="dcce1-114">Określ — StorageSyncServiceName, aby zwrócić określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="dcce1-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="dcce1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcce1-115">PARAMETERS</span></span>

### <span data-ttu-id="dcce1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcce1-116">-DefaultProfile</span></span>
<span data-ttu-id="dcce1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcce1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcce1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcce1-118">-Name</span></span>
<span data-ttu-id="dcce1-119">Nazwa usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="dcce1-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcce1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcce1-120">-ResourceGroupName</span></span>
<span data-ttu-id="dcce1-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcce1-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="dcce1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcce1-122">CommonParameters</span></span>
<span data-ttu-id="dcce1-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcce1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcce1-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcce1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcce1-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcce1-125">INPUTS</span></span>

### <span data-ttu-id="dcce1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dcce1-126">System.String</span></span>

## <span data-ttu-id="dcce1-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcce1-127">OUTPUTS</span></span>

### <span data-ttu-id="dcce1-128">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dcce1-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="dcce1-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcce1-129">NOTES</span></span>

## <span data-ttu-id="dcce1-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcce1-130">RELATED LINKS</span></span>
