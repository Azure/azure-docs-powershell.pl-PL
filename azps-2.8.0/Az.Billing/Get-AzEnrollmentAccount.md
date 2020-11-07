---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d76797f82a14c8efa2f9a3d6a77436fa2f8a1b68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706622"
---
# <span data-ttu-id="b3312-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="b3312-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="b3312-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3312-102">SYNOPSIS</span></span>
<span data-ttu-id="b3312-103">Uzyskaj konta rejestracji.</span><span class="sxs-lookup"><span data-stu-id="b3312-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="b3312-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3312-104">SYNTAX</span></span>

### <span data-ttu-id="b3312-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b3312-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3312-106">Jedn</span><span class="sxs-lookup"><span data-stu-id="b3312-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3312-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b3312-107">DESCRIPTION</span></span>
<span data-ttu-id="b3312-108">Polecenie cmdlet **Get-AzEnrollmentAccount umożliwia korzystanie** z kont rejestracji.</span><span class="sxs-lookup"><span data-stu-id="b3312-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="b3312-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3312-109">EXAMPLES</span></span>

### <span data-ttu-id="b3312-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3312-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="b3312-111">Pobierz wszystkie dostępne konta rejestracji.</span><span class="sxs-lookup"><span data-stu-id="b3312-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="b3312-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b3312-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="b3312-113">Uzyskiwanie konta rejestracji z określonym identyfikatorem obiektu.</span><span class="sxs-lookup"><span data-stu-id="b3312-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="b3312-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3312-114">PARAMETERS</span></span>

### <span data-ttu-id="b3312-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3312-115">-DefaultProfile</span></span>
<span data-ttu-id="b3312-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b3312-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3312-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b3312-117">-ObjectId</span></span>
<span data-ttu-id="b3312-118">ObjectId (identyfikator obiektu) określonego konta rejestracji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="b3312-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="b3312-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3312-119">CommonParameters</span></span>
<span data-ttu-id="b3312-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3312-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3312-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3312-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3312-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3312-122">INPUTS</span></span>

### <span data-ttu-id="b3312-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b3312-123">None</span></span>

## <span data-ttu-id="b3312-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3312-124">OUTPUTS</span></span>

### <span data-ttu-id="b3312-125">Microsoft. Azure. Commands. rozliczenia. modele. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="b3312-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="b3312-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3312-126">NOTES</span></span>

## <span data-ttu-id="b3312-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3312-127">RELATED LINKS</span></span>
