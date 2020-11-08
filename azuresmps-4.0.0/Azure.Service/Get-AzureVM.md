---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055513"
---
# <span data-ttu-id="ee57c-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee57c-101">Get-AzureVM</span></span>

## <span data-ttu-id="ee57c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee57c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee57c-103">Pobiera informacje z jednej lub większej liczby maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ee57c-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="ee57c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee57c-104">SYNTAX</span></span>

### <span data-ttu-id="ee57c-105">ListAllVMs (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ee57c-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee57c-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="ee57c-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ee57c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ee57c-107">DESCRIPTION</span></span>
<span data-ttu-id="ee57c-108">Polecenie cmdlet **Get-AzureVM** pobiera informacje o maszynach wirtualnych uruchomionych na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ee57c-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="ee57c-109">Zwraca obiekt z informacjami na określonej maszynie wirtualnej lub jeśli nie jest określona żadna maszyna wirtualna, dla wszystkich maszyn wirtualnych w określonej usłudze bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ee57c-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="ee57c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee57c-110">EXAMPLES</span></span>

### <span data-ttu-id="ee57c-111">Przykład 1: pobieranie informacji na określonej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ee57c-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="ee57c-112">To polecenie zwraca obiekt z informacjami na maszynie wirtualnej VirtualMachine02 działającej w chmurze usługi ContosoService01.</span><span class="sxs-lookup"><span data-stu-id="ee57c-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="ee57c-113">Przykład 2: pobieranie informacji na wszystkich maszynach wirtualnych</span><span class="sxs-lookup"><span data-stu-id="ee57c-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="ee57c-114">To polecenie pobiera obiekt listy z informacjami na wszystkich maszynach wirtualnych uruchomionych w usłudze Cloud ContosoService01.</span><span class="sxs-lookup"><span data-stu-id="ee57c-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="ee57c-115">Przykład 3: wyświetlanie tabeli stanu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ee57c-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="ee57c-116">To polecenie wyświetla tabelę zawierającą maszyny wirtualne uruchomione w usłudze ContosoService01, ich domenę uaktualnienia i bieżący stan każdej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ee57c-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="ee57c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee57c-117">PARAMETERS</span></span>

### <span data-ttu-id="ee57c-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ee57c-118">-InformationAction</span></span>
<span data-ttu-id="ee57c-119">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="ee57c-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ee57c-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ee57c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee57c-121">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="ee57c-121">Continue</span></span>
- <span data-ttu-id="ee57c-122">Ignorować</span><span class="sxs-lookup"><span data-stu-id="ee57c-122">Ignore</span></span>
- <span data-ttu-id="ee57c-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="ee57c-123">Inquire</span></span>
- <span data-ttu-id="ee57c-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ee57c-124">SilentlyContinue</span></span>
- <span data-ttu-id="ee57c-125">Przestaw</span><span class="sxs-lookup"><span data-stu-id="ee57c-125">Stop</span></span>
- <span data-ttu-id="ee57c-126">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="ee57c-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee57c-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ee57c-127">-InformationVariable</span></span>
<span data-ttu-id="ee57c-128">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="ee57c-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee57c-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ee57c-129">-Name</span></span>
<span data-ttu-id="ee57c-130">Określa nazwę maszyny wirtualnej, dla której mają zostać pobrane informacje.</span><span class="sxs-lookup"><span data-stu-id="ee57c-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="ee57c-131">Jeśli ten parametr nie zostanie podany, polecenie cmdlet zwraca obiekt listy z informacją o wszystkich maszynach wirtualnych w określonej usłudze.</span><span class="sxs-lookup"><span data-stu-id="ee57c-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee57c-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="ee57c-132">-Profile</span></span>
<span data-ttu-id="ee57c-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee57c-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee57c-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ee57c-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee57c-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ee57c-135">-ServiceName</span></span>
<span data-ttu-id="ee57c-136">Określa nazwę usługi w chmurze, dla której mają zostać zwrócone informacje o maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ee57c-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee57c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee57c-137">CommonParameters</span></span>
<span data-ttu-id="ee57c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee57c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee57c-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee57c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee57c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee57c-140">INPUTS</span></span>

## <span data-ttu-id="ee57c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee57c-141">OUTPUTS</span></span>

## <span data-ttu-id="ee57c-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee57c-142">NOTES</span></span>

## <span data-ttu-id="ee57c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee57c-143">RELATED LINKS</span></span>

[<span data-ttu-id="ee57c-144">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee57c-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ee57c-145">Nowe — AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ee57c-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ee57c-146">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee57c-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="ee57c-147">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee57c-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="ee57c-148">Start — AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee57c-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="ee57c-149">Zatrzymaj — AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee57c-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="ee57c-150">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee57c-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


