---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: a549e6c94ae43c8c1cc267448552565f932aa63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525342"
---
# <span data-ttu-id="70889-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="70889-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="70889-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70889-102">SYNOPSIS</span></span>
<span data-ttu-id="70889-103">Pobierz bieżące użycie konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="70889-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70889-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70889-104">SYNTAX</span></span>

### <span data-ttu-id="70889-105">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70889-105">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70889-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70889-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70889-107">ResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="70889-107">ResourceNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70889-108">Opis</span><span class="sxs-lookup"><span data-stu-id="70889-108">DESCRIPTION</span></span>
<span data-ttu-id="70889-109">Polecenie cmdlet **Get-AzureRmCognitiveServicesAccountUsage** pobiera bieżące użycie konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="70889-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="70889-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70889-110">EXAMPLES</span></span>

### <span data-ttu-id="70889-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70889-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="70889-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="70889-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="70889-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="70889-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="70889-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70889-114">PARAMETERS</span></span>

### <span data-ttu-id="70889-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70889-115">-DefaultProfile</span></span>
<span data-ttu-id="70889-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70889-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70889-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="70889-117">-InputObject</span></span>
<span data-ttu-id="70889-118">Obiekt konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="70889-118">Cognitive Services Account Object.</span></span>
```yaml
Type: PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70889-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70889-119">-Name</span></span>
<span data-ttu-id="70889-120">Nazwa konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="70889-120">Cognitive Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70889-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70889-121">-ResourceGroupName</span></span>
<span data-ttu-id="70889-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70889-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70889-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70889-123">-ResourceId</span></span>
<span data-ttu-id="70889-124">Identyfikator zasobu konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="70889-124">Cognitive Services Account Resource ID.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70889-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70889-125">CommonParameters</span></span>
<span data-ttu-id="70889-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70889-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70889-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70889-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70889-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70889-128">INPUTS</span></span>

### <span data-ttu-id="70889-129">System. String</span><span class="sxs-lookup"><span data-stu-id="70889-129">System.String</span></span>

## <span data-ttu-id="70889-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70889-130">OUTPUTS</span></span>

### <span data-ttu-id="70889-131">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="70889-131">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="70889-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70889-132">NOTES</span></span>

## <span data-ttu-id="70889-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70889-133">RELATED LINKS</span></span>
