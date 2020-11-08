---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: e61beaa43f881aa148401ef91cd4cb37c1f18d88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049957"
---
# <span data-ttu-id="d9519-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="d9519-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="d9519-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9519-102">SYNOPSIS</span></span>
<span data-ttu-id="d9519-103">Publikowanie nowej wersji programu plan.</span><span class="sxs-lookup"><span data-stu-id="d9519-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="d9519-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9519-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9519-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d9519-105">DESCRIPTION</span></span>
<span data-ttu-id="d9519-106">Publikowanie nowej wersji definicji plany.</span><span class="sxs-lookup"><span data-stu-id="d9519-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="d9519-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9519-107">EXAMPLES</span></span>

### <span data-ttu-id="d9519-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9519-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```
<span data-ttu-id="d9519-109">Publikowanie nowej wersji definicji plany.</span><span class="sxs-lookup"><span data-stu-id="d9519-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="d9519-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9519-110">PARAMETERS</span></span>

### <span data-ttu-id="d9519-111">-Plan</span><span class="sxs-lookup"><span data-stu-id="d9519-111">-Blueprint</span></span>
<span data-ttu-id="d9519-112">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="d9519-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9519-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9519-113">-DefaultProfile</span></span>
<span data-ttu-id="d9519-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9519-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9519-115">-Version</span><span class="sxs-lookup"><span data-stu-id="d9519-115">-Version</span></span>
<span data-ttu-id="d9519-116">Wersja definicji plany.</span><span class="sxs-lookup"><span data-stu-id="d9519-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="d9519-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="d9519-117">-ChangeNote</span></span>
<span data-ttu-id="d9519-118">Uwagi opisujące zawartość tej wersji programu plan.</span><span class="sxs-lookup"><span data-stu-id="d9519-118">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9519-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9519-119">CommonParameters</span></span>
<span data-ttu-id="d9519-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9519-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d9519-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9519-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9519-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9519-122">INPUTS</span></span>

### <span data-ttu-id="d9519-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d9519-123">System.String</span></span>

### <span data-ttu-id="d9519-124">Microsoft. Azure. Commands. plan. modele. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="d9519-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="d9519-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9519-125">OUTPUTS</span></span>

### <span data-ttu-id="d9519-126">Microsoft. Azure. Commands. plan. modele. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="d9519-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="d9519-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9519-127">NOTES</span></span>

## <span data-ttu-id="d9519-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9519-128">RELATED LINKS</span></span>
