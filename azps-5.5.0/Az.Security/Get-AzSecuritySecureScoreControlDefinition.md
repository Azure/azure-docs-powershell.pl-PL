---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189139"
---
# <span data-ttu-id="663ae-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="663ae-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="663ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="663ae-102">SYNOPSIS</span></span>
<span data-ttu-id="663ae-103">Pobiera definicje bezpiecznej kontroli wyników w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="663ae-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="663ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="663ae-104">SYNTAX</span></span>

### <span data-ttu-id="663ae-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="663ae-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663ae-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="663ae-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="663ae-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="663ae-107">EXAMPLES</span></span>

### <span data-ttu-id="663ae-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="663ae-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="663ae-109">Pobiera wszystkie definicje kontroli wyników bezpiecznego zabezpieczeń w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="663ae-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="663ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="663ae-110">PARAMETERS</span></span>

### <span data-ttu-id="663ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663ae-111">-DefaultProfile</span></span>
<span data-ttu-id="663ae-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="663ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="663ae-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663ae-113">CommonParameters</span></span>
<span data-ttu-id="663ae-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="663ae-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663ae-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="663ae-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663ae-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="663ae-116">INPUTS</span></span>

### <span data-ttu-id="663ae-117">System.String</span><span class="sxs-lookup"><span data-stu-id="663ae-117">System.String</span></span>

## <span data-ttu-id="663ae-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="663ae-118">OUTPUTS</span></span>

### <span data-ttu-id="663ae-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="663ae-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="663ae-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="663ae-120">NOTES</span></span>

## <span data-ttu-id="663ae-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="663ae-121">RELATED LINKS</span></span>
