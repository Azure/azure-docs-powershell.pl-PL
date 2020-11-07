---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: f7c1f129d9a5f6f6bdd117597a2943567fb4001d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707447"
---
# <span data-ttu-id="bb90e-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bb90e-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="bb90e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb90e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb90e-103">To polecenie spowoduje usunięcie określonej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="bb90e-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="bb90e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb90e-104">SYNTAX</span></span>

### <span data-ttu-id="bb90e-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb90e-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb90e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb90e-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb90e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb90e-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb90e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bb90e-108">DESCRIPTION</span></span>
<span data-ttu-id="bb90e-109">To polecenie spowoduje usunięcie określonej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="bb90e-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="bb90e-110">Grupę synchronizacji można usunąć tylko wtedy, gdy wszystkie zawarte w niej punkty końcowe zostaną usunięte jako pierwsze.</span><span class="sxs-lookup"><span data-stu-id="bb90e-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="bb90e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb90e-111">EXAMPLES</span></span>

### <span data-ttu-id="bb90e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb90e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="bb90e-113">To polecenie spowoduje usunięcie grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="bb90e-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="bb90e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb90e-114">PARAMETERS</span></span>

### <span data-ttu-id="bb90e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb90e-115">-AsJob</span></span>
<span data-ttu-id="bb90e-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bb90e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb90e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb90e-117">-DefaultProfile</span></span>
<span data-ttu-id="bb90e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb90e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb90e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bb90e-119">-Force</span></span>
<span data-ttu-id="bb90e-120">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="bb90e-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="bb90e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb90e-121">-InputObject</span></span>
<span data-ttu-id="bb90e-122">Obiekt wejściowy obiektu Sync</span><span class="sxs-lookup"><span data-stu-id="bb90e-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="bb90e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb90e-123">-Name</span></span>
<span data-ttu-id="bb90e-124">Nazwa tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="bb90e-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="bb90e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb90e-125">-PassThru</span></span>
<span data-ttu-id="bb90e-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bb90e-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bb90e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb90e-127">-ResourceGroupName</span></span>
<span data-ttu-id="bb90e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb90e-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="bb90e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb90e-129">-ResourceId</span></span>
<span data-ttu-id="bb90e-130">Identyfikator zasobu w tej usłudze</span><span class="sxs-lookup"><span data-stu-id="bb90e-130">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="bb90e-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="bb90e-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="bb90e-132">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="bb90e-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="bb90e-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb90e-133">-Confirm</span></span>
<span data-ttu-id="bb90e-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb90e-134">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb90e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb90e-135">-WhatIf</span></span>
<span data-ttu-id="bb90e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb90e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb90e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb90e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb90e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb90e-138">CommonParameters</span></span>
<span data-ttu-id="bb90e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb90e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb90e-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb90e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb90e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb90e-141">INPUTS</span></span>

### <span data-ttu-id="bb90e-142">Microsoft. Azure. Commands. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bb90e-142">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="bb90e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bb90e-143">System.String</span></span>

### <span data-ttu-id="bb90e-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bb90e-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bb90e-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb90e-145">OUTPUTS</span></span>

### <span data-ttu-id="bb90e-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="bb90e-146">System.Object</span></span>
## <span data-ttu-id="bb90e-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb90e-147">NOTES</span></span>

## <span data-ttu-id="bb90e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb90e-148">RELATED LINKS</span></span>
