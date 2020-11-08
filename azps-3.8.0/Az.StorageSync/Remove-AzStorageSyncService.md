---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052141"
---
# <span data-ttu-id="5b76d-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5b76d-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="5b76d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b76d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b76d-103">To polecenie spowoduje usunięcie określonej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="5b76d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b76d-104">SYNTAX</span></span>

### <span data-ttu-id="5b76d-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5b76d-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b76d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b76d-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b76d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b76d-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b76d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5b76d-108">DESCRIPTION</span></span>
<span data-ttu-id="5b76d-109">To polecenie spowoduje usunięcie określonej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="5b76d-110">Usługę synchronizacji magazynu można usunąć tylko wtedy, gdy wszystkie zawarte w niej grupy synchronizacji i zarejestrowane serwery zostaną usunięte jako pierwsze.</span><span class="sxs-lookup"><span data-stu-id="5b76d-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="5b76d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b76d-111">EXAMPLES</span></span>

### <span data-ttu-id="5b76d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5b76d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="5b76d-113">To polecenie spowoduje usunięcie usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="5b76d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b76d-114">PARAMETERS</span></span>

### <span data-ttu-id="5b76d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b76d-115">-AsJob</span></span>
<span data-ttu-id="5b76d-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5b76d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b76d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b76d-117">-DefaultProfile</span></span>
<span data-ttu-id="5b76d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b76d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b76d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5b76d-119">-Force</span></span>
<span data-ttu-id="5b76d-120">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="5b76d-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="5b76d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5b76d-121">-InputObject</span></span>
<span data-ttu-id="5b76d-122">Obiekt wejściowy StorageSyncService, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="5b76d-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5b76d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b76d-123">-Name</span></span>
<span data-ttu-id="5b76d-124">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5b76d-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="5b76d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b76d-125">-PassThru</span></span>
<span data-ttu-id="5b76d-126">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="5b76d-127">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="5b76d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b76d-128">-ResourceGroupName</span></span>
<span data-ttu-id="5b76d-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5b76d-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="5b76d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b76d-130">-ResourceId</span></span>
<span data-ttu-id="5b76d-131">Identyfikator zasobu StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5b76d-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="5b76d-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b76d-132">-Confirm</span></span>
<span data-ttu-id="5b76d-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b76d-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b76d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b76d-134">-WhatIf</span></span>
<span data-ttu-id="5b76d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b76d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b76d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5b76d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b76d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b76d-137">CommonParameters</span></span>
<span data-ttu-id="5b76d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b76d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b76d-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b76d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b76d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b76d-140">INPUTS</span></span>

### <span data-ttu-id="5b76d-141">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5b76d-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="5b76d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5b76d-142">System.String</span></span>

### <span data-ttu-id="5b76d-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5b76d-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5b76d-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b76d-144">OUTPUTS</span></span>

### <span data-ttu-id="5b76d-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="5b76d-145">System.Object</span></span>
## <span data-ttu-id="5b76d-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b76d-146">NOTES</span></span>

## <span data-ttu-id="5b76d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b76d-147">RELATED LINKS</span></span>
