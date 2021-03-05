---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 668b7be0a4c6f9885bf8ebb3a077d58f99b681fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978641"
---
# <span data-ttu-id="9c60b-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9c60b-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="9c60b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c60b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c60b-103">Tworzy nowe zamówienie dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="9c60b-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="9c60b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9c60b-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c60b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9c60b-105">DESCRIPTION</span></span>
<span data-ttu-id="9c60b-106">Polecenie **cmdlet New-AzDataBoxEdgeOrder** tworzy nową kolejność dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="9c60b-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="9c60b-107">Przed utworzeniem zamówienia należy utworzyć zasób urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="9c60b-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="9c60b-108">Możesz określić szczegóły, takie jak osoba kontaktowa, nazwa firmy, adres e-mail, adres itp. jako parametry tworzenia zamówienia.</span><span class="sxs-lookup"><span data-stu-id="9c60b-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="9c60b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9c60b-109">EXAMPLES</span></span>

### <span data-ttu-id="9c60b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c60b-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="9c60b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c60b-111">PARAMETERS</span></span>

### <span data-ttu-id="9c60b-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="9c60b-112">-AddressLine1</span></span>
<span data-ttu-id="9c60b-113">Pierwszy wiersz adresu</span><span class="sxs-lookup"><span data-stu-id="9c60b-113">Address first line</span></span>

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

### <span data-ttu-id="9c60b-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="9c60b-114">-AddressLine2</span></span>
<span data-ttu-id="9c60b-115">Drugi wiersz adresu</span><span class="sxs-lookup"><span data-stu-id="9c60b-115">Address second line</span></span>

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

### <span data-ttu-id="9c60b-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="9c60b-116">-AddressLine3</span></span>
<span data-ttu-id="9c60b-117">Trzeci wiersz adresu</span><span class="sxs-lookup"><span data-stu-id="9c60b-117">Address third line</span></span>

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

### <span data-ttu-id="9c60b-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9c60b-118">-AsJob</span></span>
<span data-ttu-id="9c60b-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9c60b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c60b-120">— Miasto</span><span class="sxs-lookup"><span data-stu-id="9c60b-120">-City</span></span>
<span data-ttu-id="9c60b-121">Nazwa miasta</span><span class="sxs-lookup"><span data-stu-id="9c60b-121">Name of the City</span></span>

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

### <span data-ttu-id="9c60b-122">— Nazwa_firmy</span><span class="sxs-lookup"><span data-stu-id="9c60b-122">-CompanyName</span></span>
<span data-ttu-id="9c60b-123">Nazwa firmy</span><span class="sxs-lookup"><span data-stu-id="9c60b-123">Name of the company</span></span>

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

### <span data-ttu-id="9c60b-124">— ContactPerson</span><span class="sxs-lookup"><span data-stu-id="9c60b-124">-ContactPerson</span></span>
<span data-ttu-id="9c60b-125">Imię i nazwisko osoby kontaktowej</span><span class="sxs-lookup"><span data-stu-id="9c60b-125">Name of the contact person</span></span>

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

### <span data-ttu-id="9c60b-126">— Kraj</span><span class="sxs-lookup"><span data-stu-id="9c60b-126">-Country</span></span>
<span data-ttu-id="9c60b-127">Nazwa kraju</span><span class="sxs-lookup"><span data-stu-id="9c60b-127">Name of the Country</span></span>

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

### <span data-ttu-id="9c60b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c60b-128">-DefaultProfile</span></span>
<span data-ttu-id="9c60b-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c60b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c60b-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9c60b-130">-DeviceName</span></span>
<span data-ttu-id="9c60b-131">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="9c60b-131">Resource Name</span></span>

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

### <span data-ttu-id="9c60b-132">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="9c60b-132">-Email</span></span>
<span data-ttu-id="9c60b-133">Lista wiadomości e-mail do odbierania aktualizacji, akceptuje maksymalnie 10 wiadomości e-mail</span><span class="sxs-lookup"><span data-stu-id="9c60b-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="9c60b-134">— Telefon</span><span class="sxs-lookup"><span data-stu-id="9c60b-134">-Phone</span></span>
<span data-ttu-id="9c60b-135">Numer telefonu osoby kontaktowej</span><span class="sxs-lookup"><span data-stu-id="9c60b-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="9c60b-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="9c60b-136">-PostalCode</span></span>
<span data-ttu-id="9c60b-137">Kod pocztowy adresu</span><span class="sxs-lookup"><span data-stu-id="9c60b-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="9c60b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c60b-138">-ResourceGroupName</span></span>
<span data-ttu-id="9c60b-139">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9c60b-139">Resource Group Name</span></span>

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

### <span data-ttu-id="9c60b-140">— województwo</span><span class="sxs-lookup"><span data-stu-id="9c60b-140">-State</span></span>
<span data-ttu-id="9c60b-141">Nazwa województwa</span><span class="sxs-lookup"><span data-stu-id="9c60b-141">Name of the State</span></span>

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

### <span data-ttu-id="9c60b-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c60b-142">-Confirm</span></span>
<span data-ttu-id="9c60b-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9c60b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c60b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c60b-144">-WhatIf</span></span>
<span data-ttu-id="9c60b-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c60b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c60b-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9c60b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c60b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c60b-147">CommonParameters</span></span>
<span data-ttu-id="9c60b-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c60b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c60b-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c60b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c60b-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c60b-150">INPUTS</span></span>

### <span data-ttu-id="9c60b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9c60b-151">System.String</span></span>

## <span data-ttu-id="9c60b-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c60b-152">OUTPUTS</span></span>

### <span data-ttu-id="9c60b-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9c60b-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="9c60b-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9c60b-154">NOTES</span></span>

## <span data-ttu-id="9c60b-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c60b-155">RELATED LINKS</span></span>
