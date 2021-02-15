---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183066"
---
# <span data-ttu-id="d9f81-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="d9f81-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="d9f81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f81-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f81-103">Ostrzeżenie: Wyrejestrowanie serwera spowoduje usuwanie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="d9f81-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="d9f81-104">To polecenie spowoduje wyrejestrowanie serwera z usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="d9f81-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="d9f81-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9f81-105">SYNTAX</span></span>

### <span data-ttu-id="d9f81-106">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d9f81-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f81-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f81-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f81-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f81-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9f81-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9f81-109">DESCRIPTION</span></span>
<span data-ttu-id="d9f81-110">To polecenie spowoduje wyrejestrowanie serwera z usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="d9f81-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="d9f81-111">Ostrzeżenie: Wyrejestrowanie serwera spowoduje usuwanie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="d9f81-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="d9f81-112">Powinna być wywoływana tylko wtedy, gdy masz pewność, że ścieżka na tym serwerze nie będzie już synchronizowana.</span><span class="sxs-lookup"><span data-stu-id="d9f81-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="d9f81-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9f81-113">EXAMPLES</span></span>

### <span data-ttu-id="d9f81-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9f81-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="d9f81-115">To polecenie spowoduje wyrejestrowanie serwera, powodując usuwanie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="d9f81-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="d9f81-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9f81-116">PARAMETERS</span></span>

### <span data-ttu-id="d9f81-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d9f81-117">-AsJob</span></span>
<span data-ttu-id="d9f81-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d9f81-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9f81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f81-119">-DefaultProfile</span></span>
<span data-ttu-id="d9f81-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f81-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9f81-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d9f81-121">-Force</span></span>
<span data-ttu-id="d9f81-122">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="d9f81-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="d9f81-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9f81-123">-InputObject</span></span>
<span data-ttu-id="d9f81-124">Zarejestrowany obiekt wejściowy Serwera, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="d9f81-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="d9f81-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9f81-125">-PassThru</span></span>
<span data-ttu-id="d9f81-126">W normalnym wykonywaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="d9f81-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="d9f81-127">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="d9f81-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="d9f81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f81-128">-ResourceGroupName</span></span>
<span data-ttu-id="d9f81-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9f81-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="d9f81-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9f81-130">-ResourceId</span></span>
<span data-ttu-id="d9f81-131">Zarejestrowany identyfikator zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="d9f81-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="d9f81-132">- ServerId</span><span class="sxs-lookup"><span data-stu-id="d9f81-132">-ServerId</span></span>
<span data-ttu-id="d9f81-133">Nazwa zarejestrowanego serwera.</span><span class="sxs-lookup"><span data-stu-id="d9f81-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="d9f81-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d9f81-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="d9f81-135">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="d9f81-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d9f81-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9f81-136">-Confirm</span></span>
<span data-ttu-id="d9f81-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9f81-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f81-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9f81-138">-WhatIf</span></span>
<span data-ttu-id="d9f81-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9f81-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9f81-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9f81-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9f81-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f81-141">CommonParameters</span></span>
<span data-ttu-id="d9f81-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f81-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f81-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9f81-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f81-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9f81-144">INPUTS</span></span>

### <span data-ttu-id="d9f81-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="d9f81-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="d9f81-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d9f81-146">System.String</span></span>

### <span data-ttu-id="d9f81-147">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d9f81-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d9f81-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9f81-148">OUTPUTS</span></span>

### <span data-ttu-id="d9f81-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="d9f81-149">System.Object</span></span>
## <span data-ttu-id="d9f81-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9f81-150">NOTES</span></span>

## <span data-ttu-id="d9f81-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9f81-151">RELATED LINKS</span></span>
