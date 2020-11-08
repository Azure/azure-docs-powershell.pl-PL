---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219264"
---
# <span data-ttu-id="ab658-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="ab658-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="ab658-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab658-102">SYNOPSIS</span></span>
<span data-ttu-id="ab658-103">Pobiera listę grup maszyn wirtualnych/serwerów związanych z aplikacją dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ab658-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="ab658-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab658-104">SYNTAX</span></span>

### <span data-ttu-id="ab658-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ab658-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab658-106">Opis</span><span class="sxs-lookup"><span data-stu-id="ab658-106">DESCRIPTION</span></span>
<span data-ttu-id="ab658-107">Kontrolki aplikacji adaptacyjnych są obliczane automatycznie przez usługę Azure Security Center, użyj tego polecenia cmdlet, aby uzyskać listę kontrolek aplikacji adaptacyjnych dotyczących zasobów w zakresie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="ab658-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="ab658-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab658-108">EXAMPLES</span></span>

### <span data-ttu-id="ab658-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab658-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="ab658-110">Pobiera listę grup maszyn wirtualnych/serwerów związanych z aplikacją dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ab658-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="ab658-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab658-111">PARAMETERS</span></span>

### <span data-ttu-id="ab658-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab658-112">-DefaultProfile</span></span>
<span data-ttu-id="ab658-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab658-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab658-114">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ab658-114">-SubscriptionId</span></span>
<span data-ttu-id="ab658-115">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ab658-115">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab658-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="ab658-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="ab658-117">Uwzględnij reguły zasad.</span><span class="sxs-lookup"><span data-stu-id="ab658-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab658-118">— Podsumowanie</span><span class="sxs-lookup"><span data-stu-id="ab658-118">-Summary</span></span>
<span data-ttu-id="ab658-119">Zwracanie wyników w postaci podsumowania.</span><span class="sxs-lookup"><span data-stu-id="ab658-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab658-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab658-120">CommonParameters</span></span>
<span data-ttu-id="ab658-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab658-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab658-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab658-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab658-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab658-123">INPUTS</span></span>

### <span data-ttu-id="ab658-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ab658-124">System.String</span></span>

### <span data-ttu-id="ab658-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab658-125">System.Boolean</span></span>

## <span data-ttu-id="ab658-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab658-126">OUTPUTS</span></span>

### <span data-ttu-id="ab658-127">Microsoft. Azure. Commands. Security. models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="ab658-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="ab658-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab658-128">NOTES</span></span>

## <span data-ttu-id="ab658-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab658-129">RELATED LINKS</span></span>
