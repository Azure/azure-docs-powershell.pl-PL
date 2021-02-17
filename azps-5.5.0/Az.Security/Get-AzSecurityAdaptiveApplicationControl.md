---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178602"
---
# <span data-ttu-id="248cb-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="248cb-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="248cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="248cb-102">SYNOPSIS</span></span>
<span data-ttu-id="248cb-103">Pobiera listę grup sterowanie aplikacją maszyny wirtualnej/serwera dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="248cb-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="248cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="248cb-104">SYNTAX</span></span>

### <span data-ttu-id="248cb-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="248cb-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="248cb-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="248cb-106">DESCRIPTION</span></span>
<span data-ttu-id="248cb-107">Adaptacyjne kontrolki aplikacji są automatycznie obliczane przez Azure Security Center. To polecenie cmdlet umożliwia uzyskiwanie listy zasobów adaptacyjnych kontrolek aplikacji w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="248cb-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="248cb-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="248cb-108">EXAMPLES</span></span>

### <span data-ttu-id="248cb-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="248cb-109">Example 1</span></span>
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
<span data-ttu-id="248cb-110">Pobiera listę grup sterowanie aplikacją maszyny wirtualnej/serwera dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="248cb-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="248cb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="248cb-111">PARAMETERS</span></span>

### <span data-ttu-id="248cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="248cb-112">-DefaultProfile</span></span>
<span data-ttu-id="248cb-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="248cb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="248cb-114">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="248cb-114">-SubscriptionId</span></span>
<span data-ttu-id="248cb-115">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="248cb-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="248cb-116">— IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="248cb-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="248cb-117">Uwzględnij reguły zasad.</span><span class="sxs-lookup"><span data-stu-id="248cb-117">Include the policy rules.</span></span>

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

### <span data-ttu-id="248cb-118">— Podsumowanie</span><span class="sxs-lookup"><span data-stu-id="248cb-118">-Summary</span></span>
<span data-ttu-id="248cb-119">Zwracanie danych wyjściowych w podsumowanych formularzach.</span><span class="sxs-lookup"><span data-stu-id="248cb-119">Return output in a summarized form.</span></span>

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

### <span data-ttu-id="248cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="248cb-120">CommonParameters</span></span>
<span data-ttu-id="248cb-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="248cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="248cb-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="248cb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="248cb-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="248cb-123">INPUTS</span></span>

### <span data-ttu-id="248cb-124">System.String</span><span class="sxs-lookup"><span data-stu-id="248cb-124">System.String</span></span>

### <span data-ttu-id="248cb-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="248cb-125">System.Boolean</span></span>

## <span data-ttu-id="248cb-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="248cb-126">OUTPUTS</span></span>

### <span data-ttu-id="248cb-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="248cb-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="248cb-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="248cb-128">NOTES</span></span>

## <span data-ttu-id="248cb-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="248cb-129">RELATED LINKS</span></span>
