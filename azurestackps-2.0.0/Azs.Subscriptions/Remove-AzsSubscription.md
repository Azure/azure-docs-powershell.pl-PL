---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890114"
---
# <span data-ttu-id="633f0-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="633f0-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="633f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="633f0-102">SYNOPSIS</span></span>


## <span data-ttu-id="633f0-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="633f0-103">SYNTAX</span></span>

### <span data-ttu-id="633f0-104">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="633f0-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="633f0-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="633f0-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="633f0-106">Opis</span><span class="sxs-lookup"><span data-stu-id="633f0-106">DESCRIPTION</span></span>


## <span data-ttu-id="633f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="633f0-107">EXAMPLES</span></span>

### <span data-ttu-id="633f0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="633f0-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="633f0-109">Usuwanie określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="633f0-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="633f0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="633f0-110">PARAMETERS</span></span>

### <span data-ttu-id="633f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633f0-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="633f0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="633f0-112">-Force</span></span>


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

### <span data-ttu-id="633f0-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="633f0-113">-InputObject</span></span>
<span data-ttu-id="633f0-114">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="633f0-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="633f0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="633f0-115">-PassThru</span></span>


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

### <span data-ttu-id="633f0-116">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="633f0-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="633f0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="633f0-117">-Confirm</span></span>
<span data-ttu-id="633f0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="633f0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="633f0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="633f0-119">-WhatIf</span></span>
<span data-ttu-id="633f0-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="633f0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="633f0-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="633f0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="633f0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633f0-122">CommonParameters</span></span>
<span data-ttu-id="633f0-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="633f0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633f0-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="633f0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633f0-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="633f0-125">INPUTS</span></span>

### <span data-ttu-id="633f0-126">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="633f0-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="633f0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="633f0-127">OUTPUTS</span></span>

### <span data-ttu-id="633f0-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="633f0-128">System.Boolean</span></span>



## <span data-ttu-id="633f0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="633f0-129">NOTES</span></span>

<span data-ttu-id="633f0-130">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="633f0-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="633f0-131">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="633f0-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="633f0-132">INPUTobject <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="633f0-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="633f0-133">`[DelegatedProviderId <String>]`: Identyfikator delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="633f0-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="633f0-134">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="633f0-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="633f0-135">`[OfferName <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="633f0-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="633f0-136">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="633f0-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="633f0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="633f0-137">RELATED LINKS</span></span>

