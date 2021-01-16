---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377839"
---
# <span data-ttu-id="29e3e-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="29e3e-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="29e3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="29e3e-103">Pobiera kontrolki wyników zabezpieczeń i ich wyniki w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="29e3e-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="29e3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29e3e-104">SYNTAX</span></span>

### <span data-ttu-id="29e3e-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="29e3e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29e3e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="29e3e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29e3e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29e3e-107">EXAMPLES</span></span>

### <span data-ttu-id="29e3e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="29e3e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="29e3e-109">Pobiera wszystkie oceny zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="29e3e-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="29e3e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29e3e-110">PARAMETERS</span></span>

### <span data-ttu-id="29e3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e3e-111">-DefaultProfile</span></span>
<span data-ttu-id="29e3e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29e3e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29e3e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29e3e-113">-Name</span></span>
<span data-ttu-id="29e3e-114">Bezpieczna nazwa wyniku.</span><span class="sxs-lookup"><span data-stu-id="29e3e-114">Secure score name.</span></span>

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

### <span data-ttu-id="29e3e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e3e-115">CommonParameters</span></span>
<span data-ttu-id="29e3e-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29e3e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e3e-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29e3e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e3e-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29e3e-118">INPUTS</span></span>

### <span data-ttu-id="29e3e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="29e3e-119">System.String</span></span>

## <span data-ttu-id="29e3e-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29e3e-120">OUTPUTS</span></span>

### <span data-ttu-id="29e3e-121">Microsoft. Azure. Commands. Security. MODELES. oceny. PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="29e3e-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="29e3e-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29e3e-122">NOTES</span></span>

## <span data-ttu-id="29e3e-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29e3e-123">RELATED LINKS</span></span>
