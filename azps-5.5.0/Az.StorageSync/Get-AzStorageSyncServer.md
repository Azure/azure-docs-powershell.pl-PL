---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183106"
---
# <span data-ttu-id="dc58d-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="dc58d-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="dc58d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc58d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc58d-103">To polecenie zawiera listę wszystkich serwerów zarejestrowanych w danej usłudze synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="dc58d-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="dc58d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dc58d-104">SYNTAX</span></span>

### <span data-ttu-id="dc58d-105">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dc58d-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc58d-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc58d-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc58d-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc58d-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc58d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dc58d-108">DESCRIPTION</span></span>
<span data-ttu-id="dc58d-109">To polecenie zawiera listę wszystkich serwerów zarejestrowanych w danej usłudze synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="dc58d-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="dc58d-110">Za jego pomocą można również wyświetlić listę atrybutów każdego zarejestrowanego serwera.</span><span class="sxs-lookup"><span data-stu-id="dc58d-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="dc58d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dc58d-111">EXAMPLES</span></span>

### <span data-ttu-id="dc58d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dc58d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="dc58d-113">To polecenie pobiera wszystkie serwery zarejestrowane w określonej usłudze synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="dc58d-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="dc58d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc58d-114">PARAMETERS</span></span>

### <span data-ttu-id="dc58d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc58d-115">-DefaultProfile</span></span>
<span data-ttu-id="dc58d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc58d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc58d-117">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="dc58d-117">-ParentObject</span></span>
<span data-ttu-id="dc58d-118">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="dc58d-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="dc58d-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dc58d-119">-ParentResourceId</span></span>
<span data-ttu-id="dc58d-120">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="dc58d-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="dc58d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc58d-121">-ResourceGroupName</span></span>
<span data-ttu-id="dc58d-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc58d-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc58d-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="dc58d-123">-ServerId</span></span>
<span data-ttu-id="dc58d-124">Nazwa zarejestrowanego serwera.</span><span class="sxs-lookup"><span data-stu-id="dc58d-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc58d-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="dc58d-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="dc58d-126">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="dc58d-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="dc58d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc58d-127">CommonParameters</span></span>
<span data-ttu-id="dc58d-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc58d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc58d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc58d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc58d-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc58d-130">INPUTS</span></span>

### <span data-ttu-id="dc58d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dc58d-131">System.String</span></span>

### <span data-ttu-id="dc58d-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dc58d-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="dc58d-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="dc58d-133">System.Guid</span></span>

## <span data-ttu-id="dc58d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc58d-134">OUTPUTS</span></span>

### <span data-ttu-id="dc58d-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="dc58d-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="dc58d-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dc58d-136">NOTES</span></span>

## <span data-ttu-id="dc58d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc58d-137">RELATED LINKS</span></span>
