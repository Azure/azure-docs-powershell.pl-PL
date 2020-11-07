---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893902"
---
# <span data-ttu-id="e299e-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="e299e-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="e299e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e299e-102">SYNOPSIS</span></span>
<span data-ttu-id="e299e-103">Pobiera szczegóły dotyczące konkretnej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e299e-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="e299e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e299e-104">SYNTAX</span></span>

### <span data-ttu-id="e299e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e299e-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e299e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e299e-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e299e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e299e-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e299e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e299e-108">DESCRIPTION</span></span>
<span data-ttu-id="e299e-109">Pobiera szczegóły dotyczące konkretnej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e299e-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="e299e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e299e-110">EXAMPLES</span></span>

### <span data-ttu-id="e299e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e299e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="e299e-112">Zapoznaj się z listą abonamentów.</span><span class="sxs-lookup"><span data-stu-id="e299e-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="e299e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e299e-113">PARAMETERS</span></span>

### <span data-ttu-id="e299e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e299e-114">-DefaultProfile</span></span>
<span data-ttu-id="e299e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e299e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e299e-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e299e-116">-InputObject</span></span>
<span data-ttu-id="e299e-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e299e-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e299e-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e299e-118">-SubscriptionId</span></span>
<span data-ttu-id="e299e-119">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e299e-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e299e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e299e-120">CommonParameters</span></span>
<span data-ttu-id="e299e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e299e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e299e-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e299e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e299e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e299e-123">INPUTS</span></span>

### <span data-ttu-id="e299e-124">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="e299e-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="e299e-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e299e-125">OUTPUTS</span></span>

### <span data-ttu-id="e299e-126">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="e299e-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="e299e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e299e-127">NOTES</span></span>

<span data-ttu-id="e299e-128">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e299e-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e299e-129">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e299e-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e299e-130">INPUTobject <ISubscriptionIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="e299e-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e299e-131">`[DelegatedProviderId <String>]`: Identyfikator delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="e299e-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="e299e-132">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e299e-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e299e-133">`[OfferName <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="e299e-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="e299e-134">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e299e-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="e299e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e299e-135">RELATED LINKS</span></span>

