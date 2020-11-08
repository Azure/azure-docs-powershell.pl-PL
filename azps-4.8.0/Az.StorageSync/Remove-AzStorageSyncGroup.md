---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219707"
---
# <span data-ttu-id="275dc-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="275dc-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="275dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="275dc-102">SYNOPSIS</span></span>
<span data-ttu-id="275dc-103">To polecenie spowoduje usunięcie określonej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="275dc-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="275dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="275dc-104">SYNTAX</span></span>

### <span data-ttu-id="275dc-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="275dc-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="275dc-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="275dc-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275dc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="275dc-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="275dc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="275dc-108">DESCRIPTION</span></span>
<span data-ttu-id="275dc-109">To polecenie spowoduje usunięcie określonej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="275dc-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="275dc-110">Grupę synchronizacji można usunąć tylko wtedy, gdy wszystkie zawarte w niej punkty końcowe zostaną usunięte jako pierwsze.</span><span class="sxs-lookup"><span data-stu-id="275dc-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="275dc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="275dc-111">EXAMPLES</span></span>

### <span data-ttu-id="275dc-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="275dc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="275dc-113">To polecenie spowoduje usunięcie grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="275dc-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="275dc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="275dc-114">PARAMETERS</span></span>

### <span data-ttu-id="275dc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="275dc-115">-AsJob</span></span>
<span data-ttu-id="275dc-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="275dc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="275dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275dc-117">-DefaultProfile</span></span>
<span data-ttu-id="275dc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="275dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275dc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="275dc-119">-Force</span></span>
<span data-ttu-id="275dc-120">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="275dc-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="275dc-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="275dc-121">-InputObject</span></span>
<span data-ttu-id="275dc-122">Obiekt wejściowy obiektu Sync</span><span class="sxs-lookup"><span data-stu-id="275dc-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="275dc-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="275dc-123">-Name</span></span>
<span data-ttu-id="275dc-124">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="275dc-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275dc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="275dc-125">-PassThru</span></span>
<span data-ttu-id="275dc-126">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="275dc-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="275dc-127">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="275dc-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="275dc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275dc-128">-ResourceGroupName</span></span>
<span data-ttu-id="275dc-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="275dc-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="275dc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="275dc-130">-ResourceId</span></span>
<span data-ttu-id="275dc-131">Identyfikator zasobu w tej usłudze</span><span class="sxs-lookup"><span data-stu-id="275dc-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="275dc-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="275dc-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="275dc-133">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="275dc-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="275dc-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="275dc-134">-Confirm</span></span>
<span data-ttu-id="275dc-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275dc-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275dc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275dc-136">-WhatIf</span></span>
<span data-ttu-id="275dc-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275dc-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="275dc-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="275dc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275dc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275dc-139">CommonParameters</span></span>
<span data-ttu-id="275dc-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275dc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275dc-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275dc-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275dc-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="275dc-142">INPUTS</span></span>

### <span data-ttu-id="275dc-143">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="275dc-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="275dc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="275dc-144">System.String</span></span>

### <span data-ttu-id="275dc-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="275dc-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="275dc-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="275dc-146">OUTPUTS</span></span>

### <span data-ttu-id="275dc-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="275dc-147">System.Object</span></span>
## <span data-ttu-id="275dc-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="275dc-148">NOTES</span></span>

## <span data-ttu-id="275dc-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="275dc-149">RELATED LINKS</span></span>
