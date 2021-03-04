---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: ec35083cf4495d0bf262d841563f0dc4100dcdc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974353"
---
# <span data-ttu-id="2a298-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="2a298-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="2a298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a298-102">SYNOPSIS</span></span>
<span data-ttu-id="2a298-103">Pobiera listę grup sterowanie aplikacją maszyny wirtualnej/serwera dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2a298-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="2a298-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a298-104">SYNTAX</span></span>

### <span data-ttu-id="2a298-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2a298-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a298-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a298-106">DESCRIPTION</span></span>
<span data-ttu-id="2a298-107">Adaptacyjne kontrolki aplikacji są automatycznie obliczane przez Azure Security Center. To polecenie cmdlet umożliwia uzyskiwanie listy zasobów adaptacyjnych kontrolek aplikacji w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2a298-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="2a298-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a298-108">EXAMPLES</span></span>

### <span data-ttu-id="2a298-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a298-109">Example 1</span></span>
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
<span data-ttu-id="2a298-110">Pobiera listę grup sterowanie aplikacją maszyny wirtualnej/serwera dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2a298-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="2a298-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a298-111">PARAMETERS</span></span>

### <span data-ttu-id="2a298-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a298-112">-DefaultProfile</span></span>
<span data-ttu-id="2a298-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a298-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a298-114">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a298-114">-SubscriptionId</span></span>
<span data-ttu-id="2a298-115">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a298-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="2a298-116">— IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="2a298-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="2a298-117">Uwzględnij reguły zasad.</span><span class="sxs-lookup"><span data-stu-id="2a298-117">Include the policy rules.</span></span>

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

### <span data-ttu-id="2a298-118">— Podsumowanie</span><span class="sxs-lookup"><span data-stu-id="2a298-118">-Summary</span></span>
<span data-ttu-id="2a298-119">Zwracanie danych wyjściowych w podsumowanych formularzach.</span><span class="sxs-lookup"><span data-stu-id="2a298-119">Return output in a summarized form.</span></span>

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

### <span data-ttu-id="2a298-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a298-120">CommonParameters</span></span>
<span data-ttu-id="2a298-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a298-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a298-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a298-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a298-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a298-123">INPUTS</span></span>

### <span data-ttu-id="2a298-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2a298-124">System.String</span></span>

### <span data-ttu-id="2a298-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a298-125">System.Boolean</span></span>

## <span data-ttu-id="2a298-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a298-126">OUTPUTS</span></span>

### <span data-ttu-id="2a298-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="2a298-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="2a298-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a298-128">NOTES</span></span>

## <span data-ttu-id="2a298-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a298-129">RELATED LINKS</span></span>
