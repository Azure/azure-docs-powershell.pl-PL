---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188811"
---
# <span data-ttu-id="66372-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="66372-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="66372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66372-102">SYNOPSIS</span></span>
<span data-ttu-id="66372-103">To polecenie spowoduje usunięcie określonej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="66372-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="66372-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="66372-104">SYNTAX</span></span>

### <span data-ttu-id="66372-105">StringParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="66372-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66372-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66372-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66372-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66372-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66372-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="66372-108">DESCRIPTION</span></span>
<span data-ttu-id="66372-109">To polecenie spowoduje usunięcie określonej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="66372-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="66372-110">Usługę synchronizacji przestrzeni dyskowej można usunąć tylko wtedy, gdy najpierw zostaną usunięte wszystkie zawarte w niej grupy synchronizacji i zarejestrowane serwery.</span><span class="sxs-lookup"><span data-stu-id="66372-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="66372-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="66372-111">EXAMPLES</span></span>

### <span data-ttu-id="66372-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="66372-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="66372-113">To polecenie spowoduje usunięcie usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="66372-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="66372-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66372-114">PARAMETERS</span></span>

### <span data-ttu-id="66372-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="66372-115">-AsJob</span></span>
<span data-ttu-id="66372-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="66372-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66372-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66372-117">-DefaultProfile</span></span>
<span data-ttu-id="66372-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="66372-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66372-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="66372-119">-Force</span></span>
<span data-ttu-id="66372-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="66372-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="66372-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66372-121">-InputObject</span></span>
<span data-ttu-id="66372-122">Obiekt wejściowy StorageSyncService, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="66372-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66372-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="66372-123">-Name</span></span>
<span data-ttu-id="66372-124">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="66372-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66372-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66372-125">-PassThru</span></span>
<span data-ttu-id="66372-126">W normalnym wykonywaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="66372-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="66372-127">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="66372-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="66372-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66372-128">-ResourceGroupName</span></span>
<span data-ttu-id="66372-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66372-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="66372-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66372-130">-ResourceId</span></span>
<span data-ttu-id="66372-131">Identyfikator zasobu usługi StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="66372-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="66372-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66372-132">-Confirm</span></span>
<span data-ttu-id="66372-133">Przed uruchomieniem polecenia cmdlet jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="66372-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66372-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66372-134">-WhatIf</span></span>
<span data-ttu-id="66372-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66372-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66372-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="66372-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66372-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66372-137">CommonParameters</span></span>
<span data-ttu-id="66372-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66372-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66372-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66372-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66372-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66372-140">INPUTS</span></span>

### <span data-ttu-id="66372-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="66372-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="66372-142">System.String</span><span class="sxs-lookup"><span data-stu-id="66372-142">System.String</span></span>

### <span data-ttu-id="66372-143">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="66372-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66372-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66372-144">OUTPUTS</span></span>

### <span data-ttu-id="66372-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="66372-145">System.Object</span></span>
## <span data-ttu-id="66372-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="66372-146">NOTES</span></span>

## <span data-ttu-id="66372-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66372-147">RELATED LINKS</span></span>
