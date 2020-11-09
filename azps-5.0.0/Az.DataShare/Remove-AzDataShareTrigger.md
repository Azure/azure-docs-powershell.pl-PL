---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: f4eff969d93f1c243b9dc15652249bc9800bfd45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305119"
---
# <span data-ttu-id="c7cae-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="c7cae-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="c7cae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7cae-102">SYNOPSIS</span></span>
<span data-ttu-id="c7cae-103">usuwa wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="c7cae-103">removes a trigger</span></span>

## <span data-ttu-id="c7cae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7cae-104">SYNTAX</span></span>

### <span data-ttu-id="c7cae-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c7cae-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7cae-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7cae-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7cae-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7cae-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7cae-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c7cae-108">DESCRIPTION</span></span>
<span data-ttu-id="c7cae-109">Polecenie cmdlet **Remove-AzDataShareTrigger** usuwa wyzwalacz datashare</span><span class="sxs-lookup"><span data-stu-id="c7cae-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="c7cae-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7cae-110">EXAMPLES</span></span>

### <span data-ttu-id="c7cae-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7cae-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c7cae-112">To polecenie usuwa wyzwalacz o nazwie AdsTrigger z subskrypcji udziału AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="c7cae-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="c7cae-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7cae-113">PARAMETERS</span></span>

### <span data-ttu-id="c7cae-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c7cae-114">-AccountName</span></span>
<span data-ttu-id="c7cae-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="c7cae-115">Azure data share account name</span></span>

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

### <span data-ttu-id="c7cae-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7cae-116">-AsJob</span></span>
<span data-ttu-id="c7cae-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="c7cae-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="c7cae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7cae-118">-DefaultProfile</span></span>
<span data-ttu-id="c7cae-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7cae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7cae-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c7cae-120">-InputObject</span></span>
<span data-ttu-id="c7cae-121">Obiekt wyzwalacza udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c7cae-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7cae-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7cae-122">-Name</span></span>
<span data-ttu-id="c7cae-123">Nazwa wyzwalacza udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="c7cae-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="c7cae-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7cae-124">-PassThru</span></span>
<span data-ttu-id="c7cae-125">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="c7cae-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="c7cae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7cae-126">-ResourceGroupName</span></span>
<span data-ttu-id="c7cae-127">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="c7cae-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c7cae-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7cae-128">-ResourceId</span></span>
<span data-ttu-id="c7cae-129">Identyfikator zasobu wyzwalacza udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c7cae-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="c7cae-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c7cae-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="c7cae-131">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="c7cae-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7cae-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7cae-132">-Confirm</span></span>
<span data-ttu-id="c7cae-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7cae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7cae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7cae-134">-WhatIf</span></span>
<span data-ttu-id="c7cae-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7cae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7cae-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c7cae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7cae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7cae-137">CommonParameters</span></span>
<span data-ttu-id="c7cae-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7cae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7cae-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7cae-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7cae-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7cae-140">INPUTS</span></span>

### <span data-ttu-id="c7cae-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c7cae-141">System.String</span></span>

### <span data-ttu-id="c7cae-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="c7cae-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="c7cae-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7cae-143">OUTPUTS</span></span>

### <span data-ttu-id="c7cae-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7cae-144">System.Boolean</span></span>

## <span data-ttu-id="c7cae-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7cae-145">NOTES</span></span>

## <span data-ttu-id="c7cae-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7cae-146">RELATED LINKS</span></span>
