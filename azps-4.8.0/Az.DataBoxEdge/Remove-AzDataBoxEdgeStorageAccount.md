---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223151"
---
# <span data-ttu-id="6356d-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6356d-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="6356d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6356d-102">SYNOPSIS</span></span>
<span data-ttu-id="6356d-103">Usuwa konto magazynu Edge dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="6356d-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="6356d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6356d-104">SYNTAX</span></span>

### <span data-ttu-id="6356d-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6356d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6356d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6356d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6356d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6356d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6356d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6356d-108">DESCRIPTION</span></span>
<span data-ttu-id="6356d-109">Polecenie cmdlet **Remove-AzDataBoxEdgeStorageAccount** usuwa powiązane konto magazynu Edge dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="6356d-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="6356d-110">Możesz określić nazwę konta magazynu granicznego, które ma zostać usunięte jako parametr w poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6356d-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="6356d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6356d-111">EXAMPLES</span></span>

### <span data-ttu-id="6356d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6356d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="6356d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6356d-113">PARAMETERS</span></span>

### <span data-ttu-id="6356d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6356d-114">-AsJob</span></span>
<span data-ttu-id="6356d-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6356d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6356d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6356d-116">-DefaultProfile</span></span>
<span data-ttu-id="6356d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6356d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6356d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6356d-118">-DeviceName</span></span>
<span data-ttu-id="6356d-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="6356d-119">Device Name</span></span>

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

### <span data-ttu-id="6356d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6356d-120">-InputObject</span></span>
<span data-ttu-id="6356d-121">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="6356d-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6356d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6356d-122">-Name</span></span>
<span data-ttu-id="6356d-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="6356d-123">Resource Name</span></span>

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

### <span data-ttu-id="6356d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6356d-124">-PassThru</span></span>
<span data-ttu-id="6356d-125">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="6356d-125">returns true if successful</span></span>

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

### <span data-ttu-id="6356d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6356d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6356d-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6356d-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6356d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6356d-128">-ResourceId</span></span>
<span data-ttu-id="6356d-129">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6356d-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6356d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6356d-130">-Confirm</span></span>
<span data-ttu-id="6356d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6356d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6356d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6356d-132">-WhatIf</span></span>
<span data-ttu-id="6356d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6356d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6356d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6356d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6356d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6356d-135">CommonParameters</span></span>
<span data-ttu-id="6356d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6356d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6356d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6356d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6356d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6356d-138">INPUTS</span></span>

### <span data-ttu-id="6356d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6356d-139">System.String</span></span>

### <span data-ttu-id="6356d-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6356d-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="6356d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6356d-141">OUTPUTS</span></span>

### <span data-ttu-id="6356d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6356d-142">System.Boolean</span></span>

## <span data-ttu-id="6356d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6356d-143">NOTES</span></span>

## <span data-ttu-id="6356d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6356d-144">RELATED LINKS</span></span>
