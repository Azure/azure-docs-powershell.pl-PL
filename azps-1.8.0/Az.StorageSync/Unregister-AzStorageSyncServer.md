---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 87734d63d28785282ad3285ef8cce0a574ba30e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707434"
---
# <span data-ttu-id="fdc9c-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="fdc9c-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="fdc9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fdc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc9c-103">Ostrzeżenie: Wyrejestrowanie serwera spowoduje usunięcie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="fdc9c-104">To polecenie spowoduje Wyrejestrowanie serwera, który jest usługą synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-104">This command will unregister a server it's the storage sync service.</span></span>

## <span data-ttu-id="fdc9c-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fdc9c-105">SYNTAX</span></span>

### <span data-ttu-id="fdc9c-106">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fdc9c-106">InputObjectParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc9c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdc9c-107">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc9c-108">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdc9c-108">StringParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdc9c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="fdc9c-109">DESCRIPTION</span></span>
<span data-ttu-id="fdc9c-110">To polecenie spowoduje Wyrejestrowanie serwera z usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="fdc9c-111">Ostrzeżenie: Wyrejestrowanie serwera spowoduje usunięcie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="fdc9c-112">Należy ją wywołać tylko wtedy, gdy masz pewność, że żadna ścieżka na tym serwerze nie będzie już synchronizowana.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="fdc9c-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fdc9c-113">EXAMPLES</span></span>

### <span data-ttu-id="fdc9c-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fdc9c-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="fdc9c-115">To polecenie wyrejestruje serwer, powodując usuwanie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="fdc9c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fdc9c-116">PARAMETERS</span></span>

### <span data-ttu-id="fdc9c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdc9c-117">-AsJob</span></span>
<span data-ttu-id="fdc9c-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fdc9c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdc9c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc9c-119">-DefaultProfile</span></span>
<span data-ttu-id="fdc9c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdc9c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fdc9c-121">-Force</span></span>
<span data-ttu-id="fdc9c-122">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-122">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdc9c-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fdc9c-123">-InputObject</span></span>
<span data-ttu-id="fdc9c-124">RegisteredServer obiekt wejściowy, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdc9c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdc9c-125">-PassThru</span></span>
<span data-ttu-id="fdc9c-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fdc9c-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fdc9c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdc9c-127">-ResourceGroupName</span></span>
<span data-ttu-id="fdc9c-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc9c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdc9c-129">-ResourceId</span></span>
<span data-ttu-id="fdc9c-130">Identyfikator zasobu RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="fdc9c-130">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdc9c-131">-ServerId</span><span class="sxs-lookup"><span data-stu-id="fdc9c-131">-ServerId</span></span>
<span data-ttu-id="fdc9c-132">Nazwa pola RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-132">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc9c-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fdc9c-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="fdc9c-134">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-134">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc9c-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fdc9c-135">-Confirm</span></span>
<span data-ttu-id="fdc9c-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-136">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc9c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc9c-137">-WhatIf</span></span>
<span data-ttu-id="fdc9c-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdc9c-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc9c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc9c-140">CommonParameters</span></span>
<span data-ttu-id="fdc9c-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc9c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc9c-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc9c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc9c-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdc9c-143">INPUTS</span></span>

### <span data-ttu-id="fdc9c-144">Microsoft. Azure. Commands. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="fdc9c-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="fdc9c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="fdc9c-145">System.String</span></span>

### <span data-ttu-id="fdc9c-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fdc9c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fdc9c-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fdc9c-147">OUTPUTS</span></span>

### <span data-ttu-id="fdc9c-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="fdc9c-148">System.Object</span></span>
## <span data-ttu-id="fdc9c-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fdc9c-149">NOTES</span></span>

## <span data-ttu-id="fdc9c-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fdc9c-150">RELATED LINKS</span></span>
