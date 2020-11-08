---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061491"
---
# <span data-ttu-id="d85be-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="d85be-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="d85be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d85be-102">SYNOPSIS</span></span>


## <span data-ttu-id="d85be-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d85be-103">SYNTAX</span></span>

### <span data-ttu-id="d85be-104">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d85be-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d85be-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d85be-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d85be-106">Opis</span><span class="sxs-lookup"><span data-stu-id="d85be-106">DESCRIPTION</span></span>


## <span data-ttu-id="d85be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d85be-107">EXAMPLES</span></span>

### <span data-ttu-id="d85be-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d85be-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="d85be-109">Usuwanie określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d85be-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="d85be-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d85be-110">PARAMETERS</span></span>

### <span data-ttu-id="d85be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85be-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="d85be-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d85be-112">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d85be-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d85be-113">-InputObject</span></span>
<span data-ttu-id="d85be-114">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="d85be-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d85be-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d85be-115">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d85be-116">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d85be-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d85be-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d85be-117">-Confirm</span></span>
<span data-ttu-id="d85be-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d85be-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d85be-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d85be-119">-WhatIf</span></span>
<span data-ttu-id="d85be-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d85be-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d85be-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d85be-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d85be-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85be-122">CommonParameters</span></span>
<span data-ttu-id="d85be-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d85be-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85be-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d85be-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85be-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d85be-125">INPUTS</span></span>

### <span data-ttu-id="d85be-126">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="d85be-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="d85be-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d85be-127">OUTPUTS</span></span>

### <span data-ttu-id="d85be-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d85be-128">System.Boolean</span></span>



## <span data-ttu-id="d85be-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d85be-129">NOTES</span></span>

<span data-ttu-id="d85be-130">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d85be-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d85be-131">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d85be-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d85be-132">INPUTobject <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="d85be-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="d85be-133">`[DelegatedProviderId <String>]`: Identyfikator delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="d85be-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="d85be-134">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d85be-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d85be-135">`[OfferName <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="d85be-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="d85be-136">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d85be-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="d85be-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d85be-137">RELATED LINKS</span></span>

