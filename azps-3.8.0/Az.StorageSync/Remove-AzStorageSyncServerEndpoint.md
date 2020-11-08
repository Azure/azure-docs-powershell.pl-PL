---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052140"
---
# <span data-ttu-id="f3d33-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3d33-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="f3d33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3d33-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d33-103">To polecenie spowoduje usunięcie określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="f3d33-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="f3d33-104">Synchronizacja z tą lokalizacją zostanie natychmiast zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="f3d33-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="f3d33-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3d33-105">SYNTAX</span></span>

### <span data-ttu-id="f3d33-106">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3d33-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d33-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3d33-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d33-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3d33-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3d33-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f3d33-109">DESCRIPTION</span></span>
<span data-ttu-id="f3d33-110">Usunięcie punktu końcowego serwera jest operacją niszczącą.</span><span class="sxs-lookup"><span data-stu-id="f3d33-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="f3d33-111">Ta lokalizacja serwera zatrzyma synchronizację.</span><span class="sxs-lookup"><span data-stu-id="f3d33-111">This server location will stop syncing.</span></span> <span data-ttu-id="f3d33-112">Nie należy wykonywać tej operacji, aby rozwiązać problemy z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="f3d33-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="f3d33-113">Jeśli ta lokalizacja serwera (zawierająca pliki) zostanie ponownie dodana do tej samej grupy synchronizacji, co punkt końcowy serwera, może spowodować konflikt plików i innych niezamierzonych konsekwencji.</span><span class="sxs-lookup"><span data-stu-id="f3d33-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="f3d33-114">To polecenie jest przeznaczone tylko do likwidacji.</span><span class="sxs-lookup"><span data-stu-id="f3d33-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="f3d33-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3d33-115">EXAMPLES</span></span>

### <span data-ttu-id="f3d33-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3d33-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="f3d33-117">To polecenie spowoduje usunięcie punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="f3d33-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="f3d33-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3d33-118">PARAMETERS</span></span>

### <span data-ttu-id="f3d33-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3d33-119">-AsJob</span></span>
<span data-ttu-id="f3d33-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f3d33-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3d33-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d33-121">-DefaultProfile</span></span>
<span data-ttu-id="f3d33-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d33-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3d33-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f3d33-123">-Force</span></span>
<span data-ttu-id="f3d33-124">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="f3d33-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="f3d33-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3d33-125">-InputObject</span></span>
<span data-ttu-id="f3d33-126">Obiekt wejściowy ServerEndpoint, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f3d33-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="f3d33-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3d33-127">-Name</span></span>
<span data-ttu-id="f3d33-128">Nazwa ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f3d33-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="f3d33-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3d33-129">-PassThru</span></span>
<span data-ttu-id="f3d33-130">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="f3d33-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f3d33-131">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="f3d33-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f3d33-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d33-132">-ResourceGroupName</span></span>
<span data-ttu-id="f3d33-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3d33-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="f3d33-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3d33-134">-ResourceId</span></span>
<span data-ttu-id="f3d33-135">Identyfikator zasobu ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3d33-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="f3d33-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f3d33-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="f3d33-137">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f3d33-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f3d33-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d33-138">-SyncGroupName</span></span>
<span data-ttu-id="f3d33-139">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="f3d33-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="f3d33-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3d33-140">-Confirm</span></span>
<span data-ttu-id="f3d33-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3d33-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3d33-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d33-142">-WhatIf</span></span>
<span data-ttu-id="f3d33-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3d33-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3d33-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3d33-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3d33-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d33-145">CommonParameters</span></span>
<span data-ttu-id="f3d33-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3d33-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d33-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d33-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d33-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3d33-148">INPUTS</span></span>

### <span data-ttu-id="f3d33-149">Microsoft. Azure. Commands. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3d33-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="f3d33-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f3d33-150">System.String</span></span>

## <span data-ttu-id="f3d33-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3d33-151">OUTPUTS</span></span>

### <span data-ttu-id="f3d33-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="f3d33-152">System.Object</span></span>
## <span data-ttu-id="f3d33-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3d33-153">NOTES</span></span>

## <span data-ttu-id="f3d33-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3d33-154">RELATED LINKS</span></span>
