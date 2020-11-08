---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225295"
---
# <span data-ttu-id="da889-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="da889-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="da889-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da889-102">SYNOPSIS</span></span>
<span data-ttu-id="da889-103">To polecenie spowoduje usunięcie określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="da889-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="da889-104">Synchronizacja z tą lokalizacją zostanie natychmiast zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="da889-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="da889-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da889-105">SYNTAX</span></span>

### <span data-ttu-id="da889-106">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da889-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da889-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da889-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da889-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da889-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da889-109">Opis</span><span class="sxs-lookup"><span data-stu-id="da889-109">DESCRIPTION</span></span>
<span data-ttu-id="da889-110">Usunięcie punktu końcowego serwera jest operacją niszczącą.</span><span class="sxs-lookup"><span data-stu-id="da889-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="da889-111">Ta lokalizacja serwera zatrzyma synchronizację.</span><span class="sxs-lookup"><span data-stu-id="da889-111">This server location will stop syncing.</span></span> <span data-ttu-id="da889-112">Nie należy wykonywać tej operacji, aby rozwiązać problemy z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="da889-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="da889-113">Jeśli ta lokalizacja serwera (zawierająca pliki) zostanie ponownie dodana do tej samej grupy synchronizacji, co punkt końcowy serwera, może spowodować konflikt plików i innych niezamierzonych konsekwencji.</span><span class="sxs-lookup"><span data-stu-id="da889-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="da889-114">To polecenie jest przeznaczone tylko do likwidacji.</span><span class="sxs-lookup"><span data-stu-id="da889-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="da889-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da889-115">EXAMPLES</span></span>

### <span data-ttu-id="da889-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da889-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="da889-117">To polecenie spowoduje usunięcie punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="da889-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="da889-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da889-118">PARAMETERS</span></span>

### <span data-ttu-id="da889-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da889-119">-AsJob</span></span>
<span data-ttu-id="da889-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="da889-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da889-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da889-121">-DefaultProfile</span></span>
<span data-ttu-id="da889-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da889-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da889-123">-Force</span><span class="sxs-lookup"><span data-stu-id="da889-123">-Force</span></span>
<span data-ttu-id="da889-124">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="da889-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="da889-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="da889-125">-InputObject</span></span>
<span data-ttu-id="da889-126">Obiekt wejściowy ServerEndpoint, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="da889-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da889-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da889-127">-Name</span></span>
<span data-ttu-id="da889-128">Nazwa ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="da889-128">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da889-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da889-129">-PassThru</span></span>
<span data-ttu-id="da889-130">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="da889-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="da889-131">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="da889-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="da889-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da889-132">-ResourceGroupName</span></span>
<span data-ttu-id="da889-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="da889-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="da889-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da889-134">-ResourceId</span></span>
<span data-ttu-id="da889-135">Identyfikator zasobu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="da889-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="da889-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="da889-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="da889-137">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="da889-137">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da889-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="da889-138">-SyncGroupName</span></span>
<span data-ttu-id="da889-139">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="da889-139">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da889-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da889-140">-Confirm</span></span>
<span data-ttu-id="da889-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da889-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da889-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da889-142">-WhatIf</span></span>
<span data-ttu-id="da889-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da889-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da889-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da889-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da889-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da889-145">CommonParameters</span></span>
<span data-ttu-id="da889-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da889-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da889-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da889-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da889-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da889-148">INPUTS</span></span>

### <span data-ttu-id="da889-149">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="da889-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="da889-150">System. String</span><span class="sxs-lookup"><span data-stu-id="da889-150">System.String</span></span>

## <span data-ttu-id="da889-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da889-151">OUTPUTS</span></span>

### <span data-ttu-id="da889-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="da889-152">System.Object</span></span>
## <span data-ttu-id="da889-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da889-153">NOTES</span></span>

## <span data-ttu-id="da889-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da889-154">RELATED LINKS</span></span>
