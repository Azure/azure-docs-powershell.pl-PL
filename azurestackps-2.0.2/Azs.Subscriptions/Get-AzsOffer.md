---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061498"
---
# <span data-ttu-id="03fae-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="03fae-101">Get-AzsOffer</span></span>

## <span data-ttu-id="03fae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03fae-102">SYNOPSIS</span></span>
<span data-ttu-id="03fae-103">Pobierz listę ofert publicznych dla głównego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="03fae-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="03fae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03fae-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="03fae-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03fae-105">DESCRIPTION</span></span>
<span data-ttu-id="03fae-106">Pobierz listę ofert publicznych dla głównego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="03fae-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="03fae-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03fae-107">EXAMPLES</span></span>

### <span data-ttu-id="03fae-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03fae-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="03fae-109">Uzyskiwanie listy ofert publicznych</span><span class="sxs-lookup"><span data-stu-id="03fae-109">Get the list of public offers</span></span>

## <span data-ttu-id="03fae-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03fae-110">PARAMETERS</span></span>

### <span data-ttu-id="03fae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fae-111">-DefaultProfile</span></span>
<span data-ttu-id="03fae-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03fae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="03fae-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fae-113">CommonParameters</span></span>
<span data-ttu-id="03fae-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03fae-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fae-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03fae-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fae-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03fae-116">INPUTS</span></span>

## <span data-ttu-id="03fae-117">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03fae-117">OUTPUTS</span></span>

### <span data-ttu-id="03fae-118">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="03fae-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="03fae-119">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03fae-119">NOTES</span></span>

## <span data-ttu-id="03fae-120">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03fae-120">RELATED LINKS</span></span>

