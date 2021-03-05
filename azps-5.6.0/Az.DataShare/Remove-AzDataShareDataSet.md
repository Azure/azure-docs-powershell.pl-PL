---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 8ede4fe94eccd9d9f08977a0af9cc8847e4aca1f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004234"
---
# <span data-ttu-id="11c8a-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="11c8a-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="11c8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="11c8a-103">Usuwa mapowanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="11c8a-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="11c8a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11c8a-104">SYNTAX</span></span>

### <span data-ttu-id="11c8a-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="11c8a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11c8a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c8a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11c8a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c8a-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c8a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="11c8a-108">DESCRIPTION</span></span>
<span data-ttu-id="11c8a-109">Polecenie **cmdlet Remove-AzDataShareDataSet** usuwa zestaw danych.</span><span class="sxs-lookup"><span data-stu-id="11c8a-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="11c8a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11c8a-110">EXAMPLES</span></span>

### <span data-ttu-id="11c8a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11c8a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="11c8a-112">Te polecenia usuwają zestaw danych o nazwie DS z witryny WikiAds udostępniania.</span><span class="sxs-lookup"><span data-stu-id="11c8a-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="11c8a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11c8a-113">PARAMETERS</span></span>

### <span data-ttu-id="11c8a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11c8a-114">-AccountName</span></span>
<span data-ttu-id="11c8a-115">Nazwa konta współużytkowego danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11c8a-115">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c8a-116">-DefaultProfile</span></span>
<span data-ttu-id="11c8a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11c8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11c8a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11c8a-118">-InputObject</span></span>
<span data-ttu-id="11c8a-119">Obiekt zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11c8a-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11c8a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11c8a-120">-Name</span></span>
<span data-ttu-id="11c8a-121">Nazwa zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11c8a-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c8a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11c8a-122">-PassThru</span></span>
<span data-ttu-id="11c8a-123">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="11c8a-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="11c8a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c8a-124">-ResourceGroupName</span></span>
<span data-ttu-id="11c8a-125">Nazwa grupy zasobów konta udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11c8a-125">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c8a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11c8a-126">-ResourceId</span></span>
<span data-ttu-id="11c8a-127">Identyfikator zasobu zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11c8a-127">The resource id of the azure data set.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c8a-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="11c8a-128">-ShareName</span></span>
<span data-ttu-id="11c8a-129">Nazwa udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11c8a-129">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c8a-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11c8a-130">-Confirm</span></span>
<span data-ttu-id="11c8a-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11c8a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c8a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c8a-132">-WhatIf</span></span>
<span data-ttu-id="11c8a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11c8a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11c8a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11c8a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c8a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c8a-135">CommonParameters</span></span>
<span data-ttu-id="11c8a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c8a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c8a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11c8a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c8a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11c8a-138">INPUTS</span></span>

### <span data-ttu-id="11c8a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="11c8a-139">System.String</span></span>

### <span data-ttu-id="11c8a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="11c8a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="11c8a-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11c8a-141">OUTPUTS</span></span>

### <span data-ttu-id="11c8a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11c8a-142">System.Boolean</span></span>

## <span data-ttu-id="11c8a-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11c8a-143">NOTES</span></span>

## <span data-ttu-id="11c8a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11c8a-144">RELATED LINKS</span></span>
