---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180826"
---
# <span data-ttu-id="49b8f-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="49b8f-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="49b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="49b8f-103">Usuwa konto udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="49b8f-103">Removes a datashare account</span></span>

## <span data-ttu-id="49b8f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49b8f-104">SYNTAX</span></span>

### <span data-ttu-id="49b8f-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="49b8f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49b8f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b8f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49b8f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b8f-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49b8f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="49b8f-108">DESCRIPTION</span></span>
<span data-ttu-id="49b8f-109">Polecenie **cmdlet Remove-AzDataShareAccount** usuwa konto udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="49b8f-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="49b8f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49b8f-110">EXAMPLES</span></span>

### <span data-ttu-id="49b8f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49b8f-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="49b8f-112">To polecenie usuwa konto udostępniania danych o nazwie WikiADS z grupy zasobów o nazwie ADS.</span><span class="sxs-lookup"><span data-stu-id="49b8f-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="49b8f-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="49b8f-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="49b8f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49b8f-114">PARAMETERS</span></span>

### <span data-ttu-id="49b8f-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="49b8f-115">-AsJob</span></span>
<span data-ttu-id="49b8f-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="49b8f-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="49b8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b8f-117">-DefaultProfile</span></span>
<span data-ttu-id="49b8f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49b8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b8f-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="49b8f-119">-Force</span></span>
<span data-ttu-id="49b8f-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="49b8f-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="49b8f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49b8f-121">-InputObject</span></span>
<span data-ttu-id="49b8f-122">Obiekt konta współużytkuje dane platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="49b8f-122">The azure data share account object.</span></span>


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

### <span data-ttu-id="49b8f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49b8f-123">-Name</span></span>
<span data-ttu-id="49b8f-124">Nazwa konta współużytkowego danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="49b8f-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="49b8f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49b8f-125">-PassThru</span></span>
<span data-ttu-id="49b8f-126">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="49b8f-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="49b8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="49b8f-128">Nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="49b8f-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="49b8f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49b8f-129">-ResourceId</span></span>
<span data-ttu-id="49b8f-130">Identyfikator zasobu konta udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="49b8f-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="49b8f-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49b8f-131">-Confirm</span></span>
<span data-ttu-id="49b8f-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49b8f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49b8f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b8f-133">-WhatIf</span></span>
<span data-ttu-id="49b8f-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49b8f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49b8f-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49b8f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49b8f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b8f-136">CommonParameters</span></span>
<span data-ttu-id="49b8f-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b8f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b8f-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49b8f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b8f-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49b8f-139">INPUTS</span></span>

### <span data-ttu-id="49b8f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="49b8f-140">System.String</span></span>

### <span data-ttu-id="49b8f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="49b8f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="49b8f-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49b8f-142">OUTPUTS</span></span>

### <span data-ttu-id="49b8f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49b8f-143">System.Boolean</span></span>

## <span data-ttu-id="49b8f-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49b8f-144">NOTES</span></span>

## <span data-ttu-id="49b8f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49b8f-145">RELATED LINKS</span></span>
