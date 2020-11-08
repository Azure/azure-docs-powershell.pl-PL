---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: a39986404e0969de2db4a2b58e0d275e102799cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052036"
---
# <span data-ttu-id="28dea-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="28dea-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="28dea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28dea-102">SYNOPSIS</span></span>
<span data-ttu-id="28dea-103">Tworzy nowe zamówienie dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="28dea-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="28dea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28dea-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28dea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28dea-105">DESCRIPTION</span></span>
<span data-ttu-id="28dea-106">Polecenie cmdlet **New-AzStackEdgeOrder** tworzy nowe zamówienie na urządzeniu z krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="28dea-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="28dea-107">Aby utworzyć zamówienie, należy najpierw utworzyć zasób urządzenia z krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="28dea-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="28dea-108">Możesz określić szczegóły, takie jak osoba kontaktowa, nazwa firmy, e-mail, adres itd., jako parametry tworzenia zamówienia.</span><span class="sxs-lookup"><span data-stu-id="28dea-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="28dea-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28dea-109">EXAMPLES</span></span>

### <span data-ttu-id="28dea-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28dea-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="28dea-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28dea-111">PARAMETERS</span></span>

### <span data-ttu-id="28dea-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="28dea-112">-AddressLine1</span></span>
<span data-ttu-id="28dea-113">Adres — pierwszy wiersz</span><span class="sxs-lookup"><span data-stu-id="28dea-113">Address first line</span></span>

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

### <span data-ttu-id="28dea-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="28dea-114">-AddressLine2</span></span>
<span data-ttu-id="28dea-115">Adres — drugi wiersz</span><span class="sxs-lookup"><span data-stu-id="28dea-115">Address second line</span></span>

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

### <span data-ttu-id="28dea-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="28dea-116">-AddressLine3</span></span>
<span data-ttu-id="28dea-117">Adres — trzeci wiersz</span><span class="sxs-lookup"><span data-stu-id="28dea-117">Address third line</span></span>

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

### <span data-ttu-id="28dea-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28dea-118">-AsJob</span></span>
<span data-ttu-id="28dea-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="28dea-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28dea-120">-Miasto</span><span class="sxs-lookup"><span data-stu-id="28dea-120">-City</span></span>
<span data-ttu-id="28dea-121">Nazwa miasta</span><span class="sxs-lookup"><span data-stu-id="28dea-121">Name of the City</span></span>

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

### <span data-ttu-id="28dea-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="28dea-122">-CompanyName</span></span>
<span data-ttu-id="28dea-123">Imię i nazwisko firmy</span><span class="sxs-lookup"><span data-stu-id="28dea-123">Name of the company</span></span>

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

### <span data-ttu-id="28dea-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="28dea-124">-ContactPerson</span></span>
<span data-ttu-id="28dea-125">Imię i nazwisko osoby do kontaktów</span><span class="sxs-lookup"><span data-stu-id="28dea-125">Name of the contact person</span></span>

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

### <span data-ttu-id="28dea-126">-Country</span><span class="sxs-lookup"><span data-stu-id="28dea-126">-Country</span></span>
<span data-ttu-id="28dea-127">Nazwa kraju</span><span class="sxs-lookup"><span data-stu-id="28dea-127">Name of the Country</span></span>

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

### <span data-ttu-id="28dea-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28dea-128">-DefaultProfile</span></span>
<span data-ttu-id="28dea-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28dea-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28dea-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="28dea-130">-DeviceName</span></span>
<span data-ttu-id="28dea-131">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="28dea-131">Resource Name</span></span>

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

### <span data-ttu-id="28dea-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="28dea-132">-Email</span></span>
<span data-ttu-id="28dea-133">Lista wiadomości E-mail, które mają otrzymywać aktualizacje, akceptuje maksymalnie 10 wiadomości e-mail</span><span class="sxs-lookup"><span data-stu-id="28dea-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="28dea-134">-Phone</span><span class="sxs-lookup"><span data-stu-id="28dea-134">-Phone</span></span>
<span data-ttu-id="28dea-135">Numer telefonu osoby do kontaktów</span><span class="sxs-lookup"><span data-stu-id="28dea-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="28dea-136">-KodPocztowy</span><span class="sxs-lookup"><span data-stu-id="28dea-136">-PostalCode</span></span>
<span data-ttu-id="28dea-137">Kod pocztowy adresu</span><span class="sxs-lookup"><span data-stu-id="28dea-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="28dea-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28dea-138">-ResourceGroupName</span></span>
<span data-ttu-id="28dea-139">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="28dea-139">Resource Group Name</span></span>

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

### <span data-ttu-id="28dea-140">-State</span><span class="sxs-lookup"><span data-stu-id="28dea-140">-State</span></span>
<span data-ttu-id="28dea-141">Nazwa województwa</span><span class="sxs-lookup"><span data-stu-id="28dea-141">Name of the State</span></span>

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

### <span data-ttu-id="28dea-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28dea-142">-Confirm</span></span>
<span data-ttu-id="28dea-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28dea-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28dea-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28dea-144">-WhatIf</span></span>
<span data-ttu-id="28dea-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28dea-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28dea-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28dea-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28dea-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28dea-147">CommonParameters</span></span>
<span data-ttu-id="28dea-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28dea-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28dea-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28dea-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28dea-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28dea-150">INPUTS</span></span>

### <span data-ttu-id="28dea-151">System. String</span><span class="sxs-lookup"><span data-stu-id="28dea-151">System.String</span></span>

## <span data-ttu-id="28dea-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28dea-152">OUTPUTS</span></span>

### <span data-ttu-id="28dea-153">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="28dea-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="28dea-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28dea-154">NOTES</span></span>

## <span data-ttu-id="28dea-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28dea-155">RELATED LINKS</span></span>
