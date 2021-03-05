---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 2fc4e536ed3f97b1d0e31ccea382d4dc55d59083
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981210"
---
# <span data-ttu-id="59afc-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="59afc-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="59afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59afc-102">SYNOPSIS</span></span>
<span data-ttu-id="59afc-103">Pobierz bieżące zastosowania dla konta usług cognitive services.</span><span class="sxs-lookup"><span data-stu-id="59afc-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="59afc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59afc-104">SYNTAX</span></span>

### <span data-ttu-id="59afc-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="59afc-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59afc-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59afc-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59afc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59afc-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59afc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="59afc-108">DESCRIPTION</span></span>
<span data-ttu-id="59afc-109">Polecenie **cmdlet Get-AzCognitiveServicesAccountUsage** pobiera bieżące użycie konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="59afc-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="59afc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59afc-110">EXAMPLES</span></span>

### <span data-ttu-id="59afc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59afc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="59afc-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="59afc-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="59afc-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="59afc-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="59afc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59afc-114">PARAMETERS</span></span>

### <span data-ttu-id="59afc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59afc-115">-DefaultProfile</span></span>
<span data-ttu-id="59afc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59afc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59afc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59afc-117">-InputObject</span></span>
<span data-ttu-id="59afc-118">Obiekt konta usług cognitive services.</span><span class="sxs-lookup"><span data-stu-id="59afc-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59afc-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="59afc-119">-Name</span></span>
<span data-ttu-id="59afc-120">Nazwa konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="59afc-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59afc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59afc-121">-ResourceGroupName</span></span>
<span data-ttu-id="59afc-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59afc-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59afc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59afc-123">-ResourceId</span></span>
<span data-ttu-id="59afc-124">Identyfikator zasobu konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="59afc-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59afc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59afc-125">CommonParameters</span></span>
<span data-ttu-id="59afc-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59afc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59afc-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59afc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59afc-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59afc-128">INPUTS</span></span>

### <span data-ttu-id="59afc-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="59afc-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="59afc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="59afc-130">System.String</span></span>

## <span data-ttu-id="59afc-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59afc-131">OUTPUTS</span></span>

### <span data-ttu-id="59afc-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="59afc-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="59afc-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59afc-133">NOTES</span></span>

## <span data-ttu-id="59afc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59afc-134">RELATED LINKS</span></span>
