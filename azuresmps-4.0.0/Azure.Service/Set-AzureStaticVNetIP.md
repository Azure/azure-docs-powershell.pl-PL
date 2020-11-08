---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054828"
---
# <span data-ttu-id="6a637-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="6a637-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="6a637-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a637-102">SYNOPSIS</span></span>
<span data-ttu-id="6a637-103">Ustawia statyczne informacje o adresie IP VNet dla obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a637-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="6a637-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a637-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6a637-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a637-105">DESCRIPTION</span></span>
<span data-ttu-id="6a637-106">Polecenie cmdlet **Set-AzureStaticVNetIP** ustawia informacje o adresie IP statycznej sieci wirtualnej (wirtualnej) dla obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a637-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="6a637-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a637-107">EXAMPLES</span></span>

### <span data-ttu-id="6a637-108">Przykład 1: Ustawianie adresu IP sieci wirtualnej skojarzonego z maszyną wirtualną</span><span class="sxs-lookup"><span data-stu-id="6a637-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="6a637-109">Pierwsze polecenie ustawia ścieżkę konfiguracji sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a637-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="6a637-110">Drugie polecenie tworzy konfigurację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a637-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="6a637-111">Trzecie polecenie ustawia podsieć dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a637-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="6a637-112">Czwarte polecenie ustawia adres IP maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a637-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="6a637-113">Piąte polecenie tworzy maszynę wirtualną przy użyciu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a637-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="6a637-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a637-114">PARAMETERS</span></span>

### <span data-ttu-id="6a637-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6a637-115">-InformationAction</span></span>
<span data-ttu-id="6a637-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="6a637-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6a637-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a637-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a637-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="6a637-118">Continue</span></span>
- <span data-ttu-id="6a637-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="6a637-119">Ignore</span></span>
- <span data-ttu-id="6a637-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="6a637-120">Inquire</span></span>
- <span data-ttu-id="6a637-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6a637-121">SilentlyContinue</span></span>
- <span data-ttu-id="6a637-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="6a637-122">Stop</span></span>
- <span data-ttu-id="6a637-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="6a637-123">Suspend</span></span>

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

### <span data-ttu-id="6a637-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6a637-124">-InformationVariable</span></span>
<span data-ttu-id="6a637-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="6a637-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6a637-126">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="6a637-126">-IPAddress</span></span>
<span data-ttu-id="6a637-127">Określa statyczny adres IP VNet</span><span class="sxs-lookup"><span data-stu-id="6a637-127">Specifies the static VNet IP address</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a637-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="6a637-128">-Profile</span></span>
<span data-ttu-id="6a637-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a637-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a637-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6a637-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a637-131">-VM</span><span class="sxs-lookup"><span data-stu-id="6a637-131">-VM</span></span>
<span data-ttu-id="6a637-132">Określa trwały obiekt maszyny wirtualnej, dla którego ma zostać ustawiony statyczny adres IP VNet.</span><span class="sxs-lookup"><span data-stu-id="6a637-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="6a637-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a637-133">CommonParameters</span></span>
<span data-ttu-id="6a637-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a637-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a637-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a637-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a637-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a637-136">INPUTS</span></span>

## <span data-ttu-id="6a637-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a637-137">OUTPUTS</span></span>

## <span data-ttu-id="6a637-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a637-138">NOTES</span></span>

## <span data-ttu-id="6a637-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a637-139">RELATED LINKS</span></span>

[<span data-ttu-id="6a637-140">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="6a637-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="6a637-141">Test — AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="6a637-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)


