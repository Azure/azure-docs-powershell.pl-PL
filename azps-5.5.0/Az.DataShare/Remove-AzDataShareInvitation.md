---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194570"
---
# <span data-ttu-id="c0ea6-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="c0ea6-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="c0ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ea6-103">Usuwa zaproszenie</span><span class="sxs-lookup"><span data-stu-id="c0ea6-103">removes an invitation</span></span>

## <span data-ttu-id="c0ea6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0ea6-104">SYNTAX</span></span>

### <span data-ttu-id="c0ea6-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c0ea6-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0ea6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0ea6-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0ea6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0ea6-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0ea6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0ea6-108">DESCRIPTION</span></span>
<span data-ttu-id="c0ea6-109">Polecenie **cmdlet Remove-AzDataShareInvitation** usuwa zaproszenie do udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="c0ea6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0ea6-110">EXAMPLES</span></span>

### <span data-ttu-id="c0ea6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0ea6-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c0ea6-112">Te polecenia usuwają zaproszenie o nazwie ADSInvite z usługi Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="c0ea6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0ea6-113">PARAMETERS</span></span>

### <span data-ttu-id="c0ea6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0ea6-114">-AccountName</span></span>
<span data-ttu-id="c0ea6-115">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c0ea6-115">Azure data share account name</span></span>

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

### <span data-ttu-id="c0ea6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ea6-116">-DefaultProfile</span></span>
<span data-ttu-id="c0ea6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ea6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0ea6-118">-InputObject</span></span>
<span data-ttu-id="c0ea6-119">Obiekt zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c0ea6-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ea6-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0ea6-120">-Name</span></span>
<span data-ttu-id="c0ea6-121">Nazwa zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c0ea6-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="c0ea6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0ea6-122">-PassThru</span></span>
<span data-ttu-id="c0ea6-123">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="c0ea6-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="c0ea6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ea6-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0ea6-125">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="c0ea6-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c0ea6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0ea6-126">-ResourceId</span></span>
<span data-ttu-id="c0ea6-127">Identyfikator zasobu zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c0ea6-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="c0ea6-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c0ea6-128">-ShareName</span></span>
<span data-ttu-id="c0ea6-129">Nazwa udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-129">Azure data share name.</span></span>

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

### <span data-ttu-id="c0ea6-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0ea6-130">-Confirm</span></span>
<span data-ttu-id="c0ea6-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0ea6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0ea6-132">-WhatIf</span></span>
<span data-ttu-id="c0ea6-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0ea6-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0ea6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ea6-135">CommonParameters</span></span>
<span data-ttu-id="c0ea6-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ea6-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0ea6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ea6-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0ea6-138">INPUTS</span></span>

### <span data-ttu-id="c0ea6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c0ea6-139">System.String</span></span>

### <span data-ttu-id="c0ea6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="c0ea6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="c0ea6-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0ea6-141">OUTPUTS</span></span>

### <span data-ttu-id="c0ea6-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0ea6-142">System.Boolean</span></span>

## <span data-ttu-id="c0ea6-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0ea6-143">NOTES</span></span>

## <span data-ttu-id="c0ea6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0ea6-144">RELATED LINKS</span></span>
