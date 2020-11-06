---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527049"
---
# <span data-ttu-id="a44ee-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="a44ee-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="a44ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a44ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a44ee-103">Uzyskaj konta rejestracji.</span><span class="sxs-lookup"><span data-stu-id="a44ee-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a44ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a44ee-104">SYNTAX</span></span>

### <span data-ttu-id="a44ee-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a44ee-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a44ee-106">Jedn</span><span class="sxs-lookup"><span data-stu-id="a44ee-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a44ee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a44ee-107">DESCRIPTION</span></span>
<span data-ttu-id="a44ee-108">Polecenie cmdlet **Get-AzureRmEnrollmentAccount umożliwia korzystanie** z kont rejestracji.</span><span class="sxs-lookup"><span data-stu-id="a44ee-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="a44ee-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a44ee-109">EXAMPLES</span></span>

### <span data-ttu-id="a44ee-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a44ee-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="a44ee-111">Pobierz wszystkie dostępne konta rejestracji.</span><span class="sxs-lookup"><span data-stu-id="a44ee-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="a44ee-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a44ee-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="a44ee-113">Uzyskiwanie konta rejestracji z określonym identyfikatorem obiektu.</span><span class="sxs-lookup"><span data-stu-id="a44ee-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="a44ee-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a44ee-114">PARAMETERS</span></span>

### <span data-ttu-id="a44ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44ee-115">-DefaultProfile</span></span>
<span data-ttu-id="a44ee-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a44ee-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a44ee-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a44ee-117">-ObjectId</span></span>
<span data-ttu-id="a44ee-118">ObjectId (identyfikator obiektu) określonego konta rejestracji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="a44ee-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a44ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44ee-119">CommonParameters</span></span>
<span data-ttu-id="a44ee-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a44ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44ee-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a44ee-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44ee-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a44ee-122">INPUTS</span></span>

### <span data-ttu-id="a44ee-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a44ee-123">None</span></span>

## <span data-ttu-id="a44ee-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a44ee-124">OUTPUTS</span></span>

### <span data-ttu-id="a44ee-125">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. rozliczenia. modele. PSEnrollmentAccount, Microsoft. Azure. Commands. rozliczenia, wersja = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a44ee-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="a44ee-126">Microsoft. Azure. Commands. rozliczenia. modele. PSEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="a44ee-126">Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount</span></span>

## <span data-ttu-id="a44ee-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a44ee-127">NOTES</span></span>

## <span data-ttu-id="a44ee-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a44ee-128">RELATED LINKS</span></span>

