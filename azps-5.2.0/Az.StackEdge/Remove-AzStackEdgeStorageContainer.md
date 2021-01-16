---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350017"
---
# <span data-ttu-id="a7a02-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7a02-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="a7a02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7a02-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a02-103">Usuwa kontener magazynu dla konta magazynu Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="a7a02-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="a7a02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7a02-104">SYNTAX</span></span>

### <span data-ttu-id="a7a02-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a7a02-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7a02-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7a02-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7a02-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7a02-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a02-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a7a02-108">DESCRIPTION</span></span>
<span data-ttu-id="a7a02-109">Polecenie cmdlet **Remove-AzStackEdgeStorageContainer** usuwa skojarzony kontener magazynu dla konta magazynu Edge na urządzeniu z krawędziami stosu.</span><span class="sxs-lookup"><span data-stu-id="a7a02-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="a7a02-110">Możesz określić nazwę kontenera magazynu, który ma zostać usunięty jako parametr.</span><span class="sxs-lookup"><span data-stu-id="a7a02-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="a7a02-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7a02-111">EXAMPLES</span></span>

### <span data-ttu-id="a7a02-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7a02-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="a7a02-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7a02-113">PARAMETERS</span></span>

### <span data-ttu-id="a7a02-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7a02-114">-AsJob</span></span>
<span data-ttu-id="a7a02-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a7a02-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7a02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a02-116">-DefaultProfile</span></span>
<span data-ttu-id="a7a02-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a02-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7a02-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a7a02-118">-DeviceName</span></span>
<span data-ttu-id="a7a02-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="a7a02-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a02-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a7a02-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="a7a02-121">Podaj nazwę istniejącego EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7a02-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a02-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7a02-122">-InputObject</span></span>
<span data-ttu-id="a7a02-123">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="a7a02-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a02-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a7a02-124">-Name</span></span>
<span data-ttu-id="a7a02-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="a7a02-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a02-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7a02-126">-PassThru</span></span>
<span data-ttu-id="a7a02-127">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="a7a02-127">returns true if successful</span></span>

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

### <span data-ttu-id="a7a02-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a02-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7a02-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a7a02-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a02-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7a02-130">-ResourceId</span></span>
<span data-ttu-id="a7a02-131">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a7a02-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a02-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7a02-132">-Confirm</span></span>
<span data-ttu-id="a7a02-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7a02-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a02-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a02-134">-WhatIf</span></span>
<span data-ttu-id="a7a02-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7a02-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7a02-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a7a02-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a02-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a02-137">CommonParameters</span></span>
<span data-ttu-id="a7a02-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7a02-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a02-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7a02-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a02-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7a02-140">INPUTS</span></span>

### <span data-ttu-id="a7a02-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a02-141">System.String</span></span>

### <span data-ttu-id="a7a02-142">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7a02-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="a7a02-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7a02-143">OUTPUTS</span></span>

### <span data-ttu-id="a7a02-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7a02-144">System.Boolean</span></span>

## <span data-ttu-id="a7a02-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7a02-145">NOTES</span></span>

## <span data-ttu-id="a7a02-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7a02-146">RELATED LINKS</span></span>
