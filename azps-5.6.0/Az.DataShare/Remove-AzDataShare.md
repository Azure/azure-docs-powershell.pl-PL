---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964730"
---
# <span data-ttu-id="ed317-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="ed317-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="ed317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed317-102">SYNOPSIS</span></span>
<span data-ttu-id="ed317-103">Usuwa udział danych.</span><span class="sxs-lookup"><span data-stu-id="ed317-103">Removes a data share.</span></span>

## <span data-ttu-id="ed317-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed317-104">SYNTAX</span></span>

### <span data-ttu-id="ed317-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ed317-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed317-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed317-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed317-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed317-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed317-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed317-108">DESCRIPTION</span></span>
<span data-ttu-id="ed317-109">Polecenie **cmdlet Remove-AzDataShare** usuwa udział danych.</span><span class="sxs-lookup"><span data-stu-id="ed317-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="ed317-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed317-110">EXAMPLES</span></span>

### <span data-ttu-id="ed317-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed317-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="ed317-112">Te polecenia usuwają udział danych o nazwie AdsShare z witryny WikiAds konta udostępniania danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ed317-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="ed317-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed317-113">PARAMETERS</span></span>

### <span data-ttu-id="ed317-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed317-114">-AccountName</span></span>
<span data-ttu-id="ed317-115">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ed317-115">Azure data share account name</span></span>

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

### <span data-ttu-id="ed317-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ed317-116">-AsJob</span></span>
<span data-ttu-id="ed317-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="ed317-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="ed317-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed317-118">-DefaultProfile</span></span>
<span data-ttu-id="ed317-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed317-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed317-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed317-120">-InputObject</span></span>
<span data-ttu-id="ed317-121">Azure data share object' ''yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="ed317-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="ed317-122">Wymagane: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="ed317-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed317-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ed317-123">-Name</span></span>
<span data-ttu-id="ed317-124">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ed317-124">Azure data share name</span></span>

<span data-ttu-id="ed317-125">Typ yaml: Zestawy parametrów ciągu: Aliasy ByFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="ed317-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="ed317-126">Wymagane: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="ed317-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="ed317-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed317-127">-PassThru</span></span>
<span data-ttu-id="ed317-128">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="ed317-128">Return object (if specified).</span></span>

<span data-ttu-id="ed317-129">typ yaml: Zestawy parametrów SwitchParameters: (Wszystkie) aliasy:</span><span class="sxs-lookup"><span data-stu-id="ed317-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="ed317-130">Wymagane: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="ed317-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="ed317-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed317-131">-ResourceGroupName</span></span>
<span data-ttu-id="ed317-132">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ed317-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="ed317-133">Typ yaml: Zestawy parametrów ciągu: Aliasy ByFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="ed317-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="ed317-134">Wymagane: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="ed317-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="ed317-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed317-135">-ResourceId</span></span>
<span data-ttu-id="ed317-136">Identyfikator zasobu udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ed317-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="ed317-137">Typ yaml: Zestawy parametrów ciągu: ByResourceIdParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="ed317-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="ed317-138">Wymagane: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="ed317-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="ed317-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed317-139">-Confirm</span></span>
<span data-ttu-id="ed317-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ed317-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="ed317-141">typ yaml: SwitchParameters zestawy parametrów: (Wszystkie) aliasy: cf</span><span class="sxs-lookup"><span data-stu-id="ed317-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="ed317-142">Wymagane: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="ed317-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="ed317-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed317-143">-WhatIf</span></span>
<span data-ttu-id="ed317-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed317-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed317-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ed317-145">The cmdlet is not run.</span></span>

<span data-ttu-id="ed317-146">typ yaml: SwitchParameters zestawy parametrów: (Wszystkie) aliasy: wi</span><span class="sxs-lookup"><span data-stu-id="ed317-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="ed317-147">Wymagane: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="ed317-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="ed317-148">Typ yaml: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="ed317-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="ed317-149">Wymagane: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="ed317-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="ed317-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed317-150">CommonParameters</span></span>
<span data-ttu-id="ed317-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed317-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed317-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed317-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed317-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed317-153">INPUTS</span></span>

### <span data-ttu-id="ed317-154">System.String</span><span class="sxs-lookup"><span data-stu-id="ed317-154">System.String</span></span>

### <span data-ttu-id="ed317-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ed317-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ed317-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed317-156">OUTPUTS</span></span>

### <span data-ttu-id="ed317-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed317-157">System.Boolean</span></span>

## <span data-ttu-id="ed317-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed317-158">NOTES</span></span>

## <span data-ttu-id="ed317-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed317-159">RELATED LINKS</span></span>
