---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355258"
---
# <span data-ttu-id="bcb2e-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bcb2e-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="bcb2e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bcb2e-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb2e-103">usuwa zaproszenie.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-103">removes an invitation</span></span>

## <span data-ttu-id="bcb2e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bcb2e-104">SYNTAX</span></span>

### <span data-ttu-id="bcb2e-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bcb2e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcb2e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcb2e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcb2e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcb2e-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcb2e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bcb2e-108">DESCRIPTION</span></span>
<span data-ttu-id="bcb2e-109">Polecenie cmdlet **Remove-AzDataShareInvitation** umożliwia usunięcie zaproszenia do udostępniania.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="bcb2e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bcb2e-110">EXAMPLES</span></span>

### <span data-ttu-id="bcb2e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bcb2e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="bcb2e-112">To polecenie usuwa zaproszenie o nazwie ADSInvite z AdsShare udostępniania.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="bcb2e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bcb2e-113">PARAMETERS</span></span>

### <span data-ttu-id="bcb2e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bcb2e-114">-AccountName</span></span>
<span data-ttu-id="bcb2e-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="bcb2e-115">Azure data share account name</span></span>

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

### <span data-ttu-id="bcb2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb2e-116">-DefaultProfile</span></span>
<span data-ttu-id="bcb2e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcb2e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bcb2e-118">-InputObject</span></span>
<span data-ttu-id="bcb2e-119">Obiekt zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bcb2e-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="bcb2e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bcb2e-120">-Name</span></span>
<span data-ttu-id="bcb2e-121">Nazwa zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bcb2e-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="bcb2e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcb2e-122">-PassThru</span></span>
<span data-ttu-id="bcb2e-123">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="bcb2e-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="bcb2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="bcb2e-125">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="bcb2e-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bcb2e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcb2e-126">-ResourceId</span></span>
<span data-ttu-id="bcb2e-127">Identyfikator zasobu zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bcb2e-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="bcb2e-128">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="bcb2e-128">-ShareName</span></span>
<span data-ttu-id="bcb2e-129">Nazwa udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-129">Azure data share name.</span></span>

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

### <span data-ttu-id="bcb2e-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bcb2e-130">-Confirm</span></span>
<span data-ttu-id="bcb2e-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcb2e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb2e-132">-WhatIf</span></span>
<span data-ttu-id="bcb2e-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb2e-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcb2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb2e-135">CommonParameters</span></span>
<span data-ttu-id="bcb2e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb2e-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcb2e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb2e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcb2e-138">INPUTS</span></span>

### <span data-ttu-id="bcb2e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bcb2e-139">System.String</span></span>

### <span data-ttu-id="bcb2e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bcb2e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="bcb2e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bcb2e-141">OUTPUTS</span></span>

### <span data-ttu-id="bcb2e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bcb2e-142">System.Boolean</span></span>

## <span data-ttu-id="bcb2e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bcb2e-143">NOTES</span></span>

## <span data-ttu-id="bcb2e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcb2e-144">RELATED LINKS</span></span>
