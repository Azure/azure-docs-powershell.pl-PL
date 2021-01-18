---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503036"
---
# <span data-ttu-id="42fcc-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="42fcc-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="42fcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="42fcc-103">Pobiera definicje kontroli wyników zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="42fcc-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="42fcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42fcc-104">SYNTAX</span></span>

### <span data-ttu-id="42fcc-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42fcc-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42fcc-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="42fcc-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42fcc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42fcc-107">EXAMPLES</span></span>

### <span data-ttu-id="42fcc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42fcc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="42fcc-109">Pobiera wszystkie definicje kontroli wyników zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="42fcc-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="42fcc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42fcc-110">PARAMETERS</span></span>

### <span data-ttu-id="42fcc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42fcc-111">-DefaultProfile</span></span>
<span data-ttu-id="42fcc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42fcc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42fcc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42fcc-113">CommonParameters</span></span>
<span data-ttu-id="42fcc-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42fcc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42fcc-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42fcc-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42fcc-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42fcc-116">INPUTS</span></span>

### <span data-ttu-id="42fcc-117">System. String</span><span class="sxs-lookup"><span data-stu-id="42fcc-117">System.String</span></span>

## <span data-ttu-id="42fcc-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42fcc-118">OUTPUTS</span></span>

### <span data-ttu-id="42fcc-119">Microsoft. Azure. Commands. Security. MODELES. oceny. PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="42fcc-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="42fcc-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42fcc-120">NOTES</span></span>

## <span data-ttu-id="42fcc-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42fcc-121">RELATED LINKS</span></span>
