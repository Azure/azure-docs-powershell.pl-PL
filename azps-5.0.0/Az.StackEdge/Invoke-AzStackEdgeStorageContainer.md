---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: d7e8c65a54adae1de7b7f3ba1ed2d67139638846
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307825"
---
# <span data-ttu-id="55f61-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="55f61-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="55f61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55f61-102">SYNOPSIS</span></span>
<span data-ttu-id="55f61-103">Wywołuje określone akcje w kontenerze magazynu.</span><span class="sxs-lookup"><span data-stu-id="55f61-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="55f61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55f61-104">SYNTAX</span></span>

### <span data-ttu-id="55f61-105">InvokeByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="55f61-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f61-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f61-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f61-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f61-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f61-108">Opis</span><span class="sxs-lookup"><span data-stu-id="55f61-108">DESCRIPTION</span></span>
<span data-ttu-id="55f61-109">Polecenie cmdlet **Invoke-AzStackEdgeStorageContainer** wywołuje akcje umożliwiające odświeżenie danych w kontenerze magazynu na urządzeniu z krawędziami stosu.</span><span class="sxs-lookup"><span data-stu-id="55f61-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="55f61-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55f61-110">EXAMPLES</span></span>

### <span data-ttu-id="55f61-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="55f61-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="55f61-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="55f61-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="55f61-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55f61-113">PARAMETERS</span></span>

### <span data-ttu-id="55f61-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55f61-114">-AsJob</span></span>
<span data-ttu-id="55f61-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="55f61-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55f61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f61-116">-DefaultProfile</span></span>
<span data-ttu-id="55f61-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55f61-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55f61-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="55f61-118">-DeviceName</span></span>
<span data-ttu-id="55f61-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="55f61-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f61-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="55f61-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="55f61-121">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="55f61-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f61-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55f61-122">-InputObject</span></span>
<span data-ttu-id="55f61-123">Dostarczenie istniejącego obiektu EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="55f61-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55f61-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55f61-124">-Name</span></span>
<span data-ttu-id="55f61-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="55f61-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f61-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55f61-126">-PassThru</span></span>
<span data-ttu-id="55f61-127">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="55f61-127">returns true if successful</span></span>

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

### <span data-ttu-id="55f61-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="55f61-128">-RefreshData</span></span>
<span data-ttu-id="55f61-129">Odświeżanie metadanych kontenera przy użyciu danych z chmury</span><span class="sxs-lookup"><span data-stu-id="55f61-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="55f61-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f61-130">-ResourceGroupName</span></span>
<span data-ttu-id="55f61-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="55f61-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f61-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55f61-132">-ResourceId</span></span>
<span data-ttu-id="55f61-133">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="55f61-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f61-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55f61-134">-Confirm</span></span>
<span data-ttu-id="55f61-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f61-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f61-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f61-136">-WhatIf</span></span>
<span data-ttu-id="55f61-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f61-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55f61-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="55f61-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f61-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f61-139">CommonParameters</span></span>
<span data-ttu-id="55f61-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55f61-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f61-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55f61-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f61-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55f61-142">INPUTS</span></span>

### <span data-ttu-id="55f61-143">System. String</span><span class="sxs-lookup"><span data-stu-id="55f61-143">System.String</span></span>

### <span data-ttu-id="55f61-144">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="55f61-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="55f61-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55f61-145">OUTPUTS</span></span>

### <span data-ttu-id="55f61-146">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="55f61-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="55f61-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55f61-147">NOTES</span></span>

## <span data-ttu-id="55f61-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55f61-148">RELATED LINKS</span></span>
