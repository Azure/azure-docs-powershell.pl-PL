---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 7e7b32322d6c6a131ee906c56b0c4fbdd0a5d63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708433"
---
# <span data-ttu-id="38eb9-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="38eb9-101">Update-AzReservation</span></span>

## <span data-ttu-id="38eb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="38eb9-103">Aktualizacja a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="38eb9-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="38eb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38eb9-104">SYNTAX</span></span>

### <span data-ttu-id="38eb9-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="38eb9-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38eb9-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="38eb9-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38eb9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="38eb9-107">DESCRIPTION</span></span>
<span data-ttu-id="38eb9-108">Aktualizuje zastosowane zakresy `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="38eb9-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="38eb9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38eb9-109">EXAMPLES</span></span>

### <span data-ttu-id="38eb9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38eb9-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="38eb9-111">Aktualizuje AppliedScopeType o wartości `Reservation` jeden i InstanceFlexibility na włączone.</span><span class="sxs-lookup"><span data-stu-id="38eb9-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="38eb9-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="38eb9-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="38eb9-113">Umożliwia zaktualizowanie AppliedScopeTypea określonego `Reservation` do współużytkowanego i InstanceFlexibility.</span><span class="sxs-lookup"><span data-stu-id="38eb9-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="38eb9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38eb9-114">PARAMETERS</span></span>

### <span data-ttu-id="38eb9-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="38eb9-115">-AppliedScope</span></span>
<span data-ttu-id="38eb9-116">Identyfikator subskrypcji `Reservation` do zastosowania</span><span class="sxs-lookup"><span data-stu-id="38eb9-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="38eb9-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="38eb9-117">-AppliedScopeType</span></span>
<span data-ttu-id="38eb9-118">Typ zastosowanego zakresu</span><span class="sxs-lookup"><span data-stu-id="38eb9-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="38eb9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38eb9-119">-DefaultProfile</span></span>
<span data-ttu-id="38eb9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38eb9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38eb9-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="38eb9-121">-InstanceFlexibility</span></span>
<span data-ttu-id="38eb9-122">Jeśli jest obecny, aktualizuje wartość InstanceFlexibility `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="38eb9-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="38eb9-123">Jeśli nie określono tej wartości, istniejąca wartość pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="38eb9-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="38eb9-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38eb9-124">-Name</span></span>
<span data-ttu-id="38eb9-125">Nazwa rezerwacji</span><span class="sxs-lookup"><span data-stu-id="38eb9-125">Name of Reservation</span></span>

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

### <span data-ttu-id="38eb9-126">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="38eb9-126">-Reservation</span></span>
<span data-ttu-id="38eb9-127">Parametr obiektu potoku `Reservation`</span><span class="sxs-lookup"><span data-stu-id="38eb9-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="38eb9-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="38eb9-128">-ReservationId</span></span>
<span data-ttu-id="38eb9-129">Identyfikator `Reservation` aktualizacji</span><span class="sxs-lookup"><span data-stu-id="38eb9-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="38eb9-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="38eb9-130">-ReservationOrderId</span></span>
<span data-ttu-id="38eb9-131">Identyfikator `ReservationOrder` aktualizacji</span><span class="sxs-lookup"><span data-stu-id="38eb9-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="38eb9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38eb9-132">-Confirm</span></span>
<span data-ttu-id="38eb9-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38eb9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38eb9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38eb9-134">-WhatIf</span></span>
<span data-ttu-id="38eb9-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38eb9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38eb9-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="38eb9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38eb9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38eb9-137">CommonParameters</span></span>
<span data-ttu-id="38eb9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38eb9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38eb9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38eb9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38eb9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38eb9-140">INPUTS</span></span>

### <span data-ttu-id="38eb9-141">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="38eb9-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="38eb9-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38eb9-142">OUTPUTS</span></span>

### <span data-ttu-id="38eb9-143">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="38eb9-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="38eb9-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38eb9-144">NOTES</span></span>

## <span data-ttu-id="38eb9-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38eb9-145">RELATED LINKS</span></span>
