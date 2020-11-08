---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054617"
---
# <span data-ttu-id="82a67-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="82a67-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="82a67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82a67-102">SYNOPSIS</span></span>
<span data-ttu-id="82a67-103">Pobiera dyski z danymi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="82a67-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="82a67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82a67-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="82a67-105">Opis</span><span class="sxs-lookup"><span data-stu-id="82a67-105">DESCRIPTION</span></span>
<span data-ttu-id="82a67-106">Polecenie cmdlet **Get-AzureDataDisk** pobiera obiekt reprezentujący dyski danych na maszynie wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="82a67-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="82a67-107">Aby uzyskać określony obiekt dysk danych, określ logiczny numer jednostki (LUN) dysku.</span><span class="sxs-lookup"><span data-stu-id="82a67-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="82a67-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82a67-108">EXAMPLES</span></span>

### <span data-ttu-id="82a67-109">Przykład 1: pobieranie wszystkich dysków danych dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="82a67-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="82a67-110">To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="82a67-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="82a67-111">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="82a67-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="82a67-112">Bieżące polecenie cmdlet pobiera wszystkie dyski danych dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="82a67-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="82a67-113">Przykład 2: uzyskiwanie określonego dysku z danymi dla vituralvirtual machinevirtual</span><span class="sxs-lookup"><span data-stu-id="82a67-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="82a67-114">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine07 w usłudze o nazwie ContosoService.</span><span class="sxs-lookup"><span data-stu-id="82a67-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="82a67-115">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82a67-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="82a67-116">Bieżące polecenie cmdlet umożliwia pobieranie danych z dysku jednostki LUN 2.</span><span class="sxs-lookup"><span data-stu-id="82a67-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="82a67-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82a67-117">PARAMETERS</span></span>

### <span data-ttu-id="82a67-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="82a67-118">-InformationAction</span></span>
<span data-ttu-id="82a67-119">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="82a67-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="82a67-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="82a67-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82a67-121">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="82a67-121">Continue</span></span>
- <span data-ttu-id="82a67-122">Ignorować</span><span class="sxs-lookup"><span data-stu-id="82a67-122">Ignore</span></span>
- <span data-ttu-id="82a67-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="82a67-123">Inquire</span></span>
- <span data-ttu-id="82a67-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="82a67-124">SilentlyContinue</span></span>
- <span data-ttu-id="82a67-125">Przestaw</span><span class="sxs-lookup"><span data-stu-id="82a67-125">Stop</span></span>
- <span data-ttu-id="82a67-126">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="82a67-126">Suspend</span></span>

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

### <span data-ttu-id="82a67-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="82a67-127">-InformationVariable</span></span>
<span data-ttu-id="82a67-128">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="82a67-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="82a67-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="82a67-129">-Lun</span></span>
<span data-ttu-id="82a67-130">Określa jednostkę LUN dla dysku danych na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="82a67-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="82a67-131">Prawidłowe wartości to: od 0 do 15.</span><span class="sxs-lookup"><span data-stu-id="82a67-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a67-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="82a67-132">-Profile</span></span>
<span data-ttu-id="82a67-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82a67-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82a67-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="82a67-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82a67-135">-VM</span><span class="sxs-lookup"><span data-stu-id="82a67-135">-VM</span></span>
<span data-ttu-id="82a67-136">Określa obiekt maszyny wirtualnej, dla którego to polecenie cmdlet pobiera dyski danych.</span><span class="sxs-lookup"><span data-stu-id="82a67-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="82a67-137">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="82a67-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82a67-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a67-138">CommonParameters</span></span>
<span data-ttu-id="82a67-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a67-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a67-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a67-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a67-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82a67-141">INPUTS</span></span>

## <span data-ttu-id="82a67-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82a67-142">OUTPUTS</span></span>

## <span data-ttu-id="82a67-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82a67-143">NOTES</span></span>

## <span data-ttu-id="82a67-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82a67-144">RELATED LINKS</span></span>

[<span data-ttu-id="82a67-145">Dodaj-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="82a67-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="82a67-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="82a67-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="82a67-147">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="82a67-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="82a67-148">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="82a67-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


