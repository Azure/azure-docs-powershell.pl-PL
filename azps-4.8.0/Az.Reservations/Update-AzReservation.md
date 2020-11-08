---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219277"
---
# <span data-ttu-id="86a43-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="86a43-101">Update-AzReservation</span></span>

## <span data-ttu-id="86a43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86a43-102">SYNOPSIS</span></span>
<span data-ttu-id="86a43-103">Aktualizacja a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="86a43-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="86a43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86a43-104">SYNTAX</span></span>

### <span data-ttu-id="86a43-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="86a43-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86a43-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="86a43-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86a43-107">Opis</span><span class="sxs-lookup"><span data-stu-id="86a43-107">DESCRIPTION</span></span>
<span data-ttu-id="86a43-108">Aktualizuje zastosowane zakresy `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="86a43-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="86a43-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86a43-109">EXAMPLES</span></span>

### <span data-ttu-id="86a43-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86a43-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="86a43-111">Aktualizuje AppliedScopeType o wartości `Reservation` jeden i InstanceFlexibility na włączone.</span><span class="sxs-lookup"><span data-stu-id="86a43-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="86a43-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="86a43-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="86a43-113">Umożliwia zaktualizowanie AppliedScopeTypea określonego `Reservation` do współużytkowanego i InstanceFlexibility.</span><span class="sxs-lookup"><span data-stu-id="86a43-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="86a43-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86a43-114">PARAMETERS</span></span>

### <span data-ttu-id="86a43-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="86a43-115">-AppliedScope</span></span>
<span data-ttu-id="86a43-116">Identyfikator subskrypcji `Reservation` do zastosowania</span><span class="sxs-lookup"><span data-stu-id="86a43-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="86a43-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="86a43-117">-AppliedScopeType</span></span>
<span data-ttu-id="86a43-118">Typ zastosowanego zakresu</span><span class="sxs-lookup"><span data-stu-id="86a43-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="86a43-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a43-119">-DefaultProfile</span></span>
<span data-ttu-id="86a43-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86a43-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86a43-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="86a43-121">-InstanceFlexibility</span></span>
<span data-ttu-id="86a43-122">Jeśli jest obecny, aktualizuje wartość InstanceFlexibility `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="86a43-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="86a43-123">Jeśli nie określono tej wartości, istniejąca wartość pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="86a43-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="86a43-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86a43-124">-Name</span></span>
<span data-ttu-id="86a43-125">Nazwa rezerwacji</span><span class="sxs-lookup"><span data-stu-id="86a43-125">Name of Reservation</span></span>

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

### <span data-ttu-id="86a43-126">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="86a43-126">-Reservation</span></span>
<span data-ttu-id="86a43-127">Parametr obiektu potoku `Reservation`</span><span class="sxs-lookup"><span data-stu-id="86a43-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="86a43-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="86a43-128">-ReservationId</span></span>
<span data-ttu-id="86a43-129">Identyfikator `Reservation` aktualizacji</span><span class="sxs-lookup"><span data-stu-id="86a43-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="86a43-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="86a43-130">-ReservationOrderId</span></span>
<span data-ttu-id="86a43-131">Identyfikator `ReservationOrder` aktualizacji</span><span class="sxs-lookup"><span data-stu-id="86a43-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="86a43-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86a43-132">-Confirm</span></span>
<span data-ttu-id="86a43-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86a43-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86a43-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86a43-134">-WhatIf</span></span>
<span data-ttu-id="86a43-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86a43-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86a43-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86a43-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86a43-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a43-137">CommonParameters</span></span>
<span data-ttu-id="86a43-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a43-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a43-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86a43-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a43-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86a43-140">INPUTS</span></span>

### <span data-ttu-id="86a43-141">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="86a43-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="86a43-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86a43-142">OUTPUTS</span></span>

### <span data-ttu-id="86a43-143">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="86a43-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="86a43-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86a43-144">NOTES</span></span>

## <span data-ttu-id="86a43-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86a43-145">RELATED LINKS</span></span>
