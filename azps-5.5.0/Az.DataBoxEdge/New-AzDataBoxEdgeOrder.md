---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181090"
---
# <span data-ttu-id="30f6d-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="30f6d-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="30f6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="30f6d-103">Tworzy nowe zamówienie dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="30f6d-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="30f6d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="30f6d-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30f6d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="30f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="30f6d-106">Polecenie **cmdlet New-AzDataBoxEdgeOrder** tworzy nową kolejność dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="30f6d-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="30f6d-107">Przed utworzeniem zamówienia należy utworzyć zasób urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="30f6d-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="30f6d-108">Możesz określić szczegóły, takie jak osoba kontaktowa, nazwa firmy, adres e-mail, adres itp. jako parametry tworzenia zamówienia.</span><span class="sxs-lookup"><span data-stu-id="30f6d-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="30f6d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="30f6d-109">EXAMPLES</span></span>

### <span data-ttu-id="30f6d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30f6d-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="30f6d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30f6d-111">PARAMETERS</span></span>

### <span data-ttu-id="30f6d-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="30f6d-112">-AddressLine1</span></span>
<span data-ttu-id="30f6d-113">Pierwszy wiersz adresu</span><span class="sxs-lookup"><span data-stu-id="30f6d-113">Address first line</span></span>

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

### <span data-ttu-id="30f6d-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="30f6d-114">-AddressLine2</span></span>
<span data-ttu-id="30f6d-115">Drugi wiersz adresu</span><span class="sxs-lookup"><span data-stu-id="30f6d-115">Address second line</span></span>

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

### <span data-ttu-id="30f6d-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="30f6d-116">-AddressLine3</span></span>
<span data-ttu-id="30f6d-117">Trzeci wiersz adresu</span><span class="sxs-lookup"><span data-stu-id="30f6d-117">Address third line</span></span>

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

### <span data-ttu-id="30f6d-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="30f6d-118">-AsJob</span></span>
<span data-ttu-id="30f6d-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="30f6d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30f6d-120">— Miasto</span><span class="sxs-lookup"><span data-stu-id="30f6d-120">-City</span></span>
<span data-ttu-id="30f6d-121">Nazwa miasta</span><span class="sxs-lookup"><span data-stu-id="30f6d-121">Name of the City</span></span>

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

### <span data-ttu-id="30f6d-122">— Nazwa_firmy</span><span class="sxs-lookup"><span data-stu-id="30f6d-122">-CompanyName</span></span>
<span data-ttu-id="30f6d-123">Nazwa firmy</span><span class="sxs-lookup"><span data-stu-id="30f6d-123">Name of the company</span></span>

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

### <span data-ttu-id="30f6d-124">— ContactPerson</span><span class="sxs-lookup"><span data-stu-id="30f6d-124">-ContactPerson</span></span>
<span data-ttu-id="30f6d-125">Imię i nazwisko osoby kontaktowej</span><span class="sxs-lookup"><span data-stu-id="30f6d-125">Name of the contact person</span></span>

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

### <span data-ttu-id="30f6d-126">— Kraj</span><span class="sxs-lookup"><span data-stu-id="30f6d-126">-Country</span></span>
<span data-ttu-id="30f6d-127">Nazwa kraju</span><span class="sxs-lookup"><span data-stu-id="30f6d-127">Name of the Country</span></span>

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

### <span data-ttu-id="30f6d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f6d-128">-DefaultProfile</span></span>
<span data-ttu-id="30f6d-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="30f6d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30f6d-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="30f6d-130">-DeviceName</span></span>
<span data-ttu-id="30f6d-131">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="30f6d-131">Resource Name</span></span>

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

### <span data-ttu-id="30f6d-132">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="30f6d-132">-Email</span></span>
<span data-ttu-id="30f6d-133">Lista wiadomości e-mail do odbierania aktualizacji, akceptuje maksymalnie 10 wiadomości e-mail</span><span class="sxs-lookup"><span data-stu-id="30f6d-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="30f6d-134">— Telefon</span><span class="sxs-lookup"><span data-stu-id="30f6d-134">-Phone</span></span>
<span data-ttu-id="30f6d-135">Numer telefonu osoby kontaktowej</span><span class="sxs-lookup"><span data-stu-id="30f6d-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="30f6d-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="30f6d-136">-PostalCode</span></span>
<span data-ttu-id="30f6d-137">Kod pocztowy adresu</span><span class="sxs-lookup"><span data-stu-id="30f6d-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="30f6d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f6d-138">-ResourceGroupName</span></span>
<span data-ttu-id="30f6d-139">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="30f6d-139">Resource Group Name</span></span>

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

### <span data-ttu-id="30f6d-140">— województwo</span><span class="sxs-lookup"><span data-stu-id="30f6d-140">-State</span></span>
<span data-ttu-id="30f6d-141">Nazwa województwa</span><span class="sxs-lookup"><span data-stu-id="30f6d-141">Name of the State</span></span>

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

### <span data-ttu-id="30f6d-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30f6d-142">-Confirm</span></span>
<span data-ttu-id="30f6d-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="30f6d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f6d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f6d-144">-WhatIf</span></span>
<span data-ttu-id="30f6d-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30f6d-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30f6d-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="30f6d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f6d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f6d-147">CommonParameters</span></span>
<span data-ttu-id="30f6d-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f6d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f6d-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30f6d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f6d-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30f6d-150">INPUTS</span></span>

### <span data-ttu-id="30f6d-151">System.String</span><span class="sxs-lookup"><span data-stu-id="30f6d-151">System.String</span></span>

## <span data-ttu-id="30f6d-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30f6d-152">OUTPUTS</span></span>

### <span data-ttu-id="30f6d-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="30f6d-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="30f6d-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="30f6d-154">NOTES</span></span>

## <span data-ttu-id="30f6d-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30f6d-155">RELATED LINKS</span></span>
