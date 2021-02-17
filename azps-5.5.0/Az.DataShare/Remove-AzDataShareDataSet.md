---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194578"
---
# <span data-ttu-id="22169-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="22169-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="22169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22169-102">SYNOPSIS</span></span>
<span data-ttu-id="22169-103">Usuwa mapowanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="22169-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="22169-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22169-104">SYNTAX</span></span>

### <span data-ttu-id="22169-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="22169-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22169-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22169-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22169-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22169-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22169-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="22169-108">DESCRIPTION</span></span>
<span data-ttu-id="22169-109">Polecenie **cmdlet Remove-AzDataShareDataSet** usuwa zestaw danych.</span><span class="sxs-lookup"><span data-stu-id="22169-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="22169-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22169-110">EXAMPLES</span></span>

### <span data-ttu-id="22169-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22169-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="22169-112">Te polecenia usuwają zestaw danych o nazwie DS z witryny WikiAds udostępniania.</span><span class="sxs-lookup"><span data-stu-id="22169-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="22169-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22169-113">PARAMETERS</span></span>

### <span data-ttu-id="22169-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22169-114">-AccountName</span></span>
<span data-ttu-id="22169-115">Nazwa konta współużytkowego danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22169-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="22169-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22169-116">-DefaultProfile</span></span>
<span data-ttu-id="22169-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="22169-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22169-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22169-118">-InputObject</span></span>
<span data-ttu-id="22169-119">Obiekt zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22169-119">The azure data set object.</span></span>


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

### <span data-ttu-id="22169-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="22169-120">-Name</span></span>
<span data-ttu-id="22169-121">Nazwa zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22169-121">Azure data set name.</span></span>

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

### <span data-ttu-id="22169-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22169-122">-PassThru</span></span>
<span data-ttu-id="22169-123">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="22169-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="22169-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22169-124">-ResourceGroupName</span></span>
<span data-ttu-id="22169-125">Nazwa grupy zasobów konta udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22169-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="22169-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22169-126">-ResourceId</span></span>
<span data-ttu-id="22169-127">Identyfikator zasobu zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22169-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="22169-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="22169-128">-ShareName</span></span>
<span data-ttu-id="22169-129">Nazwa udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22169-129">Azure data share name.</span></span>

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

### <span data-ttu-id="22169-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22169-130">-Confirm</span></span>
<span data-ttu-id="22169-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="22169-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22169-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22169-132">-WhatIf</span></span>
<span data-ttu-id="22169-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22169-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22169-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="22169-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22169-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22169-135">CommonParameters</span></span>
<span data-ttu-id="22169-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22169-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22169-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22169-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22169-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22169-138">INPUTS</span></span>

### <span data-ttu-id="22169-139">System.String</span><span class="sxs-lookup"><span data-stu-id="22169-139">System.String</span></span>

### <span data-ttu-id="22169-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="22169-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="22169-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22169-141">OUTPUTS</span></span>

### <span data-ttu-id="22169-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22169-142">System.Boolean</span></span>

## <span data-ttu-id="22169-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22169-143">NOTES</span></span>

## <span data-ttu-id="22169-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22169-144">RELATED LINKS</span></span>
