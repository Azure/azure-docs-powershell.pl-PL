---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 74651ea4a9a108db9cc3f666ad6f78f494fcd676
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971121"
---
# <span data-ttu-id="9b3b4-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="9b3b4-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="9b3b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3b4-103">Usuwa konto udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="9b3b4-103">Removes a datashare account</span></span>

## <span data-ttu-id="9b3b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b3b4-104">SYNTAX</span></span>

### <span data-ttu-id="9b3b4-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9b3b4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3b4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b3b4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3b4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b3b4-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b3b4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b3b4-108">DESCRIPTION</span></span>
<span data-ttu-id="9b3b4-109">Polecenie **cmdlet Remove-AzDataShareAccount** usuwa konto udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="9b3b4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b3b4-110">EXAMPLES</span></span>

### <span data-ttu-id="9b3b4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b3b4-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="9b3b4-112">To polecenie usuwa konto udostępniania danych o nazwie WikiADS z grupy zasobów o nazwie ADS.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="9b3b4-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="9b3b4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b3b4-114">PARAMETERS</span></span>

### <span data-ttu-id="9b3b4-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9b3b4-115">-AsJob</span></span>
<span data-ttu-id="9b3b4-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="9b3b4-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="9b3b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3b4-117">-DefaultProfile</span></span>
<span data-ttu-id="9b3b4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3b4-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9b3b4-119">-Force</span></span>
<span data-ttu-id="9b3b4-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="9b3b4-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="9b3b4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b3b4-121">-InputObject</span></span>
<span data-ttu-id="9b3b4-122">Obiekt konta współużytkowego usługi Azure Data.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b3b4-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9b3b4-123">-Name</span></span>
<span data-ttu-id="9b3b4-124">Nazwa konta współużytkowego danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="9b3b4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b3b4-125">-PassThru</span></span>
<span data-ttu-id="9b3b4-126">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="9b3b4-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="9b3b4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b3b4-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b3b4-128">Nazwa grupy zasobów konta współużytkowania danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="9b3b4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b3b4-129">-ResourceId</span></span>
<span data-ttu-id="9b3b4-130">Identyfikator zasobu konta udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="9b3b4-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b3b4-131">-Confirm</span></span>
<span data-ttu-id="9b3b4-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b3b4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b3b4-133">-WhatIf</span></span>
<span data-ttu-id="9b3b4-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b3b4-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b3b4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3b4-136">CommonParameters</span></span>
<span data-ttu-id="9b3b4-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b3b4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3b4-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b3b4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3b4-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b3b4-139">INPUTS</span></span>

### <span data-ttu-id="9b3b4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9b3b4-140">System.String</span></span>

### <span data-ttu-id="9b3b4-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="9b3b4-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="9b3b4-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b3b4-142">OUTPUTS</span></span>

### <span data-ttu-id="9b3b4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b3b4-143">System.Boolean</span></span>

## <span data-ttu-id="9b3b4-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b3b4-144">NOTES</span></span>

## <span data-ttu-id="9b3b4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b3b4-145">RELATED LINKS</span></span>
