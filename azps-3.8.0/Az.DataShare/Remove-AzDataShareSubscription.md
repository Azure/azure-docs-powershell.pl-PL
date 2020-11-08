---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 12298f5c61981cb34572a104d39a279f7024adf2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051832"
---
# <span data-ttu-id="f5dda-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="f5dda-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="f5dda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5dda-102">SYNOPSIS</span></span>
<span data-ttu-id="f5dda-103">usuwa subskrypcję udostępnioną.</span><span class="sxs-lookup"><span data-stu-id="f5dda-103">removes a share subscription</span></span>

## <span data-ttu-id="f5dda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5dda-104">SYNTAX</span></span>

### <span data-ttu-id="f5dda-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f5dda-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dda-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5dda-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dda-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5dda-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5dda-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f5dda-108">DESCRIPTION</span></span>
<span data-ttu-id="f5dda-109">Polecenie cmdlet **Remove-AzDataShareSubscription** usuwa subskrypcję udostępniania</span><span class="sxs-lookup"><span data-stu-id="f5dda-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="f5dda-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5dda-110">EXAMPLES</span></span>

### <span data-ttu-id="f5dda-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5dda-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="f5dda-112">To polecenie usuwa sharesubscription o nazwie AdsShareSubscription z konta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="f5dda-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="f5dda-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5dda-113">PARAMETERS</span></span>

### <span data-ttu-id="f5dda-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5dda-114">-AccountName</span></span>
<span data-ttu-id="f5dda-115">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="f5dda-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="f5dda-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5dda-116">-AsJob</span></span>
<span data-ttu-id="f5dda-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="f5dda-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="f5dda-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5dda-118">-DefaultProfile</span></span>
<span data-ttu-id="f5dda-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5dda-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5dda-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5dda-120">-InputObject</span></span>
<span data-ttu-id="f5dda-121">Obiekt subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f5dda-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="f5dda-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5dda-122">-Name</span></span>
<span data-ttu-id="f5dda-123">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="f5dda-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="f5dda-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5dda-124">-PassThru</span></span>
<span data-ttu-id="f5dda-125">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="f5dda-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="f5dda-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5dda-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5dda-127">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="f5dda-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f5dda-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5dda-128">-ResourceId</span></span>
<span data-ttu-id="f5dda-129">Identyfikator zasobu subskrypcji udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f5dda-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="f5dda-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5dda-130">-Confirm</span></span>
<span data-ttu-id="f5dda-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5dda-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5dda-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5dda-132">-WhatIf</span></span>
<span data-ttu-id="f5dda-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5dda-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5dda-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f5dda-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5dda-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5dda-135">CommonParameters</span></span>
<span data-ttu-id="f5dda-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5dda-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5dda-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5dda-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5dda-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5dda-138">INPUTS</span></span>

### <span data-ttu-id="f5dda-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f5dda-139">System.String</span></span>

### <span data-ttu-id="f5dda-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="f5dda-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="f5dda-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5dda-141">OUTPUTS</span></span>

### <span data-ttu-id="f5dda-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5dda-142">System.Boolean</span></span>

## <span data-ttu-id="f5dda-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5dda-143">NOTES</span></span>

## <span data-ttu-id="f5dda-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5dda-144">RELATED LINKS</span></span>
