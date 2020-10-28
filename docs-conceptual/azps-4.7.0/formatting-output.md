---
title: Formatowanie danych wyjściowych polecenia cmdlet programu Azure PowerShell
description: Jak formatować dane wyjściowe polecenia cmdlet programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 27acf416d118fb4e25f0f683d97f3a56fe882a1a
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928269"
---
# <a name="format-azure-powershell-cmdlet-output"></a><span data-ttu-id="a6151-103">Formatowanie danych wyjściowych polecenia cmdlet programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6151-103">Format Azure PowerShell cmdlet output</span></span>

<span data-ttu-id="a6151-104">Domyślnie każde polecenie cmdlet programu Azure PowerShell formatuje dane wyjściowe, aby ułatwić ich odczyt.</span><span class="sxs-lookup"><span data-stu-id="a6151-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="a6151-105">Program PowerShell umożliwia konwertowanie lub formatowanie danych wyjściowych poleceń cmdlet przez przesyłanie potokowe do jednego z następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a6151-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="a6151-106">Formatowanie</span><span class="sxs-lookup"><span data-stu-id="a6151-106">Formatting</span></span>      | <span data-ttu-id="a6151-107">Konwersja</span><span class="sxs-lookup"><span data-stu-id="a6151-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="a6151-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="a6151-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="a6151-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="a6151-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="a6151-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="a6151-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="a6151-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="a6151-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="a6151-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="a6151-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="a6151-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="a6151-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="a6151-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="a6151-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="a6151-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="a6151-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="a6151-116">Formatowanie jest używane na potrzeby wyświetlania w terminalu programu PowerShell, a konwersja umożliwia generowanie danych do użycia przez inne skrypty lub programy.</span><span class="sxs-lookup"><span data-stu-id="a6151-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="a6151-117">Format danych wyjściowych tabeli</span><span class="sxs-lookup"><span data-stu-id="a6151-117">Table output format</span></span>

<span data-ttu-id="a6151-118">Domyślnie dane wyjściowe poleceń cmdlet programu Azure PowerShell są przedstawiane w formacie tabeli.</span><span class="sxs-lookup"><span data-stu-id="a6151-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="a6151-119">Ten format nie umożliwia wyświetlania wszystkich informacji o żądanym zasobie:</span><span class="sxs-lookup"><span data-stu-id="a6151-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="a6151-120">Na ilość danych wyświetlanych przez polecenie `Format-Table` może mieć wpływ szerokość okna sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6151-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="a6151-121">W celu ograniczenia danych wyjściowych do określonych właściwości i ustalenia ich kolejności można podać nazwy właściwości jako argumenty polecenia `Format-Table`:</span><span class="sxs-lookup"><span data-stu-id="a6151-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="a6151-122">Format danych wyjściowych listy</span><span class="sxs-lookup"><span data-stu-id="a6151-122">List output format</span></span>

<span data-ttu-id="a6151-123">W formacie danych wyjściowych listy są tworzone dwie kolumny: nazwy właściwości i wartość.</span><span class="sxs-lookup"><span data-stu-id="a6151-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="a6151-124">W przypadku złożonych obiektów zamiast tego jest wyświetlany typ obiektu.</span><span class="sxs-lookup"><span data-stu-id="a6151-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="a6151-125">W poniższych danych wyjściowych usunięto niektóre pola.</span><span class="sxs-lookup"><span data-stu-id="a6151-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="a6151-126">Podobnie jak w przypadku polecenia `Format-Table`, nazwy właściwości można podać, aby ustalić kolejność danych wyjściowych i je ograniczyć:</span><span class="sxs-lookup"><span data-stu-id="a6151-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="a6151-127">Szeroki format danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="a6151-127">Wide output format</span></span>

<span data-ttu-id="a6151-128">Szeroki format danych wyjściowych tworzy tylko jedną nazwę właściwości na zapytanie.</span><span class="sxs-lookup"><span data-stu-id="a6151-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="a6151-129">Wyświetlane właściwości można kontrolować przez podanie właściwości jako argumentu.</span><span class="sxs-lookup"><span data-stu-id="a6151-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="a6151-130">Niestandardowy format danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="a6151-130">Custom output format</span></span>

