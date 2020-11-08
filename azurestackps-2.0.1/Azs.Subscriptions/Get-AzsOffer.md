---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054300"
---
# <span data-ttu-id="83d1c-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="83d1c-101">Get-AzsOffer</span></span>

## <span data-ttu-id="83d1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="83d1c-103">Pobierz listę ofert publicznych dla głównego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="83d1c-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="83d1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83d1c-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="83d1c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83d1c-105">DESCRIPTION</span></span>
<span data-ttu-id="83d1c-106">Pobierz listę ofert publicznych dla głównego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="83d1c-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="83d1c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83d1c-107">EXAMPLES</span></span>

### <span data-ttu-id="83d1c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83d1c-108">Example 1</span></span>
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

<span data-ttu-id="83d1c-109">Uzyskiwanie listy ofert publicznych</span><span class="sxs-lookup"><span data-stu-id="83d1c-109">Get the list of public offers</span></span>

## <span data-ttu-id="83d1c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83d1c-110">PARAMETERS</span></span>

### <span data-ttu-id="83d1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d1c-111">-DefaultProfile</span></span>
<span data-ttu-id="83d1c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83d1c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83d1c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d1c-113">CommonParameters</span></span>
<span data-ttu-id="83d1c-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d1c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d1c-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83d1c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d1c-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83d1c-116">INPUTS</span></span>

## <span data-ttu-id="83d1c-117">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83d1c-117">OUTPUTS</span></span>

### <span data-ttu-id="83d1c-118">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="83d1c-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="83d1c-119">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83d1c-119">NOTES</span></span>

## <span data-ttu-id="83d1c-120">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83d1c-120">RELATED LINKS</span></span>

