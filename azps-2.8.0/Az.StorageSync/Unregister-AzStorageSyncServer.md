---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 3752e520c3637ffa1e08bfd89d03c6caeebd4e18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871995"
---
# <span data-ttu-id="dd53f-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="dd53f-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="dd53f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd53f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd53f-103">Ostrzeżenie: Wyrejestrowanie serwera spowoduje usunięcie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="dd53f-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="dd53f-104">To polecenie spowoduje Wyrejestrowanie serwera z usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="dd53f-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="dd53f-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd53f-105">SYNTAX</span></span>

### <span data-ttu-id="dd53f-106">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dd53f-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd53f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd53f-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd53f-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd53f-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd53f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="dd53f-109">DESCRIPTION</span></span>
<span data-ttu-id="dd53f-110">To polecenie spowoduje Wyrejestrowanie serwera z usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="dd53f-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="dd53f-111">Ostrzeżenie: Wyrejestrowanie serwera spowoduje usunięcie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="dd53f-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="dd53f-112">Należy ją wywołać tylko wtedy, gdy masz pewność, że żadna ścieżka na tym serwerze nie będzie już synchronizowana.</span><span class="sxs-lookup"><span data-stu-id="dd53f-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="dd53f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd53f-113">EXAMPLES</span></span>

### <span data-ttu-id="dd53f-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd53f-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="dd53f-115">To polecenie wyrejestruje serwer, powodując usuwanie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="dd53f-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="dd53f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd53f-116">PARAMETERS</span></span>

### <span data-ttu-id="dd53f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd53f-117">-AsJob</span></span>
<span data-ttu-id="dd53f-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dd53f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd53f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd53f-119">-DefaultProfile</span></span>
<span data-ttu-id="dd53f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd53f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd53f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dd53f-121">-Force</span></span>
<span data-ttu-id="dd53f-122">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="dd53f-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="dd53f-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd53f-123">-InputObject</span></span>
<span data-ttu-id="dd53f-124">RegisteredServer obiekt wejściowy, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="dd53f-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="dd53f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd53f-125">-PassThru</span></span>
<span data-ttu-id="dd53f-126">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="dd53f-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="dd53f-127">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="dd53f-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="dd53f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd53f-128">-ResourceGroupName</span></span>
<span data-ttu-id="dd53f-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd53f-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd53f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd53f-130">-ResourceId</span></span>
<span data-ttu-id="dd53f-131">Identyfikator zasobu RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="dd53f-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="dd53f-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="dd53f-132">-ServerId</span></span>
<span data-ttu-id="dd53f-133">Nazwa pola RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="dd53f-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="dd53f-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="dd53f-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="dd53f-135">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="dd53f-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="dd53f-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd53f-136">-Confirm</span></span>
<span data-ttu-id="dd53f-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd53f-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd53f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd53f-138">-WhatIf</span></span>
<span data-ttu-id="dd53f-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd53f-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd53f-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd53f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd53f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd53f-141">CommonParameters</span></span>
<span data-ttu-id="dd53f-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd53f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd53f-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd53f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd53f-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd53f-144">INPUTS</span></span>

### <span data-ttu-id="dd53f-145">Microsoft. Azure. Commands. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="dd53f-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="dd53f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dd53f-146">System.String</span></span>

### <span data-ttu-id="dd53f-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dd53f-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dd53f-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd53f-148">OUTPUTS</span></span>

### <span data-ttu-id="dd53f-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="dd53f-149">System.Object</span></span>
## <span data-ttu-id="dd53f-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd53f-150">NOTES</span></span>

## <span data-ttu-id="dd53f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd53f-151">RELATED LINKS</span></span>
