---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054917"
---
# <span data-ttu-id="d4845-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="d4845-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="d4845-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4845-102">SYNOPSIS</span></span>
<span data-ttu-id="d4845-103">Umożliwia zdefiniowanie listy podsieci dla maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d4845-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="d4845-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4845-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d4845-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d4845-105">DESCRIPTION</span></span>
<span data-ttu-id="d4845-106">Polecenie cmdlet **Set-AzureSubnet** ustawia listę podsieci dla konfiguracji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d4845-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="d4845-107">Aby ustawić podsieci maszyny wirtualnej, Użyj ustawień **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="d4845-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="d4845-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4845-108">EXAMPLES</span></span>

### <span data-ttu-id="d4845-109">Przykład 1: Dodawanie podsieci do konfiguracji maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d4845-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="d4845-110">To polecenie umożliwia dodanie podsieci do konfiguracji maszyny wirtualnej, a następnie utworzenie maszyny wirtualnej o nazwie VirtualMachine04.</span><span class="sxs-lookup"><span data-stu-id="d4845-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="d4845-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4845-111">PARAMETERS</span></span>

### <span data-ttu-id="d4845-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d4845-112">-InformationAction</span></span>
<span data-ttu-id="d4845-113">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="d4845-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d4845-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d4845-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4845-115">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="d4845-115">Continue</span></span>
- <span data-ttu-id="d4845-116">Ignorować</span><span class="sxs-lookup"><span data-stu-id="d4845-116">Ignore</span></span>
- <span data-ttu-id="d4845-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="d4845-117">Inquire</span></span>
- <span data-ttu-id="d4845-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d4845-118">SilentlyContinue</span></span>
- <span data-ttu-id="d4845-119">Przestaw</span><span class="sxs-lookup"><span data-stu-id="d4845-119">Stop</span></span>
- <span data-ttu-id="d4845-120">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="d4845-120">Suspend</span></span>

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

### <span data-ttu-id="d4845-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d4845-121">-InformationVariable</span></span>
<span data-ttu-id="d4845-122">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="d4845-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d4845-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="d4845-123">-Profile</span></span>
<span data-ttu-id="d4845-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4845-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4845-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d4845-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4845-126">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="d4845-126">-SubnetNames</span></span>
<span data-ttu-id="d4845-127">Określa tablicę zawierającą listę nazw podsieci.</span><span class="sxs-lookup"><span data-stu-id="d4845-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4845-128">-VM</span><span class="sxs-lookup"><span data-stu-id="d4845-128">-VM</span></span>
<span data-ttu-id="d4845-129">Określa obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d4845-129">Specifies the virtual machine object.</span></span>

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

### <span data-ttu-id="d4845-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4845-130">CommonParameters</span></span>
<span data-ttu-id="d4845-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4845-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4845-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4845-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4845-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4845-133">INPUTS</span></span>

## <span data-ttu-id="d4845-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4845-134">OUTPUTS</span></span>

## <span data-ttu-id="d4845-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4845-135">NOTES</span></span>

## <span data-ttu-id="d4845-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4845-136">RELATED LINKS</span></span>

[<span data-ttu-id="d4845-137">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d4845-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="d4845-138">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="d4845-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="d4845-139">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d4845-139">Update-AzureVM</span></span>](./Update-AzureVM.md)


