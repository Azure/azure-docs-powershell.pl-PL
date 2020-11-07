---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: a1ec489b91d2d510c16709fa0923117bbbaa804a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705650"
---
# <span data-ttu-id="81fdb-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="81fdb-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="81fdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="81fdb-103">usuwa wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="81fdb-103">removes a trigger</span></span>

## <span data-ttu-id="81fdb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81fdb-104">SYNTAX</span></span>

### <span data-ttu-id="81fdb-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="81fdb-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81fdb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81fdb-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81fdb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81fdb-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81fdb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="81fdb-108">DESCRIPTION</span></span>
<span data-ttu-id="81fdb-109">Polecenie cmdlet **Remove-AzDataShareTrigger** usuwa wyzwalacz datashare</span><span class="sxs-lookup"><span data-stu-id="81fdb-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="81fdb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81fdb-110">EXAMPLES</span></span>

### <span data-ttu-id="81fdb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81fdb-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="81fdb-112">To polecenie usuwa wyzwalacz o nazwie AdsTrigger z subskrypcji udziału AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="81fdb-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="81fdb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81fdb-113">PARAMETERS</span></span>

### <span data-ttu-id="81fdb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="81fdb-114">-AccountName</span></span>
<span data-ttu-id="81fdb-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="81fdb-115">Azure data share account name</span></span>

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

### <span data-ttu-id="81fdb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81fdb-116">-AsJob</span></span>
<span data-ttu-id="81fdb-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="81fdb-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="81fdb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81fdb-118">-DefaultProfile</span></span>
<span data-ttu-id="81fdb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81fdb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81fdb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81fdb-120">-InputObject</span></span>
<span data-ttu-id="81fdb-121">Obiekt wyzwalacza udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="81fdb-121">Azure data share trigger object</span></span>


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

### <span data-ttu-id="81fdb-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81fdb-122">-Name</span></span>
<span data-ttu-id="81fdb-123">Nazwa wyzwalacza udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="81fdb-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="81fdb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81fdb-124">-PassThru</span></span>
<span data-ttu-id="81fdb-125">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="81fdb-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="81fdb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81fdb-126">-ResourceGroupName</span></span>
<span data-ttu-id="81fdb-127">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="81fdb-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="81fdb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81fdb-128">-ResourceId</span></span>
<span data-ttu-id="81fdb-129">Identyfikator zasobu wyzwalacza udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="81fdb-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="81fdb-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="81fdb-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="81fdb-131">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="81fdb-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="81fdb-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81fdb-132">-Confirm</span></span>
<span data-ttu-id="81fdb-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81fdb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81fdb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81fdb-134">-WhatIf</span></span>
<span data-ttu-id="81fdb-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81fdb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81fdb-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81fdb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81fdb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81fdb-137">CommonParameters</span></span>
<span data-ttu-id="81fdb-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81fdb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81fdb-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81fdb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81fdb-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81fdb-140">INPUTS</span></span>

### <span data-ttu-id="81fdb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="81fdb-141">System.String</span></span>

### <span data-ttu-id="81fdb-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="81fdb-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="81fdb-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81fdb-143">OUTPUTS</span></span>

### <span data-ttu-id="81fdb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81fdb-144">System.Boolean</span></span>

## <span data-ttu-id="81fdb-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81fdb-145">NOTES</span></span>

## <span data-ttu-id="81fdb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81fdb-146">RELATED LINKS</span></span>
