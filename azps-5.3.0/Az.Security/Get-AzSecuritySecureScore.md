---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503037"
---
# <span data-ttu-id="3b110-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="3b110-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="3b110-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b110-102">SYNOPSIS</span></span>
<span data-ttu-id="3b110-103">Pobiera wyniki zabezpieczeń i ich wyniki w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="3b110-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="3b110-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b110-104">SYNTAX</span></span>

### <span data-ttu-id="3b110-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3b110-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b110-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3b110-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b110-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b110-107">EXAMPLES</span></span>

### <span data-ttu-id="3b110-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b110-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="3b110-109">Pobiera wszystkie oceny zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3b110-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="3b110-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b110-110">PARAMETERS</span></span>

### <span data-ttu-id="3b110-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b110-111">-DefaultProfile</span></span>
<span data-ttu-id="3b110-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b110-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b110-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b110-113">-Name</span></span>
<span data-ttu-id="3b110-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b110-114">Resource name.</span></span>

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

### <span data-ttu-id="3b110-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b110-115">CommonParameters</span></span>
<span data-ttu-id="3b110-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b110-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b110-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b110-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b110-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b110-118">INPUTS</span></span>

### <span data-ttu-id="3b110-119">System. String</span><span class="sxs-lookup"><span data-stu-id="3b110-119">System.String</span></span>

## <span data-ttu-id="3b110-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b110-120">OUTPUTS</span></span>

### <span data-ttu-id="3b110-121">Microsoft. Azure. Commands. Security. MODELES. oceny. PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="3b110-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="3b110-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b110-122">NOTES</span></span>

## <span data-ttu-id="3b110-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b110-123">RELATED LINKS</span></span>
