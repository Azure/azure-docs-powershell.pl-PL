---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051371"
---
# <span data-ttu-id="47126-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="47126-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="47126-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47126-102">SYNOPSIS</span></span>
<span data-ttu-id="47126-103">Uzyskaj konta rejestracji.</span><span class="sxs-lookup"><span data-stu-id="47126-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="47126-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47126-104">SYNTAX</span></span>

### <span data-ttu-id="47126-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="47126-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47126-106">Jedn</span><span class="sxs-lookup"><span data-stu-id="47126-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47126-107">Opis</span><span class="sxs-lookup"><span data-stu-id="47126-107">DESCRIPTION</span></span>
<span data-ttu-id="47126-108">Polecenie cmdlet **Get-AzEnrollmentAccount umożliwia korzystanie** z kont rejestracji.</span><span class="sxs-lookup"><span data-stu-id="47126-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="47126-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47126-109">EXAMPLES</span></span>

### <span data-ttu-id="47126-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47126-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="47126-111">Pobierz wszystkie dostępne konta rejestracji.</span><span class="sxs-lookup"><span data-stu-id="47126-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="47126-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="47126-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="47126-113">Uzyskiwanie konta rejestracji z określonym identyfikatorem obiektu.</span><span class="sxs-lookup"><span data-stu-id="47126-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="47126-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47126-114">PARAMETERS</span></span>

### <span data-ttu-id="47126-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47126-115">-DefaultProfile</span></span>
<span data-ttu-id="47126-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="47126-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47126-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="47126-117">-ObjectId</span></span>
<span data-ttu-id="47126-118">ObjectId (identyfikator obiektu) określonego konta rejestracji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="47126-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="47126-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47126-119">CommonParameters</span></span>
<span data-ttu-id="47126-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47126-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47126-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47126-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47126-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47126-122">INPUTS</span></span>

### <span data-ttu-id="47126-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="47126-123">None</span></span>

## <span data-ttu-id="47126-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47126-124">OUTPUTS</span></span>

### <span data-ttu-id="47126-125">Microsoft. Azure. Commands. rozliczenia. modele. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="47126-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="47126-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47126-126">NOTES</span></span>

## <span data-ttu-id="47126-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47126-127">RELATED LINKS</span></span>
