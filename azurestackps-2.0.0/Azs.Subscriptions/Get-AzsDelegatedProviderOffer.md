---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893914"
---
# <span data-ttu-id="2ea40-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="2ea40-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="2ea40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ea40-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea40-103">Uzyskaj określoną ofertę dla delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="2ea40-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="2ea40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ea40-104">SYNTAX</span></span>

### <span data-ttu-id="2ea40-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2ea40-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ea40-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2ea40-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ea40-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2ea40-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ea40-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2ea40-108">DESCRIPTION</span></span>
<span data-ttu-id="2ea40-109">Uzyskaj określoną ofertę dla delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="2ea40-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="2ea40-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ea40-110">EXAMPLES</span></span>

### <span data-ttu-id="2ea40-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ea40-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="2ea40-112">Pobieranie listy ofert dla określonego dostawcy delegowanego</span><span class="sxs-lookup"><span data-stu-id="2ea40-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="2ea40-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ea40-113">PARAMETERS</span></span>

### <span data-ttu-id="2ea40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea40-114">-DefaultProfile</span></span>
<span data-ttu-id="2ea40-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ea40-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="2ea40-116">-DelegatedProviderId</span></span>
<span data-ttu-id="2ea40-117">Identyfikator delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="2ea40-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ea40-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2ea40-118">-InputObject</span></span>
<span data-ttu-id="2ea40-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2ea40-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ea40-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="2ea40-120">-OfferName</span></span>
<span data-ttu-id="2ea40-121">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="2ea40-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ea40-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea40-122">CommonParameters</span></span>
<span data-ttu-id="2ea40-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea40-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea40-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ea40-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea40-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ea40-125">INPUTS</span></span>

### <span data-ttu-id="2ea40-126">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="2ea40-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="2ea40-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ea40-127">OUTPUTS</span></span>

### <span data-ttu-id="2ea40-128">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="2ea40-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="2ea40-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ea40-129">NOTES</span></span>

<span data-ttu-id="2ea40-130">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2ea40-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ea40-131">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ea40-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2ea40-132">INPUTobject <ISubscriptionIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2ea40-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ea40-133">`[DelegatedProviderId <String>]`: Identyfikator delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="2ea40-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="2ea40-134">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2ea40-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ea40-135">`[OfferName <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="2ea40-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="2ea40-136">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2ea40-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="2ea40-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ea40-137">RELATED LINKS</span></span>

