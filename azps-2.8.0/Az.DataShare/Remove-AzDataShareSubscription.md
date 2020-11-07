---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: a2bcfa4232c7e69bdb17a5d56ff7b79373593b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705652"
---
# <span data-ttu-id="5a849-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="5a849-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="5a849-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a849-102">SYNOPSIS</span></span>
<span data-ttu-id="5a849-103">usuwa subskrypcję udostępnioną.</span><span class="sxs-lookup"><span data-stu-id="5a849-103">removes a share subscription</span></span>

## <span data-ttu-id="5a849-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a849-104">SYNTAX</span></span>

### <span data-ttu-id="5a849-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5a849-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a849-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a849-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a849-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a849-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a849-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5a849-108">DESCRIPTION</span></span>
<span data-ttu-id="5a849-109">Polecenie cmdlet **Remove-AzDataShareSubscription** usuwa subskrypcję udostępniania</span><span class="sxs-lookup"><span data-stu-id="5a849-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="5a849-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a849-110">EXAMPLES</span></span>

### <span data-ttu-id="5a849-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a849-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="5a849-112">To polecenie usuwa sharesubscription o nazwie AdsShareSubscription z konta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="5a849-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="5a849-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a849-113">PARAMETERS</span></span>

### <span data-ttu-id="5a849-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5a849-114">-AccountName</span></span>
<span data-ttu-id="5a849-115">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="5a849-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="5a849-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a849-116">-AsJob</span></span>
<span data-ttu-id="5a849-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="5a849-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="5a849-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a849-118">-DefaultProfile</span></span>
<span data-ttu-id="5a849-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a849-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a849-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5a849-120">-InputObject</span></span>
<span data-ttu-id="5a849-121">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5a849-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a849-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a849-122">-Name</span></span>
<span data-ttu-id="5a849-123">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="5a849-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="5a849-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a849-124">-PassThru</span></span>
<span data-ttu-id="5a849-125">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="5a849-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="5a849-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a849-126">-ResourceGroupName</span></span>
<span data-ttu-id="5a849-127">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="5a849-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5a849-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a849-128">-ResourceId</span></span>
<span data-ttu-id="5a849-129">Identyfikator zasobu subskrypcji udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5a849-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="5a849-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a849-130">-Confirm</span></span>
<span data-ttu-id="5a849-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a849-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a849-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a849-132">-WhatIf</span></span>
<span data-ttu-id="5a849-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a849-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a849-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5a849-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a849-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a849-135">CommonParameters</span></span>
<span data-ttu-id="5a849-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a849-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a849-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a849-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a849-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a849-138">INPUTS</span></span>

### <span data-ttu-id="5a849-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5a849-139">System.String</span></span>

### <span data-ttu-id="5a849-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="5a849-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="5a849-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a849-141">OUTPUTS</span></span>

### <span data-ttu-id="5a849-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a849-142">System.Boolean</span></span>

## <span data-ttu-id="5a849-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a849-143">NOTES</span></span>

## <span data-ttu-id="5a849-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a849-144">RELATED LINKS</span></span>