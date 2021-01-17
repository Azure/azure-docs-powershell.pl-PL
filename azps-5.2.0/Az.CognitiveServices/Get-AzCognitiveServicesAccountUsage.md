---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: c287fd6aafcfe63a26c5f1dfd01503adb741428d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338722"
---
# <span data-ttu-id="c4e59-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="c4e59-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="c4e59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4e59-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e59-103">Pobierz bieżące użycie konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="c4e59-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="c4e59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4e59-104">SYNTAX</span></span>

### <span data-ttu-id="c4e59-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4e59-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4e59-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e59-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4e59-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e59-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4e59-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c4e59-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e59-109">Polecenie cmdlet **Get-AzCognitiveServicesAccountUsage** pobiera bieżące użycie konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="c4e59-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="c4e59-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4e59-110">EXAMPLES</span></span>

### <span data-ttu-id="c4e59-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c4e59-111">Example 1</span></span>
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

### <span data-ttu-id="c4e59-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c4e59-112">Example 2</span></span>
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

### <span data-ttu-id="c4e59-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c4e59-113">Example 3</span></span>
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

## <span data-ttu-id="c4e59-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4e59-114">PARAMETERS</span></span>

### <span data-ttu-id="c4e59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e59-115">-DefaultProfile</span></span>
<span data-ttu-id="c4e59-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4e59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4e59-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c4e59-117">-InputObject</span></span>
<span data-ttu-id="c4e59-118">Obiekt konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="c4e59-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="c4e59-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4e59-119">-Name</span></span>
<span data-ttu-id="c4e59-120">Nazwa konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="c4e59-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="c4e59-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e59-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4e59-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4e59-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c4e59-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e59-123">-ResourceId</span></span>
<span data-ttu-id="c4e59-124">Identyfikator zasobu konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="c4e59-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="c4e59-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e59-125">CommonParameters</span></span>
<span data-ttu-id="c4e59-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4e59-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e59-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4e59-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e59-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4e59-128">INPUTS</span></span>

### <span data-ttu-id="c4e59-129">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c4e59-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="c4e59-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e59-130">System.String</span></span>

## <span data-ttu-id="c4e59-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4e59-131">OUTPUTS</span></span>

### <span data-ttu-id="c4e59-132">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="c4e59-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="c4e59-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4e59-133">NOTES</span></span>

## <span data-ttu-id="c4e59-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4e59-134">RELATED LINKS</span></span>
