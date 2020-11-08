---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052087"
---
# <span data-ttu-id="3c8ae-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="3c8ae-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="3c8ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8ae-103">To polecenie rejestruje serwer w usłudze synchronizacji magazynu, która tworzy relację zaufania.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="3c8ae-104">Za pomocą programu PowerShell lub portalu Azure można skonfigurować synchronizację na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="3c8ae-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c8ae-105">SYNTAX</span></span>

### <span data-ttu-id="3c8ae-106">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3c8ae-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c8ae-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c8ae-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c8ae-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c8ae-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c8ae-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3c8ae-109">DESCRIPTION</span></span>
<span data-ttu-id="3c8ae-110">To polecenie rejestruje serwer w usłudze synchronizacji magazynu, zasób najwyższego poziomu w usłudze Azure File Sync. Utworzono relację zaufania między serwerem a usługą synchronizacji magazynu, która zapewnia bezpieczne przesyłanie danych i kanałów zarządzania.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="3c8ae-111">Za pomocą programu PowerShell lub portalu Azure można skonfigurować synchronizację na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="3c8ae-112">Serwer może być zarejestrowany tylko w jednej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="3c8ae-113">Jeśli serwery muszą brać udział w synchronizowaniu tego samego zestawu plików, zarejestruj je w tej samej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="3c8ae-114">Polecenie musi być uruchamiane lokalnie na serwerze, który ma zostać zarejestrowany — wykonywane bezpośrednio lub za pośrednictwem zdalnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="3c8ae-115">Nie można zaakceptować obiektu komputera zdalnego.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="3c8ae-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c8ae-116">EXAMPLES</span></span>

### <span data-ttu-id="3c8ae-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c8ae-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="3c8ae-118">To polecenie spowoduje zarejestrowanie serwera lokalnego.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="3c8ae-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c8ae-119">PARAMETERS</span></span>

### <span data-ttu-id="3c8ae-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c8ae-120">-AsJob</span></span>
<span data-ttu-id="3c8ae-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3c8ae-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c8ae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c8ae-122">-DefaultProfile</span></span>
<span data-ttu-id="3c8ae-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c8ae-124">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="3c8ae-124">-ParentObject</span></span>
<span data-ttu-id="3c8ae-125">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3c8ae-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3c8ae-126">-ParentResourceId</span></span>
<span data-ttu-id="3c8ae-127">Identyfikator zasobu nadrzędnego StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3c8ae-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="3c8ae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c8ae-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c8ae-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="3c8ae-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3c8ae-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="3c8ae-131">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="3c8ae-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c8ae-132">-Confirm</span></span>
<span data-ttu-id="3c8ae-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c8ae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c8ae-134">-WhatIf</span></span>
<span data-ttu-id="3c8ae-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c8ae-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c8ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8ae-137">CommonParameters</span></span>
<span data-ttu-id="3c8ae-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c8ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8ae-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c8ae-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8ae-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c8ae-140">INPUTS</span></span>

### <span data-ttu-id="3c8ae-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3c8ae-141">System.String</span></span>

### <span data-ttu-id="3c8ae-142">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3c8ae-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="3c8ae-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c8ae-143">OUTPUTS</span></span>

### <span data-ttu-id="3c8ae-144">Microsoft. Azure. Commands. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="3c8ae-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="3c8ae-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c8ae-145">NOTES</span></span>

## <span data-ttu-id="3c8ae-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c8ae-146">RELATED LINKS</span></span>
