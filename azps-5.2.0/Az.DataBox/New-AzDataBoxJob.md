---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352894"
---
# <span data-ttu-id="04cdd-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="04cdd-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="04cdd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="04cdd-103">Tworzy nowe zadanie DATAbox przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="04cdd-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="04cdd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04cdd-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04cdd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04cdd-105">DESCRIPTION</span></span>
<span data-ttu-id="04cdd-106">Polecenie cmdlet **New-AzDataBoxJob** służy do tworzenia nowego zadania DATAbox przez określenie szczegółów wymaganych do utworzenia zadania.</span><span class="sxs-lookup"><span data-stu-id="04cdd-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="04cdd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04cdd-107">EXAMPLES</span></span>

### <span data-ttu-id="04cdd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04cdd-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="04cdd-109">Polecenie cmdlet pobiera wszystkie wymagane parametry i niektóre parametry opcjonalne, aby utworzyć zadanie DATAbox.</span><span class="sxs-lookup"><span data-stu-id="04cdd-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="04cdd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04cdd-110">PARAMETERS</span></span>

### <span data-ttu-id="04cdd-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="04cdd-111">-AddressType</span></span>
<span data-ttu-id="04cdd-112">Typ adresu.</span><span class="sxs-lookup"><span data-stu-id="04cdd-112">Type of Address.</span></span> <span data-ttu-id="04cdd-113">Dostępne wartości: wartość w polu adres. Brak (domyślnie), AddressType. mieszkalna, adres. komercyjne</span><span class="sxs-lookup"><span data-stu-id="04cdd-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="04cdd-114">-Miasto</span><span class="sxs-lookup"><span data-stu-id="04cdd-114">-City</span></span>
<span data-ttu-id="04cdd-115">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="04cdd-115">Name of the City.</span></span> <span data-ttu-id="04cdd-116">Ex: San Francisco</span><span class="sxs-lookup"><span data-stu-id="04cdd-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="04cdd-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="04cdd-117">-CompanyName</span></span>
<span data-ttu-id="04cdd-118">Imię i nazwisko firmy</span><span class="sxs-lookup"><span data-stu-id="04cdd-118">Name of the company</span></span>

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

### <span data-ttu-id="04cdd-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="04cdd-119">-ContactName</span></span>
<span data-ttu-id="04cdd-120">Nazwa kontaktu</span><span class="sxs-lookup"><span data-stu-id="04cdd-120">Contact Name</span></span>

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

### <span data-ttu-id="04cdd-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="04cdd-121">-CountryCode</span></span>
<span data-ttu-id="04cdd-122">Numer kierunkowy kraju.</span><span class="sxs-lookup"><span data-stu-id="04cdd-122">Country Code.</span></span> <span data-ttu-id="04cdd-123">Ex: My</span><span class="sxs-lookup"><span data-stu-id="04cdd-123">Ex: US</span></span>

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

### <span data-ttu-id="04cdd-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="04cdd-124">-DataBoxType</span></span>
<span data-ttu-id="04cdd-125">Typ SKU DATAbox.</span><span class="sxs-lookup"><span data-stu-id="04cdd-125">Sku type of Databox.</span></span>  <span data-ttu-id="04cdd-126">Dostępne wartości: DataBoxDisk, DATAbox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="04cdd-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="04cdd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04cdd-127">-DefaultProfile</span></span>
<span data-ttu-id="04cdd-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04cdd-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04cdd-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="04cdd-129">-EmailId</span></span>
<span data-ttu-id="04cdd-130">Możesz podać listę EmailIds.</span><span class="sxs-lookup"><span data-stu-id="04cdd-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="04cdd-131">Co najmniej jedna jest wymagana.</span><span class="sxs-lookup"><span data-stu-id="04cdd-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="04cdd-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="04cdd-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="04cdd-133">W przypadku zlecenia DataBoxDisk określenie oczekiwanych danych w terabajtach jest obowiązkowe.</span><span class="sxs-lookup"><span data-stu-id="04cdd-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="04cdd-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="04cdd-134">-Location</span></span>
<span data-ttu-id="04cdd-135">Lokalizacja subskrypcji</span><span class="sxs-lookup"><span data-stu-id="04cdd-135">Location of the subscription</span></span>

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

### <span data-ttu-id="04cdd-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="04cdd-136">-Name</span></span>
<span data-ttu-id="04cdd-137">Nazwa zadania DATAbox, które ma zostać utworzone</span><span class="sxs-lookup"><span data-stu-id="04cdd-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="04cdd-138">-Rachunek</span><span class="sxs-lookup"><span data-stu-id="04cdd-138">-PhoneNumber</span></span>
<span data-ttu-id="04cdd-139">Numer kontaktu</span><span class="sxs-lookup"><span data-stu-id="04cdd-139">Contact Number</span></span> 

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

### <span data-ttu-id="04cdd-140">-KodPocztowy</span><span class="sxs-lookup"><span data-stu-id="04cdd-140">-PostalCode</span></span>
<span data-ttu-id="04cdd-141">Kod pocztowy</span><span class="sxs-lookup"><span data-stu-id="04cdd-141">Postal Code</span></span>

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

### <span data-ttu-id="04cdd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04cdd-142">-ResourceGroupName</span></span>
<span data-ttu-id="04cdd-143">Nazwa grupy zasobów, pod którą zadanie DATAbox musi zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="04cdd-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="04cdd-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="04cdd-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="04cdd-145">Wprowadź kod województwa.</span><span class="sxs-lookup"><span data-stu-id="04cdd-145">Input the state or province code.</span></span> <span data-ttu-id="04cdd-146">Taki jak CA-California; FL — Florydzie; NY — Nowy Jork</span><span class="sxs-lookup"><span data-stu-id="04cdd-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="04cdd-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="04cdd-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="04cdd-148">Lista identyfikatorów zasobów dla kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="04cdd-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="04cdd-149">Co najmniej jedna jest wymagana.</span><span class="sxs-lookup"><span data-stu-id="04cdd-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="04cdd-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="04cdd-150">-StreetAddress1</span></span>
<span data-ttu-id="04cdd-151">Ulica</span><span class="sxs-lookup"><span data-stu-id="04cdd-151">Street Address</span></span>

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

### <span data-ttu-id="04cdd-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="04cdd-152">-StreetAddress2</span></span>
<span data-ttu-id="04cdd-153">Dodatkowy adres — ulica</span><span class="sxs-lookup"><span data-stu-id="04cdd-153">Additional Street Address</span></span>

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

### <span data-ttu-id="04cdd-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="04cdd-154">-StreetAddress3</span></span>
<span data-ttu-id="04cdd-155">Dodatkowy adres — ulica</span><span class="sxs-lookup"><span data-stu-id="04cdd-155">Additional Street Address</span></span>

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

### <span data-ttu-id="04cdd-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04cdd-156">-Confirm</span></span>
<span data-ttu-id="04cdd-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04cdd-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04cdd-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04cdd-158">-WhatIf</span></span>
<span data-ttu-id="04cdd-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04cdd-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04cdd-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04cdd-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04cdd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04cdd-161">CommonParameters</span></span>
<span data-ttu-id="04cdd-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04cdd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04cdd-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04cdd-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04cdd-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04cdd-164">INPUTS</span></span>

### <span data-ttu-id="04cdd-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="04cdd-165">System.String[]</span></span>

## <span data-ttu-id="04cdd-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04cdd-166">OUTPUTS</span></span>

### <span data-ttu-id="04cdd-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="04cdd-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="04cdd-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04cdd-168">NOTES</span></span>

## <span data-ttu-id="04cdd-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04cdd-169">RELATED LINKS</span></span>
