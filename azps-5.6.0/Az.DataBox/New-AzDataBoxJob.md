---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 2c78f8b40621ba58b84169f2bd9022399fce80b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998677"
---
# <span data-ttu-id="2dd7c-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="2dd7c-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="2dd7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd7c-103">Tworzy nowe zadanie pola danych przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="2dd7c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2dd7c-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dd7c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2dd7c-105">DESCRIPTION</span></span>
<span data-ttu-id="2dd7c-106">Polecenie cmdlet **New-AzDataBoxJob** służy do tworzenia nowego zadania pola danych przez określenie szczegółów wymaganych do utworzenia zadania.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="2dd7c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2dd7c-107">EXAMPLES</span></span>

### <span data-ttu-id="2dd7c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2dd7c-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="2dd7c-109">Polecenie cmdlet pobiera wszystkie wymagane parametry i niektóre opcjonalne parametry do utworzenia zadania skrzynki danych.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="2dd7c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dd7c-110">PARAMETERS</span></span>

### <span data-ttu-id="2dd7c-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="2dd7c-111">-AddressType</span></span>
<span data-ttu-id="2dd7c-112">Typ adresu.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-112">Type of Address.</span></span> <span data-ttu-id="2dd7c-113">Dostępne wartości: AddressType.None (domyślne), AddressType.Nawd, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="2dd7c-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd7c-114">— Miasto</span><span class="sxs-lookup"><span data-stu-id="2dd7c-114">-City</span></span>
<span data-ttu-id="2dd7c-115">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-115">Name of the City.</span></span> <span data-ttu-id="2dd7c-116">Np.: San Francisco</span><span class="sxs-lookup"><span data-stu-id="2dd7c-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="2dd7c-117">— Nazwa_firmy</span><span class="sxs-lookup"><span data-stu-id="2dd7c-117">-CompanyName</span></span>
<span data-ttu-id="2dd7c-118">Nazwa firmy</span><span class="sxs-lookup"><span data-stu-id="2dd7c-118">Name of the company</span></span>

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

### <span data-ttu-id="2dd7c-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="2dd7c-119">-ContactName</span></span>
<span data-ttu-id="2dd7c-120">Nazwa kontaktu</span><span class="sxs-lookup"><span data-stu-id="2dd7c-120">Contact Name</span></span>

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

### <span data-ttu-id="2dd7c-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="2dd7c-121">-CountryCode</span></span>
<span data-ttu-id="2dd7c-122">Kod kraju.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-122">Country Code.</span></span> <span data-ttu-id="2dd7c-123">Np.: USA</span><span class="sxs-lookup"><span data-stu-id="2dd7c-123">Ex: US</span></span>

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

### <span data-ttu-id="2dd7c-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="2dd7c-124">-DataBoxType</span></span>
<span data-ttu-id="2dd7c-125">Typ sku pola danych.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-125">Sku type of Databox.</span></span>  <span data-ttu-id="2dd7c-126">Dostępne wartości: DataBox Jednakowy, Pole Danych, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="2dd7c-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd7c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd7c-127">-DefaultProfile</span></span>
<span data-ttu-id="2dd7c-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dd7c-129">- EmailId</span><span class="sxs-lookup"><span data-stu-id="2dd7c-129">-EmailId</span></span>
<span data-ttu-id="2dd7c-130">Można uzyskać listę adresów e-mail.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="2dd7c-131">Co najmniej jeden z nich jest obowiązkowy</span><span class="sxs-lookup"><span data-stu-id="2dd7c-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="2dd7c-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="2dd7c-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="2dd7c-133">W przypadku kolejności DataBox Jednak określanie oczekiwanych danych w terabajtach jest obowiązkowe.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd7c-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2dd7c-134">-Location</span></span>
<span data-ttu-id="2dd7c-135">Lokalizacja subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2dd7c-135">Location of the subscription</span></span>

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

### <span data-ttu-id="2dd7c-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2dd7c-136">-Name</span></span>
<span data-ttu-id="2dd7c-137">Nazwa zadania skrzynki danych do utworzenia</span><span class="sxs-lookup"><span data-stu-id="2dd7c-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="2dd7c-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="2dd7c-138">-PhoneNumber</span></span>
<span data-ttu-id="2dd7c-139">Numer kontaktu</span><span class="sxs-lookup"><span data-stu-id="2dd7c-139">Contact Number</span></span> 

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

### <span data-ttu-id="2dd7c-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="2dd7c-140">-PostalCode</span></span>
<span data-ttu-id="2dd7c-141">Kod pocztowy</span><span class="sxs-lookup"><span data-stu-id="2dd7c-141">Postal Code</span></span>

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

### <span data-ttu-id="2dd7c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd7c-142">-ResourceGroupName</span></span>
<span data-ttu-id="2dd7c-143">Nazwa grupy zasobów, pod którą należy utworzyć zadanie pola danych.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="2dd7c-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="2dd7c-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="2dd7c-145">Wprowadź kod województwa.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-145">Input the state or province code.</span></span> <span data-ttu-id="2dd7c-146">Like CA — Kalifornia; FL — Floryda; NY — Nowy Jork</span><span class="sxs-lookup"><span data-stu-id="2dd7c-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="2dd7c-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2dd7c-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="2dd7c-148">Lista identyfikatorów zasobów kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="2dd7c-149">Co najmniej jeden z nich jest obowiązkowy.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd7c-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="2dd7c-150">-StreetAddress1</span></span>
<span data-ttu-id="2dd7c-151">Ulica</span><span class="sxs-lookup"><span data-stu-id="2dd7c-151">Street Address</span></span>

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

### <span data-ttu-id="2dd7c-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="2dd7c-152">-StreetAddress2</span></span>
<span data-ttu-id="2dd7c-153">Dodatkowy adres pocztowy</span><span class="sxs-lookup"><span data-stu-id="2dd7c-153">Additional Street Address</span></span>

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

### <span data-ttu-id="2dd7c-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="2dd7c-154">-StreetAddress3</span></span>
<span data-ttu-id="2dd7c-155">Dodatkowy adres pocztowy</span><span class="sxs-lookup"><span data-stu-id="2dd7c-155">Additional Street Address</span></span>

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

### <span data-ttu-id="2dd7c-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dd7c-156">-Confirm</span></span>
<span data-ttu-id="2dd7c-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dd7c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd7c-158">-WhatIf</span></span>
<span data-ttu-id="2dd7c-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dd7c-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dd7c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd7c-161">CommonParameters</span></span>
<span data-ttu-id="2dd7c-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd7c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd7c-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dd7c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd7c-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd7c-164">INPUTS</span></span>

### <span data-ttu-id="2dd7c-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2dd7c-165">System.String[]</span></span>

## <span data-ttu-id="2dd7c-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd7c-166">OUTPUTS</span></span>

### <span data-ttu-id="2dd7c-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="2dd7c-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="2dd7c-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2dd7c-168">NOTES</span></span>

## <span data-ttu-id="2dd7c-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dd7c-169">RELATED LINKS</span></span>
