---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360493"
---
# <span data-ttu-id="6cb29-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6cb29-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="6cb29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6cb29-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb29-103">Wywołuje określone akcje w kontenerze magazynu.</span><span class="sxs-lookup"><span data-stu-id="6cb29-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="6cb29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6cb29-104">SYNTAX</span></span>

### <span data-ttu-id="6cb29-105">InvokeByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6cb29-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb29-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cb29-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb29-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cb29-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cb29-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6cb29-108">DESCRIPTION</span></span>
<span data-ttu-id="6cb29-109">Polecenie cmdlet **Invoke-AzDataBoxEdgeStorageContainer** wywołuje akcje umożliwiające odświeżenie danych w kontenerze magazynu na urządzeniu z krawędziami pola danych.</span><span class="sxs-lookup"><span data-stu-id="6cb29-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="6cb29-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6cb29-110">EXAMPLES</span></span>

### <span data-ttu-id="6cb29-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6cb29-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="6cb29-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6cb29-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="6cb29-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6cb29-113">PARAMETERS</span></span>

### <span data-ttu-id="6cb29-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cb29-114">-AsJob</span></span>
<span data-ttu-id="6cb29-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6cb29-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cb29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb29-116">-DefaultProfile</span></span>
<span data-ttu-id="6cb29-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb29-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cb29-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6cb29-118">-DeviceName</span></span>
<span data-ttu-id="6cb29-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="6cb29-119">Device Name</span></span>

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

### <span data-ttu-id="6cb29-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6cb29-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="6cb29-121">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="6cb29-121">Resource Name</span></span>

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

### <span data-ttu-id="6cb29-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6cb29-122">-InputObject</span></span>
<span data-ttu-id="6cb29-123">Dostarczenie istniejącego obiektu EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6cb29-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb29-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6cb29-124">-Name</span></span>
<span data-ttu-id="6cb29-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="6cb29-125">Resource Name</span></span>

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

### <span data-ttu-id="6cb29-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cb29-126">-PassThru</span></span>
<span data-ttu-id="6cb29-127">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="6cb29-127">returns true if successful</span></span>

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

### <span data-ttu-id="6cb29-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="6cb29-128">-RefreshData</span></span>
<span data-ttu-id="6cb29-129">Odświeżanie metadanych kontenera przy użyciu danych z chmury</span><span class="sxs-lookup"><span data-stu-id="6cb29-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="6cb29-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb29-130">-ResourceGroupName</span></span>
<span data-ttu-id="6cb29-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6cb29-131">Resource Group Name</span></span>

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

### <span data-ttu-id="6cb29-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cb29-132">-ResourceId</span></span>
<span data-ttu-id="6cb29-133">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6cb29-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="6cb29-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6cb29-134">-Confirm</span></span>
<span data-ttu-id="6cb29-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cb29-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb29-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb29-136">-WhatIf</span></span>
<span data-ttu-id="6cb29-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cb29-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cb29-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6cb29-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb29-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb29-139">CommonParameters</span></span>
<span data-ttu-id="6cb29-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb29-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb29-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cb29-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb29-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cb29-142">INPUTS</span></span>

### <span data-ttu-id="6cb29-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6cb29-143">System.String</span></span>

### <span data-ttu-id="6cb29-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6cb29-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="6cb29-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6cb29-145">OUTPUTS</span></span>

### <span data-ttu-id="6cb29-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6cb29-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="6cb29-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6cb29-147">NOTES</span></span>

## <span data-ttu-id="6cb29-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cb29-148">RELATED LINKS</span></span>
