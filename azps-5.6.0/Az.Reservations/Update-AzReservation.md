---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: b93dd1462bb019b12fe761e0bdd6cc4172c01b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000177"
---
# <span data-ttu-id="320ed-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="320ed-101">Update-AzReservation</span></span>

## <span data-ttu-id="320ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="320ed-102">SYNOPSIS</span></span>
<span data-ttu-id="320ed-103">Aktualizowanie. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="320ed-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="320ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="320ed-104">SYNTAX</span></span>

### <span data-ttu-id="320ed-105">CommandLine (Default)</span><span class="sxs-lookup"><span data-stu-id="320ed-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320ed-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="320ed-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="320ed-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="320ed-107">DESCRIPTION</span></span>
<span data-ttu-id="320ed-108">Aktualizuje zastosowane `Reservation` zakresy.</span><span class="sxs-lookup"><span data-stu-id="320ed-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="320ed-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="320ed-109">EXAMPLES</span></span>

### <span data-ttu-id="320ed-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="320ed-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="320ed-111">Aktualizuje typ AppliedScopeType określonego typu `Reservation` na Wartość Single i InstanceFlexibility do wartości On.</span><span class="sxs-lookup"><span data-stu-id="320ed-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="320ed-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="320ed-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="320ed-113">Aktualizuje typ AppliedScopeType określonego dla wartości `Reservation` Shared (Udostępnione) i InstanceFlexibility (Sztywność Wystąpienia) na Wartość Wyłączone.</span><span class="sxs-lookup"><span data-stu-id="320ed-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="320ed-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="320ed-114">PARAMETERS</span></span>

### <span data-ttu-id="320ed-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="320ed-115">-AppliedScope</span></span>
<span data-ttu-id="320ed-116">SubscriptionId tego do `Reservation` zastosowania</span><span class="sxs-lookup"><span data-stu-id="320ed-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320ed-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="320ed-117">-AppliedScopeType</span></span>
<span data-ttu-id="320ed-118">Typ zastosowanego zakresu</span><span class="sxs-lookup"><span data-stu-id="320ed-118">Type of the Applied Scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320ed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320ed-119">-DefaultProfile</span></span>
<span data-ttu-id="320ed-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="320ed-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="320ed-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="320ed-121">-InstanceFlexibility</span></span>
<span data-ttu-id="320ed-122">Jeśli występuje, aktualizuje wartość InstanceFlexibility (Sztywność Wystąpienia) właściwości `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="320ed-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="320ed-123">Jeśli nie zostanie określona, istniejąca wartość pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="320ed-123">If not specified, the existing value remains unchanged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320ed-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="320ed-124">-Name</span></span>
<span data-ttu-id="320ed-125">Nazwa rezerwacji</span><span class="sxs-lookup"><span data-stu-id="320ed-125">Name of Reservation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320ed-126">— Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="320ed-126">-Reservation</span></span>
<span data-ttu-id="320ed-127">Parametr obiektu Pipe dla `Reservation`</span><span class="sxs-lookup"><span data-stu-id="320ed-127">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="320ed-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="320ed-128">-ReservationId</span></span>
<span data-ttu-id="320ed-129">Identyfikator `Reservation` aktualizacji</span><span class="sxs-lookup"><span data-stu-id="320ed-129">Id of the `Reservation` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320ed-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="320ed-130">-ReservationOrderId</span></span>
<span data-ttu-id="320ed-131">Identyfikator `ReservationOrder` aktualizacji</span><span class="sxs-lookup"><span data-stu-id="320ed-131">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320ed-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="320ed-132">-Confirm</span></span>
<span data-ttu-id="320ed-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="320ed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320ed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320ed-134">-WhatIf</span></span>
<span data-ttu-id="320ed-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320ed-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="320ed-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="320ed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320ed-137">CommonParameters</span></span>
<span data-ttu-id="320ed-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320ed-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="320ed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320ed-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="320ed-140">INPUTS</span></span>

### <span data-ttu-id="320ed-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="320ed-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="320ed-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="320ed-142">OUTPUTS</span></span>

### <span data-ttu-id="320ed-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="320ed-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="320ed-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="320ed-144">NOTES</span></span>

## <span data-ttu-id="320ed-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="320ed-145">RELATED LINKS</span></span>
