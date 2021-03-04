---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: 62dcefcf48e1d4c685b2a4f4855af41da7d8db75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011322"
---
# <span data-ttu-id="e09dd-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="e09dd-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="e09dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e09dd-102">SYNOPSIS</span></span>
<span data-ttu-id="e09dd-103">To polecenie rejestruje serwer w usłudze synchronizacji magazynu, co tworzy relację zaufania.</span><span class="sxs-lookup"><span data-stu-id="e09dd-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="e09dd-104">Następnie można użyć programu PowerShell lub portalu Azure w celu skonfigurowania synchronizacji na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="e09dd-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="e09dd-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e09dd-105">SYNTAX</span></span>

### <span data-ttu-id="e09dd-106">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e09dd-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e09dd-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e09dd-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e09dd-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e09dd-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e09dd-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e09dd-109">DESCRIPTION</span></span>
<span data-ttu-id="e09dd-110">To polecenie rejestruje serwer w usłudze synchronizacji magazynu, zasób najwyższego poziomu do synchronizacji plików platformy Azure. Utworzono relację zaufania między serwerem a usługą synchronizacji magazynu, która zapewnia bezpieczeństwo kanałów transferu danych i zarządzania nimi.</span><span class="sxs-lookup"><span data-stu-id="e09dd-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="e09dd-111">Następnie można użyć programu PowerShell lub portalu Azure w celu skonfigurowania synchronizowanych danych na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="e09dd-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="e09dd-112">Serwer można zarejestrować tylko w jednej usłudze synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="e09dd-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="e09dd-113">Jeśli serwery zawsze muszą uczestniczyć w synchronizacji tego samego zestawu plików, zarejestruj je w tej samej usłudze synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="e09dd-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="e09dd-114">To polecenie musi być uruchamiane lokalnie na serwerze, który ma zostać zarejestrowany — wykonane bezpośrednio lub podczas zdalnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e09dd-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="e09dd-115">Nie można zaakceptować obiektu komputera zdalnego.</span><span class="sxs-lookup"><span data-stu-id="e09dd-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="e09dd-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e09dd-116">EXAMPLES</span></span>

### <span data-ttu-id="e09dd-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e09dd-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="e09dd-118">To polecenie zarejestruje serwer lokalny, na którym jest uruchomione to polecenie.</span><span class="sxs-lookup"><span data-stu-id="e09dd-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="e09dd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e09dd-119">PARAMETERS</span></span>

### <span data-ttu-id="e09dd-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e09dd-120">-AsJob</span></span>
<span data-ttu-id="e09dd-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e09dd-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e09dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09dd-122">-DefaultProfile</span></span>
<span data-ttu-id="e09dd-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e09dd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e09dd-124">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="e09dd-124">-ParentObject</span></span>
<span data-ttu-id="e09dd-125">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="e09dd-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="e09dd-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e09dd-126">-ParentResourceId</span></span>
<span data-ttu-id="e09dd-127">Identyfikator zasobu nadrzędnego usługi StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e09dd-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="e09dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e09dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="e09dd-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e09dd-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="e09dd-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e09dd-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="e09dd-131">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e09dd-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="e09dd-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e09dd-132">-Confirm</span></span>
<span data-ttu-id="e09dd-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e09dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e09dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e09dd-134">-WhatIf</span></span>
<span data-ttu-id="e09dd-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e09dd-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e09dd-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e09dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e09dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09dd-137">CommonParameters</span></span>
<span data-ttu-id="e09dd-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e09dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09dd-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e09dd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09dd-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e09dd-140">INPUTS</span></span>

### <span data-ttu-id="e09dd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e09dd-141">System.String</span></span>

### <span data-ttu-id="e09dd-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e09dd-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="e09dd-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e09dd-143">OUTPUTS</span></span>

### <span data-ttu-id="e09dd-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="e09dd-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="e09dd-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e09dd-145">NOTES</span></span>

## <span data-ttu-id="e09dd-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e09dd-146">RELATED LINKS</span></span>
