---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: bd1665ee82dfad0bb6028252ad100e5c651d0c2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887778"
---
# <span data-ttu-id="1c9b0-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="1c9b0-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="1c9b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9b0-103">To polecenie wyświetla listę wszystkich serwerów zarejestrowanych w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="1c9b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c9b0-104">SYNTAX</span></span>

### <span data-ttu-id="1c9b0-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c9b0-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c9b0-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c9b0-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c9b0-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c9b0-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c9b0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1c9b0-108">DESCRIPTION</span></span>
<span data-ttu-id="1c9b0-109">To polecenie wyświetla listę wszystkich serwerów zarejestrowanych w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="1c9b0-110">Można go również użyć, aby wyświetlić listę atrybutów każdego zarejestrowanego serwera.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="1c9b0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c9b0-111">EXAMPLES</span></span>

### <span data-ttu-id="1c9b0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c9b0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="1c9b0-113">To polecenie pobiera wszystkie serwery zarejestrowane w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="1c9b0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c9b0-114">PARAMETERS</span></span>

### <span data-ttu-id="1c9b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9b0-115">-DefaultProfile</span></span>
<span data-ttu-id="1c9b0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c9b0-117">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="1c9b0-117">-ParentObject</span></span>
<span data-ttu-id="1c9b0-118">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1c9b0-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1c9b0-119">-ParentResourceId</span></span>
<span data-ttu-id="1c9b0-120">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1c9b0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c9b0-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c9b0-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="1c9b0-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="1c9b0-123">-ServerId</span></span>
<span data-ttu-id="1c9b0-124">Nazwa pola RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-124">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="1c9b0-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1c9b0-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="1c9b0-126">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="1c9b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9b0-127">CommonParameters</span></span>
<span data-ttu-id="1c9b0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9b0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c9b0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9b0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c9b0-130">INPUTS</span></span>

### <span data-ttu-id="1c9b0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1c9b0-131">System.String</span></span>

### <span data-ttu-id="1c9b0-132">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1c9b0-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="1c9b0-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1c9b0-133">System.Guid</span></span>

## <span data-ttu-id="1c9b0-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c9b0-134">OUTPUTS</span></span>

### <span data-ttu-id="1c9b0-135">Microsoft. Azure. Commands. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="1c9b0-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="1c9b0-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c9b0-136">NOTES</span></span>

## <span data-ttu-id="1c9b0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c9b0-137">RELATED LINKS</span></span>
