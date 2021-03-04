---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: 4cb6c46f3cadae9d36ec273fe7d6198e35927c81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981985"
---
# <span data-ttu-id="1bba2-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1bba2-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="1bba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bba2-102">SYNOPSIS</span></span>
<span data-ttu-id="1bba2-103">Tworzy nowe zamówienie dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="1bba2-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="1bba2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1bba2-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bba2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1bba2-105">DESCRIPTION</span></span>
<span data-ttu-id="1bba2-106">Polecenie **cmdlet New-AzStackEdgeOrder** tworzy nową kolejność dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="1bba2-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="1bba2-107">Przed utworzeniem zamówienia należy najpierw utworzyć zasób urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="1bba2-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="1bba2-108">Możesz określić szczegóły, takie jak osoba kontaktowa, nazwa firmy, adres e-mail, adres itp. jako parametry tworzenia zamówienia.</span><span class="sxs-lookup"><span data-stu-id="1bba2-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="1bba2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1bba2-109">EXAMPLES</span></span>

### <span data-ttu-id="1bba2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1bba2-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="1bba2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bba2-111">PARAMETERS</span></span>

### <span data-ttu-id="1bba2-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="1bba2-112">-AddressLine1</span></span>
<span data-ttu-id="1bba2-113">Pierwszy wiersz adresu</span><span class="sxs-lookup"><span data-stu-id="1bba2-113">Address first line</span></span>

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

### <span data-ttu-id="1bba2-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="1bba2-114">-AddressLine2</span></span>
<span data-ttu-id="1bba2-115">Drugi wiersz adresu</span><span class="sxs-lookup"><span data-stu-id="1bba2-115">Address second line</span></span>

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

### <span data-ttu-id="1bba2-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="1bba2-116">-AddressLine3</span></span>
<span data-ttu-id="1bba2-117">Trzeci wiersz adresu</span><span class="sxs-lookup"><span data-stu-id="1bba2-117">Address third line</span></span>

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

### <span data-ttu-id="1bba2-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1bba2-118">-AsJob</span></span>
<span data-ttu-id="1bba2-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1bba2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bba2-120">— Miasto</span><span class="sxs-lookup"><span data-stu-id="1bba2-120">-City</span></span>
<span data-ttu-id="1bba2-121">Nazwa miasta</span><span class="sxs-lookup"><span data-stu-id="1bba2-121">Name of the City</span></span>

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

### <span data-ttu-id="1bba2-122">— Nazwa_firmy</span><span class="sxs-lookup"><span data-stu-id="1bba2-122">-CompanyName</span></span>
<span data-ttu-id="1bba2-123">Nazwa firmy</span><span class="sxs-lookup"><span data-stu-id="1bba2-123">Name of the company</span></span>

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

### <span data-ttu-id="1bba2-124">— ContactPerson</span><span class="sxs-lookup"><span data-stu-id="1bba2-124">-ContactPerson</span></span>
<span data-ttu-id="1bba2-125">Imię i nazwisko osoby kontaktowej</span><span class="sxs-lookup"><span data-stu-id="1bba2-125">Name of the contact person</span></span>

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

### <span data-ttu-id="1bba2-126">— Kraj</span><span class="sxs-lookup"><span data-stu-id="1bba2-126">-Country</span></span>
<span data-ttu-id="1bba2-127">Nazwa kraju</span><span class="sxs-lookup"><span data-stu-id="1bba2-127">Name of the Country</span></span>

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

### <span data-ttu-id="1bba2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bba2-128">-DefaultProfile</span></span>
<span data-ttu-id="1bba2-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1bba2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bba2-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1bba2-130">-DeviceName</span></span>
<span data-ttu-id="1bba2-131">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="1bba2-131">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bba2-132">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="1bba2-132">-Email</span></span>
<span data-ttu-id="1bba2-133">Lista wiadomości e-mail do odbierania aktualizacji, akceptuje maksymalnie 10 wiadomości e-mail</span><span class="sxs-lookup"><span data-stu-id="1bba2-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bba2-134">— Telefon</span><span class="sxs-lookup"><span data-stu-id="1bba2-134">-Phone</span></span>
<span data-ttu-id="1bba2-135">Numer telefonu osoby kontaktowej</span><span class="sxs-lookup"><span data-stu-id="1bba2-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="1bba2-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="1bba2-136">-PostalCode</span></span>
<span data-ttu-id="1bba2-137">Kod pocztowy adresu</span><span class="sxs-lookup"><span data-stu-id="1bba2-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="1bba2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bba2-138">-ResourceGroupName</span></span>
<span data-ttu-id="1bba2-139">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1bba2-139">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bba2-140">— województwo</span><span class="sxs-lookup"><span data-stu-id="1bba2-140">-State</span></span>
<span data-ttu-id="1bba2-141">Nazwa województwa</span><span class="sxs-lookup"><span data-stu-id="1bba2-141">Name of the State</span></span>

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

### <span data-ttu-id="1bba2-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1bba2-142">-Confirm</span></span>
<span data-ttu-id="1bba2-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1bba2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bba2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bba2-144">-WhatIf</span></span>
<span data-ttu-id="1bba2-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bba2-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bba2-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1bba2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bba2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bba2-147">CommonParameters</span></span>
<span data-ttu-id="1bba2-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bba2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bba2-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bba2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bba2-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bba2-150">INPUTS</span></span>

### <span data-ttu-id="1bba2-151">System.String</span><span class="sxs-lookup"><span data-stu-id="1bba2-151">System.String</span></span>

## <span data-ttu-id="1bba2-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bba2-152">OUTPUTS</span></span>

### <span data-ttu-id="1bba2-153">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1bba2-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="1bba2-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1bba2-154">NOTES</span></span>

## <span data-ttu-id="1bba2-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bba2-155">RELATED LINKS</span></span>
