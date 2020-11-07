---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: edfeebf9781c40b44a5a06db407757a5e2f5d2a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707450"
---
# <span data-ttu-id="9e078-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="9e078-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="9e078-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e078-102">SYNOPSIS</span></span>
<span data-ttu-id="9e078-103">To polecenie rejestruje serwer w usłudze synchronizacji magazynu, która tworzy relację zaufania.</span><span class="sxs-lookup"><span data-stu-id="9e078-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="9e078-104">Za pomocą programu PowerShell lub portalu Azure można skonfigurować synchronizację na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="9e078-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="9e078-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e078-105">SYNTAX</span></span>

### <span data-ttu-id="9e078-106">ObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e078-106">ObjectParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e078-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e078-107">StringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e078-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e078-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e078-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9e078-109">DESCRIPTION</span></span>
<span data-ttu-id="9e078-110">To polecenie rejestruje serwer w usłudze synchronizacji magazynu, zasób najwyższego poziomu w usłudze Azure File Sync. Utworzono relację zaufania między serwerem a usługą synchronizacji magazynu, która zapewnia bezpieczne przesyłanie danych i kanałów zarządzania.</span><span class="sxs-lookup"><span data-stu-id="9e078-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="9e078-111">Za pomocą programu PowerShell lub portalu Azure można skonfigurować synchronizację na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="9e078-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="9e078-112">Serwer może być zarejestrowany tylko w jednej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="9e078-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="9e078-113">Jeśli serwery muszą brać udział w synchronizowaniu tego samego zestawu plików, zarejestruj je w tej samej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="9e078-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="9e078-114">Polecenie musi być uruchamiane lokalnie na serwerze, który ma zostać zarejestrowany — wykonywane bezpośrednio lub za pośrednictwem zdalnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9e078-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="9e078-115">Nie można zaakceptować obiektu komputera zdalnego.</span><span class="sxs-lookup"><span data-stu-id="9e078-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="9e078-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e078-116">EXAMPLES</span></span>

### <span data-ttu-id="9e078-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e078-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="9e078-118">To polecenie spowoduje zarejestrowanie serwera lokalnego.</span><span class="sxs-lookup"><span data-stu-id="9e078-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="9e078-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e078-119">PARAMETERS</span></span>

### <span data-ttu-id="9e078-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e078-120">-AsJob</span></span>
<span data-ttu-id="9e078-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9e078-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e078-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e078-122">-DefaultProfile</span></span>
<span data-ttu-id="9e078-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e078-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e078-124">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="9e078-124">-ParentObject</span></span>
<span data-ttu-id="9e078-125">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="9e078-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9e078-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9e078-126">-ParentResourceId</span></span>
<span data-ttu-id="9e078-127">Identyfikator zasobu nadrzędnego StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9e078-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="9e078-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e078-128">-ResourceGroupName</span></span>
<span data-ttu-id="9e078-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e078-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="9e078-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9e078-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="9e078-131">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="9e078-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9e078-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e078-132">CommonParameters</span></span>
<span data-ttu-id="9e078-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e078-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e078-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e078-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e078-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e078-135">INPUTS</span></span>

### <span data-ttu-id="9e078-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9e078-136">System.String</span></span>

### <span data-ttu-id="9e078-137">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9e078-137">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="9e078-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e078-138">OUTPUTS</span></span>

### <span data-ttu-id="9e078-139">Microsoft. Azure. Commands. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="9e078-139">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="9e078-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e078-140">NOTES</span></span>

## <span data-ttu-id="9e078-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e078-141">RELATED LINKS</span></span>