<span data-ttu-id="a6151-131">Typ danych wyjściowych `Custom-Format` jest przeznaczony do formatowania niestandardowych obiektów.</span><span class="sxs-lookup"><span data-stu-id="a6151-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="a6151-132">Bez żadnych argumentów zachowuje się jak polecenie `Format-List`, ale umożliwia wyświetlanie nazw właściwości klas niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="a6151-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="a6151-133">W poniższych danych wyjściowych usunięto niektóre pola.</span><span class="sxs-lookup"><span data-stu-id="a6151-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="a6151-134">Podawanie nazw właściwości jako argumentów polecenia `Custom-Format` powoduje wyświetlanie par właściwość/wartość dla niestandardowych obiektów ustawionych jako wartości:</span><span class="sxs-lookup"><span data-stu-id="a6151-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="a6151-135">W poniższych danych wyjściowych usunięto niektóre pola.</span><span class="sxs-lookup"><span data-stu-id="a6151-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="a6151-136">Konwersja na inne formaty danych</span><span class="sxs-lookup"><span data-stu-id="a6151-136">Conversion to other data formats</span></span>

<span data-ttu-id="a6151-137">Rodzina poleceń cmdlet `ConvertTo-*` umożliwia konwertowanie wyników poleceń cmdlet programu Azure PowerShell na formaty możliwe do odczytania przez maszyny.</span><span class="sxs-lookup"><span data-stu-id="a6151-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="a6151-138">Aby uzyskać tylko niektóre właściwości z wyników programu Azure PowerShell, użyj polecenia `Select-Object` w potoku przed przeprowadzeniem konwersji.</span><span class="sxs-lookup"><span data-stu-id="a6151-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="a6151-139">W poniższych przykładach pokazano różne rodzaje danych wyjściowych tworzonych w ramach poszczególnych operacji konwersji.</span><span class="sxs-lookup"><span data-stu-id="a6151-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="a6151-140">Konwersja na plik CSV</span><span class="sxs-lookup"><span data-stu-id="a6151-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="a6151-141">Konwersja na plik JSON</span><span class="sxs-lookup"><span data-stu-id="a6151-141">Conversion to JSON</span></span>

<span data-ttu-id="a6151-142">Domyślnie w danych wyjściowych JSON nie są rozwinięte wszystkie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a6151-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="a6151-143">Aby zmienić głębokość rozwiniętych właściwości, użyj argumentu `-Depth`.</span><span class="sxs-lookup"><span data-stu-id="a6151-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="a6151-144">Domyślnie głębokość rozszerzenia ma wartość `2`.</span><span class="sxs-lookup"><span data-stu-id="a6151-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="a6151-145">W poniższych danych wyjściowych usunięto niektóre pola.</span><span class="sxs-lookup"><span data-stu-id="a6151-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="a6151-146">Konwersja na plik XML</span><span class="sxs-lookup"><span data-stu-id="a6151-146">Conversion to XML</span></span>

<span data-ttu-id="a6151-147">Polecenie cmdlet `ConvertTo-XML` konwertuje obiekt odpowiedzi programu Azure PowerShell na czysty obiekt XML, który może być obsługiwany jak każdy inny obiekt XML w programie PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6151-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="a6151-148">Konwersja na plik HTML</span><span class="sxs-lookup"><span data-stu-id="a6151-148">Conversion to HTML</span></span>

<span data-ttu-id="a6151-149">Przekonwertowanie obiektu na format HTML powoduje wygenerowanie danych wyjściowych, które będą renderowane jako tabela HTML.</span><span class="sxs-lookup"><span data-stu-id="a6151-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="a6151-150">Renderowanie kodu HTML zależy od zachowania przeglądarki w przypadku renderowania tabel, które nie zawierają żadnych informacji o szerokości.</span><span class="sxs-lookup"><span data-stu-id="a6151-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="a6151-151">Nie są rozwijane żadne niestandardowe obiekty klas.</span><span class="sxs-lookup"><span data-stu-id="a6151-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```