---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: a00edef30c327e9bce4e2fa008dad373a2e6367d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979338"
---
# <span data-ttu-id="385b3-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="385b3-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="385b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="385b3-102">SYNOPSIS</span></span>
<span data-ttu-id="385b3-103">Pobiera kontakty zabezpieczeń, które zostały skonfigurowane w tej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="385b3-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="385b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="385b3-104">SYNTAX</span></span>

### <span data-ttu-id="385b3-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="385b3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="385b3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="385b3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="385b3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="385b3-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="385b3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="385b3-108">DESCRIPTION</span></span>
<span data-ttu-id="385b3-109">Pobiera kontakty zabezpieczeń, które zostały skonfigurowane w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="385b3-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="385b3-110">Kontakt zabezpieczeń może otrzymywać powiadomienia o alertach zabezpieczeń, które są wysyłane w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="385b3-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="385b3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="385b3-111">EXAMPLES</span></span>

### <span data-ttu-id="385b3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="385b3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="385b3-113">Pobiera wszystkie skonfigurowane kontakty zabezpieczeń w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="385b3-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="385b3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="385b3-114">PARAMETERS</span></span>

### <span data-ttu-id="385b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385b3-115">-DefaultProfile</span></span>
<span data-ttu-id="385b3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="385b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="385b3-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="385b3-117">-Name</span></span>
<span data-ttu-id="385b3-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="385b3-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385b3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="385b3-119">-ResourceId</span></span>
<span data-ttu-id="385b3-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="385b3-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385b3-121">CommonParameters</span></span>
<span data-ttu-id="385b3-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385b3-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="385b3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385b3-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="385b3-124">INPUTS</span></span>

### <span data-ttu-id="385b3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="385b3-125">System.String</span></span>

## <span data-ttu-id="385b3-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="385b3-126">OUTPUTS</span></span>

### <span data-ttu-id="385b3-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="385b3-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="385b3-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="385b3-128">NOTES</span></span>

## <span data-ttu-id="385b3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="385b3-129">RELATED LINKS</span></span>
