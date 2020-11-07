---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: c724527b380e0004d30e0790024634bcc6ce550d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707467"
---
# <span data-ttu-id="cf123-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="cf123-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="cf123-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf123-102">SYNOPSIS</span></span>
<span data-ttu-id="cf123-103">To polecenie wyświetla listę wszystkich usług synchronizacji magazynu w danym zakresie grupy abonament/Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf123-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="cf123-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf123-104">SYNTAX</span></span>

### <span data-ttu-id="cf123-105">ParentStringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cf123-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf123-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf123-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf123-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cf123-107">DESCRIPTION</span></span>
<span data-ttu-id="cf123-108">To polecenie wyświetla listę wszystkich usług synchronizacji magazynu w danym zakresie grupy abonament/Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf123-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="cf123-109">Można go również użyć w celu przejrzenia atrybutów każdej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf123-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="cf123-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf123-110">EXAMPLES</span></span>

### <span data-ttu-id="cf123-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf123-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="cf123-112">To polecenie wyświetla listę wszystkich zasobów usługi synchronizacji magazynu w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf123-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="cf123-113">Można go również użyć w celu przejrzenia atrybutów każdej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf123-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="cf123-114">Określ — StorageSyncServiceName, aby zwrócić określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="cf123-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="cf123-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf123-115">PARAMETERS</span></span>

### <span data-ttu-id="cf123-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf123-116">-DefaultProfile</span></span>
<span data-ttu-id="cf123-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf123-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf123-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf123-118">-Name</span></span>
<span data-ttu-id="cf123-119">Nazwa usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf123-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="cf123-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf123-120">-ResourceGroupName</span></span>
<span data-ttu-id="cf123-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf123-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="cf123-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf123-122">CommonParameters</span></span>
<span data-ttu-id="cf123-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf123-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf123-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf123-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf123-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf123-125">INPUTS</span></span>

### <span data-ttu-id="cf123-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cf123-126">System.String</span></span>

## <span data-ttu-id="cf123-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf123-127">OUTPUTS</span></span>

### <span data-ttu-id="cf123-128">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="cf123-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="cf123-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf123-129">NOTES</span></span>

## <span data-ttu-id="cf123-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf123-130">RELATED LINKS</span></span>