---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718268"
---
# <span data-ttu-id="31b24-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="31b24-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="31b24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31b24-102">SYNOPSIS</span></span>
<span data-ttu-id="31b24-103">Pobiera kontakty zabezpieczeń, które zostały skonfigurowane w tej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="31b24-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31b24-104">SYNTAX</span></span>

### <span data-ttu-id="31b24-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="31b24-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b24-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="31b24-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b24-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="31b24-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b24-108">Opis</span><span class="sxs-lookup"><span data-stu-id="31b24-108">DESCRIPTION</span></span>
<span data-ttu-id="31b24-109">Pobiera kontakty zabezpieczeń, które zostały skonfigurowane w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="31b24-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="31b24-110">Kontakt z zabezpieczeniami może otrzymywać powiadomienia na temat alertów zabezpieczeń, które są wykonywane w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="31b24-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="31b24-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31b24-111">EXAMPLES</span></span>

### <span data-ttu-id="31b24-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="31b24-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="31b24-113">Pobiera wszystkie skonfigurowane kontakty zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="31b24-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="31b24-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31b24-114">PARAMETERS</span></span>

### <span data-ttu-id="31b24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b24-115">-DefaultProfile</span></span>
<span data-ttu-id="31b24-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31b24-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b24-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31b24-117">-Name</span></span>
<span data-ttu-id="31b24-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="31b24-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b24-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31b24-119">-ResourceId</span></span>
<span data-ttu-id="31b24-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="31b24-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b24-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b24-121">CommonParameters</span></span>
<span data-ttu-id="31b24-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b24-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b24-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b24-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b24-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31b24-124">INPUTS</span></span>

### <span data-ttu-id="31b24-125">System. String</span><span class="sxs-lookup"><span data-stu-id="31b24-125">System.String</span></span>

## <span data-ttu-id="31b24-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31b24-126">OUTPUTS</span></span>

### <span data-ttu-id="31b24-127">Microsoft. Azure. Commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="31b24-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="31b24-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31b24-128">NOTES</span></span>

## <span data-ttu-id="31b24-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31b24-129">RELATED LINKS</span></span>
