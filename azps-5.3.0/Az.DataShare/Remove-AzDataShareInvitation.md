---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377111"
---
# <span data-ttu-id="d15dd-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="d15dd-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="d15dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d15dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d15dd-103">usuwa zaproszenie.</span><span class="sxs-lookup"><span data-stu-id="d15dd-103">removes an invitation</span></span>

## <span data-ttu-id="d15dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d15dd-104">SYNTAX</span></span>

### <span data-ttu-id="d15dd-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d15dd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d15dd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d15dd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d15dd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d15dd-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d15dd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d15dd-108">DESCRIPTION</span></span>
<span data-ttu-id="d15dd-109">Polecenie cmdlet **Remove-AzDataShareInvitation** umożliwia usunięcie zaproszenia do udostępniania.</span><span class="sxs-lookup"><span data-stu-id="d15dd-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="d15dd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d15dd-110">EXAMPLES</span></span>

### <span data-ttu-id="d15dd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d15dd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d15dd-112">To polecenie usuwa zaproszenie o nazwie ADSInvite z AdsShare udostępniania.</span><span class="sxs-lookup"><span data-stu-id="d15dd-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="d15dd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d15dd-113">PARAMETERS</span></span>

### <span data-ttu-id="d15dd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d15dd-114">-AccountName</span></span>
<span data-ttu-id="d15dd-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="d15dd-115">Azure data share account name</span></span>

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

### <span data-ttu-id="d15dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15dd-116">-DefaultProfile</span></span>
<span data-ttu-id="d15dd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d15dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d15dd-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d15dd-118">-InputObject</span></span>
<span data-ttu-id="d15dd-119">Obiekt zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d15dd-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="d15dd-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d15dd-120">-Name</span></span>
<span data-ttu-id="d15dd-121">Nazwa zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d15dd-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="d15dd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d15dd-122">-PassThru</span></span>
<span data-ttu-id="d15dd-123">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="d15dd-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="d15dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d15dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="d15dd-125">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="d15dd-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d15dd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d15dd-126">-ResourceId</span></span>
<span data-ttu-id="d15dd-127">Identyfikator zasobu zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d15dd-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="d15dd-128">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="d15dd-128">-ShareName</span></span>
<span data-ttu-id="d15dd-129">Nazwa udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d15dd-129">Azure data share name.</span></span>

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

### <span data-ttu-id="d15dd-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d15dd-130">-Confirm</span></span>
<span data-ttu-id="d15dd-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d15dd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d15dd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d15dd-132">-WhatIf</span></span>
<span data-ttu-id="d15dd-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d15dd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d15dd-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d15dd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d15dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15dd-135">CommonParameters</span></span>
<span data-ttu-id="d15dd-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d15dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15dd-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d15dd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15dd-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d15dd-138">INPUTS</span></span>

### <span data-ttu-id="d15dd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d15dd-139">System.String</span></span>

### <span data-ttu-id="d15dd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="d15dd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="d15dd-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d15dd-141">OUTPUTS</span></span>

### <span data-ttu-id="d15dd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d15dd-142">System.Boolean</span></span>

## <span data-ttu-id="d15dd-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d15dd-143">NOTES</span></span>

## <span data-ttu-id="d15dd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d15dd-144">RELATED LINKS</span></span>
