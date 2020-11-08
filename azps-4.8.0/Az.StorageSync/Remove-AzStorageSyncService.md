---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061968"
---
# <span data-ttu-id="36f12-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="36f12-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="36f12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36f12-102">SYNOPSIS</span></span>
<span data-ttu-id="36f12-103">To polecenie spowoduje usunięcie określonej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="36f12-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="36f12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36f12-104">SYNTAX</span></span>

### <span data-ttu-id="36f12-105">StringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="36f12-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36f12-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36f12-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36f12-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36f12-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36f12-108">Opis</span><span class="sxs-lookup"><span data-stu-id="36f12-108">DESCRIPTION</span></span>
<span data-ttu-id="36f12-109">To polecenie spowoduje usunięcie określonej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="36f12-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="36f12-110">Usługę synchronizacji magazynu można usunąć tylko wtedy, gdy wszystkie zawarte w niej grupy synchronizacji i zarejestrowane serwery zostaną usunięte jako pierwsze.</span><span class="sxs-lookup"><span data-stu-id="36f12-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="36f12-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36f12-111">EXAMPLES</span></span>

### <span data-ttu-id="36f12-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36f12-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="36f12-113">To polecenie spowoduje usunięcie usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="36f12-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="36f12-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36f12-114">PARAMETERS</span></span>

### <span data-ttu-id="36f12-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36f12-115">-AsJob</span></span>
<span data-ttu-id="36f12-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="36f12-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36f12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f12-117">-DefaultProfile</span></span>
<span data-ttu-id="36f12-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36f12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f12-119">-Force</span><span class="sxs-lookup"><span data-stu-id="36f12-119">-Force</span></span>
<span data-ttu-id="36f12-120">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="36f12-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="36f12-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36f12-121">-InputObject</span></span>
<span data-ttu-id="36f12-122">Obiekt wejściowy StorageSyncService, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="36f12-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="36f12-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36f12-123">-Name</span></span>
<span data-ttu-id="36f12-124">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="36f12-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="36f12-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36f12-125">-PassThru</span></span>
<span data-ttu-id="36f12-126">W przypadku normalnego wykonywania to polecenie cmdlet nie zwraca żadnej wartości po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="36f12-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="36f12-127">Jeśli podasz parametr PassThru, polecenie cmdlet nastąpi wartość do rurociągu po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="36f12-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="36f12-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f12-128">-ResourceGroupName</span></span>
<span data-ttu-id="36f12-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36f12-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="36f12-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36f12-130">-ResourceId</span></span>
<span data-ttu-id="36f12-131">Identyfikator zasobu StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="36f12-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="36f12-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36f12-132">-Confirm</span></span>
<span data-ttu-id="36f12-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36f12-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f12-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f12-134">-WhatIf</span></span>
<span data-ttu-id="36f12-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36f12-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36f12-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36f12-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f12-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f12-137">CommonParameters</span></span>
<span data-ttu-id="36f12-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f12-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f12-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f12-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f12-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36f12-140">INPUTS</span></span>

### <span data-ttu-id="36f12-141">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="36f12-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="36f12-142">System. String</span><span class="sxs-lookup"><span data-stu-id="36f12-142">System.String</span></span>

### <span data-ttu-id="36f12-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36f12-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36f12-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36f12-144">OUTPUTS</span></span>

### <span data-ttu-id="36f12-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="36f12-145">System.Object</span></span>
## <span data-ttu-id="36f12-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36f12-146">NOTES</span></span>

## <span data-ttu-id="36f12-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36f12-147">RELATED LINKS</span></span>
