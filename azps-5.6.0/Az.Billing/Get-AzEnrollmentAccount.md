---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d05499ded326787b9930574872dd0681f773d1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992930"
---
# <span data-ttu-id="c79f2-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="c79f2-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="c79f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c79f2-102">SYNOPSIS</span></span>
<span data-ttu-id="c79f2-103">Uzyskaj konta rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c79f2-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="c79f2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c79f2-104">SYNTAX</span></span>

### <span data-ttu-id="c79f2-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c79f2-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c79f2-106">Single</span><span class="sxs-lookup"><span data-stu-id="c79f2-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c79f2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c79f2-107">DESCRIPTION</span></span>
<span data-ttu-id="c79f2-108">Polecenie **cmdlet Get-AzEnrollmentAccount** pobiera konta rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c79f2-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="c79f2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c79f2-109">EXAMPLES</span></span>

### <span data-ttu-id="c79f2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c79f2-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="c79f2-111">Uzyskaj wszystkie dostępne konta rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c79f2-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="c79f2-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c79f2-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="c79f2-113">Uzyskaj konto rejestracji z określonym identyfikatorem obiektu.</span><span class="sxs-lookup"><span data-stu-id="c79f2-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="c79f2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c79f2-114">PARAMETERS</span></span>

### <span data-ttu-id="c79f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79f2-115">-DefaultProfile</span></span>
<span data-ttu-id="c79f2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c79f2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c79f2-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c79f2-117">-ObjectId</span></span>
<span data-ttu-id="c79f2-118">ObjectId konkretnego konta rejestracji do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="c79f2-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79f2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79f2-119">CommonParameters</span></span>
<span data-ttu-id="c79f2-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c79f2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79f2-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79f2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79f2-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c79f2-122">INPUTS</span></span>

### <span data-ttu-id="c79f2-123">Brak</span><span class="sxs-lookup"><span data-stu-id="c79f2-123">None</span></span>

## <span data-ttu-id="c79f2-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c79f2-124">OUTPUTS</span></span>

### <span data-ttu-id="c79f2-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="c79f2-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="c79f2-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c79f2-126">NOTES</span></span>

## <span data-ttu-id="c79f2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c79f2-127">RELATED LINKS</span></span>
