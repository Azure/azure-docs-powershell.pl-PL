---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3cf8532871ce2f011eb7174118d80a7aee11a583
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891577"
---
# <span data-ttu-id="79b5d-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="79b5d-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="79b5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="79b5d-103">Usuwa kontener magazynu dla konta magazynu Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="79b5d-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="79b5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79b5d-104">SYNTAX</span></span>

### <span data-ttu-id="79b5d-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79b5d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b5d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79b5d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b5d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79b5d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b5d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="79b5d-108">DESCRIPTION</span></span>
<span data-ttu-id="79b5d-109">Polecenie cmdlet **Remove-AzDataBoxEdgeStorageContainer** usuwa skojarzony kontener magazynu dla konta magazynu Edge na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="79b5d-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="79b5d-110">Możesz określić nazwę kontenera magazynu, który ma zostać usunięty jako parametr.</span><span class="sxs-lookup"><span data-stu-id="79b5d-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="79b5d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79b5d-111">EXAMPLES</span></span>

### <span data-ttu-id="79b5d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79b5d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="79b5d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79b5d-113">PARAMETERS</span></span>

### <span data-ttu-id="79b5d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79b5d-114">-AsJob</span></span>
<span data-ttu-id="79b5d-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="79b5d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79b5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b5d-116">-DefaultProfile</span></span>
<span data-ttu-id="79b5d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79b5d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79b5d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="79b5d-118">-DeviceName</span></span>
<span data-ttu-id="79b5d-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="79b5d-119">Device Name</span></span>

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

### <span data-ttu-id="79b5d-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="79b5d-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="79b5d-121">Podaj nazwę istniejącego EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="79b5d-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="79b5d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="79b5d-122">-InputObject</span></span>
<span data-ttu-id="79b5d-123">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="79b5d-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79b5d-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79b5d-124">-Name</span></span>
<span data-ttu-id="79b5d-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="79b5d-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b5d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79b5d-126">-PassThru</span></span>
<span data-ttu-id="79b5d-127">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="79b5d-127">returns true if successful</span></span>

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

### <span data-ttu-id="79b5d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b5d-128">-ResourceGroupName</span></span>
<span data-ttu-id="79b5d-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="79b5d-129">Resource Group Name</span></span>

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

### <span data-ttu-id="79b5d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79b5d-130">-ResourceId</span></span>
<span data-ttu-id="79b5d-131">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="79b5d-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="79b5d-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79b5d-132">-Confirm</span></span>
<span data-ttu-id="79b5d-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b5d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b5d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b5d-134">-WhatIf</span></span>
<span data-ttu-id="79b5d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b5d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79b5d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79b5d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b5d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b5d-137">CommonParameters</span></span>
<span data-ttu-id="79b5d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b5d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b5d-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79b5d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b5d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79b5d-140">INPUTS</span></span>

### <span data-ttu-id="79b5d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="79b5d-141">System.String</span></span>

### <span data-ttu-id="79b5d-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="79b5d-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="79b5d-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79b5d-143">OUTPUTS</span></span>

### <span data-ttu-id="79b5d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79b5d-144">System.Boolean</span></span>

## <span data-ttu-id="79b5d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79b5d-145">NOTES</span></span>

## <span data-ttu-id="79b5d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79b5d-146">RELATED LINKS</span></span>
