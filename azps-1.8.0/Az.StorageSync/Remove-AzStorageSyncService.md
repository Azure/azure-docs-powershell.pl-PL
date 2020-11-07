---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 5116ead7111902b1009517ff42ff6594ac87d8c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707441"
---
# <span data-ttu-id="4d1e9-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="4d1e9-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="4d1e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1e9-103">To polecenie spowoduje usunięcie określonej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="4d1e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d1e9-104">SYNTAX</span></span>

### <span data-ttu-id="4d1e9-105">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4d1e9-105">InputObjectParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d1e9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d1e9-106">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d1e9-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d1e9-107">StringParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d1e9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4d1e9-108">DESCRIPTION</span></span>
<span data-ttu-id="4d1e9-109">To polecenie spowoduje usunięcie określonej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="4d1e9-110">Usługę synchronizacji magazynu można usunąć tylko wtedy, gdy wszystkie zawarte w niej grupy synchronizacji i zarejestrowane serwery zostaną usunięte jako pierwsze.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="4d1e9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d1e9-111">EXAMPLES</span></span>

### <span data-ttu-id="4d1e9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d1e9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="4d1e9-113">To polecenie spowoduje usunięcie usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="4d1e9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d1e9-114">PARAMETERS</span></span>

### <span data-ttu-id="4d1e9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d1e9-115">-AsJob</span></span>
<span data-ttu-id="4d1e9-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4d1e9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d1e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1e9-117">-DefaultProfile</span></span>
<span data-ttu-id="4d1e9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d1e9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4d1e9-119">-Force</span></span>
<span data-ttu-id="4d1e9-120">Dostawa — Wymuś pominięcie potwierdzenia tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="4d1e9-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4d1e9-121">-InputObject</span></span>
<span data-ttu-id="4d1e9-122">Obiekt wejściowy StorageSyncService, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4d1e9-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d1e9-123">-Name</span></span>
<span data-ttu-id="4d1e9-124">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4d1e9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d1e9-125">-PassThru</span></span>
<span data-ttu-id="4d1e9-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4d1e9-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4d1e9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d1e9-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d1e9-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="4d1e9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d1e9-129">-ResourceId</span></span>
<span data-ttu-id="4d1e9-130">Identyfikator zasobu StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="4d1e9-130">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="4d1e9-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d1e9-131">-Confirm</span></span>
<span data-ttu-id="4d1e9-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-132">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d1e9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1e9-133">-WhatIf</span></span>
<span data-ttu-id="4d1e9-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d1e9-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d1e9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1e9-136">CommonParameters</span></span>
<span data-ttu-id="4d1e9-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1e9-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1e9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1e9-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d1e9-139">INPUTS</span></span>

### <span data-ttu-id="4d1e9-140">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="4d1e9-140">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="4d1e9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4d1e9-141">System.String</span></span>

### <span data-ttu-id="4d1e9-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d1e9-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4d1e9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d1e9-143">OUTPUTS</span></span>

### <span data-ttu-id="4d1e9-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="4d1e9-144">System.Object</span></span>
## <span data-ttu-id="4d1e9-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d1e9-145">NOTES</span></span>

## <span data-ttu-id="4d1e9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d1e9-146">RELATED LINKS</span></span>
