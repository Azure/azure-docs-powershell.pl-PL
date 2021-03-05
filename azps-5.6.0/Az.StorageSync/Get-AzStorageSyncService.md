---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: 3aa6c569eb7f67b6021f7f40059cc9e528355a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973121"
---
# <span data-ttu-id="84059-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="84059-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="84059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84059-102">SYNOPSIS</span></span>
<span data-ttu-id="84059-103">To polecenie zawiera listę wszystkich usług synchronizacji przestrzeni dyskowej w obrębie danego zakresu grupy subskrypcji/zasobów.</span><span class="sxs-lookup"><span data-stu-id="84059-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="84059-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84059-104">SYNTAX</span></span>

### <span data-ttu-id="84059-105">ParentStringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="84059-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84059-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="84059-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84059-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="84059-107">DESCRIPTION</span></span>
<span data-ttu-id="84059-108">To polecenie zawiera listę wszystkich usług synchronizacji przestrzeni dyskowej w obrębie danego zakresu grupy subskrypcji/zasobów.</span><span class="sxs-lookup"><span data-stu-id="84059-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="84059-109">Za jego pomocą można również wyświetlić listę atrybutów poszczególnych usług synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="84059-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="84059-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84059-110">EXAMPLES</span></span>

### <span data-ttu-id="84059-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84059-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="84059-112">To polecenie zawiera listę wszystkich zasobów usługi synchronizacji magazynu w obrębie danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84059-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="84059-113">Za jego pomocą można również wyświetlić listę atrybutów poszczególnych usług synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="84059-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="84059-114">Specify -StorageSyncServiceName, aby zwrócić określoną.</span><span class="sxs-lookup"><span data-stu-id="84059-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="84059-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84059-115">PARAMETERS</span></span>

### <span data-ttu-id="84059-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84059-116">-DefaultProfile</span></span>
<span data-ttu-id="84059-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="84059-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84059-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="84059-118">-Name</span></span>
<span data-ttu-id="84059-119">Nazwa usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="84059-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="84059-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84059-120">-ResourceGroupName</span></span>
<span data-ttu-id="84059-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84059-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="84059-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84059-122">CommonParameters</span></span>
<span data-ttu-id="84059-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84059-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84059-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84059-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84059-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84059-125">INPUTS</span></span>

### <span data-ttu-id="84059-126">System.String</span><span class="sxs-lookup"><span data-stu-id="84059-126">System.String</span></span>

## <span data-ttu-id="84059-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84059-127">OUTPUTS</span></span>

### <span data-ttu-id="84059-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="84059-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="84059-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84059-129">NOTES</span></span>

## <span data-ttu-id="84059-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84059-130">RELATED LINKS</span></span>
