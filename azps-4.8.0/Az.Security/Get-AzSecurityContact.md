---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219871"
---
# <span data-ttu-id="fb95f-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="fb95f-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="fb95f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb95f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb95f-103">Pobiera kontakty zabezpieczeń, które zostały skonfigurowane w tej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fb95f-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="fb95f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb95f-104">SYNTAX</span></span>

### <span data-ttu-id="fb95f-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fb95f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb95f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="fb95f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb95f-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="fb95f-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb95f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fb95f-108">DESCRIPTION</span></span>
<span data-ttu-id="fb95f-109">Pobiera kontakty zabezpieczeń, które zostały skonfigurowane w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fb95f-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="fb95f-110">Kontakt z zabezpieczeniami może otrzymywać powiadomienia na temat alertów zabezpieczeń, które są wykonywane w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="fb95f-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="fb95f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb95f-111">EXAMPLES</span></span>

### <span data-ttu-id="fb95f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb95f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="fb95f-113">Pobiera wszystkie skonfigurowane kontakty zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fb95f-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="fb95f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb95f-114">PARAMETERS</span></span>

### <span data-ttu-id="fb95f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb95f-115">-DefaultProfile</span></span>
<span data-ttu-id="fb95f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb95f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb95f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb95f-117">-Name</span></span>
<span data-ttu-id="fb95f-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="fb95f-118">Resource name.</span></span>

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

### <span data-ttu-id="fb95f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb95f-119">-ResourceId</span></span>
<span data-ttu-id="fb95f-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="fb95f-120">Resource ID.</span></span>

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

### <span data-ttu-id="fb95f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb95f-121">CommonParameters</span></span>
<span data-ttu-id="fb95f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb95f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb95f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb95f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb95f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb95f-124">INPUTS</span></span>

### <span data-ttu-id="fb95f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fb95f-125">System.String</span></span>

## <span data-ttu-id="fb95f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb95f-126">OUTPUTS</span></span>

### <span data-ttu-id="fb95f-127">Microsoft. Azure. Commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="fb95f-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="fb95f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb95f-128">NOTES</span></span>

## <span data-ttu-id="fb95f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb95f-129">RELATED LINKS</span></span>
