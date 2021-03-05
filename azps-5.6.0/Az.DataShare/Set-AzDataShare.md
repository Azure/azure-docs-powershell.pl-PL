---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: ea159b52de0dd7d30c898f5119bc819c94d418fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966522"
---
# <span data-ttu-id="eea54-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="eea54-101">Set-AzDataShare</span></span>

## <span data-ttu-id="eea54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea54-102">SYNOPSIS</span></span>
<span data-ttu-id="eea54-103">Aktualizacje istniejącego udziału danych</span><span class="sxs-lookup"><span data-stu-id="eea54-103">Updates an existing data share</span></span>

## <span data-ttu-id="eea54-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eea54-104">SYNTAX</span></span>

### <span data-ttu-id="eea54-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="eea54-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea54-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea54-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea54-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea54-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea54-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="eea54-108">DESCRIPTION</span></span>
<span data-ttu-id="eea54-109">Polecenie **cmdlet Set-AzDataShare** aktualizuje udział danych, który istnieje w ramach określonego konta udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eea54-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="eea54-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eea54-110">EXAMPLES</span></span>

### <span data-ttu-id="eea54-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eea54-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="eea54-112">To polecenie aktualizuje istniejący udział danych o nazwie AdsShare</span><span class="sxs-lookup"><span data-stu-id="eea54-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="eea54-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eea54-113">PARAMETERS</span></span>

### <span data-ttu-id="eea54-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eea54-114">-AccountName</span></span>
<span data-ttu-id="eea54-115">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eea54-115">Azure data share account name</span></span>

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

### <span data-ttu-id="eea54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea54-116">-DefaultProfile</span></span>
<span data-ttu-id="eea54-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eea54-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea54-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="eea54-118">-Description</span></span>
<span data-ttu-id="eea54-119">Opis udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="eea54-119">Description of Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea54-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eea54-120">-InputObject</span></span>
<span data-ttu-id="eea54-121">Obiekt udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eea54-121">Azure data share object</span></span>


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

### <span data-ttu-id="eea54-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="eea54-122">-Name</span></span>
<span data-ttu-id="eea54-123">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eea54-123">Azure data share name</span></span>

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

### <span data-ttu-id="eea54-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea54-124">-ResourceGroupName</span></span>
<span data-ttu-id="eea54-125">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eea54-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="eea54-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea54-126">-ResourceId</span></span>
<span data-ttu-id="eea54-127">Identyfikator zasobu udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eea54-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="eea54-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="eea54-128">-TermsOfUse</span></span>
<span data-ttu-id="eea54-129">Warunki użytkowania udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="eea54-129">Terms of Use for Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea54-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eea54-130">-Confirm</span></span>
<span data-ttu-id="eea54-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eea54-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea54-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea54-132">-WhatIf</span></span>
<span data-ttu-id="eea54-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eea54-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eea54-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="eea54-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea54-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea54-135">CommonParameters</span></span>
<span data-ttu-id="eea54-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea54-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea54-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eea54-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea54-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eea54-138">INPUTS</span></span>

### <span data-ttu-id="eea54-139">System.String</span><span class="sxs-lookup"><span data-stu-id="eea54-139">System.String</span></span>

### <span data-ttu-id="eea54-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="eea54-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="eea54-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eea54-141">OUTPUTS</span></span>

### <span data-ttu-id="eea54-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="eea54-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="eea54-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eea54-143">NOTES</span></span>

## <span data-ttu-id="eea54-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eea54-144">RELATED LINKS</span></span>
