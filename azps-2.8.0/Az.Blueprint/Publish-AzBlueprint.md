---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 5286b8953a9f28c5e63fe176f19d9d885e9c1d06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706600"
---
# <span data-ttu-id="5cf58-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="5cf58-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="5cf58-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cf58-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf58-103">Publikowanie nowej wersji programu plan.</span><span class="sxs-lookup"><span data-stu-id="5cf58-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="5cf58-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cf58-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cf58-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5cf58-105">DESCRIPTION</span></span>
<span data-ttu-id="5cf58-106">Publikowanie nowej wersji definicji plany.</span><span class="sxs-lookup"><span data-stu-id="5cf58-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="5cf58-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cf58-107">EXAMPLES</span></span>

### <span data-ttu-id="5cf58-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5cf58-108">Example 1</span></span>
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
<span data-ttu-id="5cf58-109">Publikowanie nowej wersji definicji plany.</span><span class="sxs-lookup"><span data-stu-id="5cf58-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="5cf58-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cf58-110">PARAMETERS</span></span>

### <span data-ttu-id="5cf58-111">-Plan</span><span class="sxs-lookup"><span data-stu-id="5cf58-111">-Blueprint</span></span>
<span data-ttu-id="5cf58-112">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="5cf58-112">Blueprint object.</span></span>

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

### <span data-ttu-id="5cf58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf58-113">-DefaultProfile</span></span>
<span data-ttu-id="5cf58-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf58-115">-Version</span><span class="sxs-lookup"><span data-stu-id="5cf58-115">-Version</span></span>
<span data-ttu-id="5cf58-116">Wersja definicji plany.</span><span class="sxs-lookup"><span data-stu-id="5cf58-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="5cf58-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="5cf58-117">-ChangeNote</span></span>
<span data-ttu-id="5cf58-118">Uwagi opisujące zawartość tej wersji programu plan.</span><span class="sxs-lookup"><span data-stu-id="5cf58-118">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="5cf58-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf58-119">CommonParameters</span></span>
<span data-ttu-id="5cf58-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf58-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5cf58-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf58-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf58-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cf58-122">INPUTS</span></span>

### <span data-ttu-id="5cf58-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf58-123">System.String</span></span>

### <span data-ttu-id="5cf58-124">Microsoft. Azure. Commands. plan. modele. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="5cf58-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="5cf58-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cf58-125">OUTPUTS</span></span>

### <span data-ttu-id="5cf58-126">Microsoft. Azure. Commands. plan. modele. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="5cf58-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="5cf58-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cf58-127">NOTES</span></span>

## <span data-ttu-id="5cf58-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cf58-128">RELATED LINKS</span></span>
