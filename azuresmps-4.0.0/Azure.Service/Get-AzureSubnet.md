---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054509"
---
# <span data-ttu-id="e623f-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="e623f-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="e623f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e623f-102">SYNOPSIS</span></span>
<span data-ttu-id="e623f-103">Pobiera listę podsieci skojarzonych z określoną maszyną wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e623f-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="e623f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e623f-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e623f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e623f-105">DESCRIPTION</span></span>
<span data-ttu-id="e623f-106">Polecenie cmdlet **Get-AzureSubnet** zwraca listę podsieci skojarzonych z określoną maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="e623f-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="e623f-107">Użyj **Get-AzureVM** , aby określić maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="e623f-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="e623f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e623f-108">EXAMPLES</span></span>

### <span data-ttu-id="e623f-109">Przykład 1: uzyskiwanie podsieci dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e623f-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="e623f-110">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine01 w usłudze o nazwie ContosoService03, a następnie zapisuje ją w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="e623f-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="e623f-111">Drugie polecenie pobiera podsieci platformy Azure dla maszyny wirtualnej w $VM.</span><span class="sxs-lookup"><span data-stu-id="e623f-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="e623f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e623f-112">PARAMETERS</span></span>

### <span data-ttu-id="e623f-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e623f-113">-InformationAction</span></span>
<span data-ttu-id="e623f-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e623f-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e623f-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e623f-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e623f-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e623f-116">Continue</span></span>
- <span data-ttu-id="e623f-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e623f-117">Ignore</span></span>
- <span data-ttu-id="e623f-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="e623f-118">Inquire</span></span>
- <span data-ttu-id="e623f-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e623f-119">SilentlyContinue</span></span>
- <span data-ttu-id="e623f-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e623f-120">Stop</span></span>
- <span data-ttu-id="e623f-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e623f-121">Suspend</span></span>

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

### <span data-ttu-id="e623f-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e623f-122">-InformationVariable</span></span>
<span data-ttu-id="e623f-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e623f-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e623f-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="e623f-124">-Profile</span></span>
<span data-ttu-id="e623f-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e623f-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e623f-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e623f-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e623f-127">-VM</span><span class="sxs-lookup"><span data-stu-id="e623f-127">-VM</span></span>
<span data-ttu-id="e623f-128">Określa obiekt maszyny wirtualnej, z której ma zostać wykorzystana lista podsieci.</span><span class="sxs-lookup"><span data-stu-id="e623f-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

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

### <span data-ttu-id="e623f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e623f-129">CommonParameters</span></span>
<span data-ttu-id="e623f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e623f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e623f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e623f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e623f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e623f-132">INPUTS</span></span>

## <span data-ttu-id="e623f-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e623f-133">OUTPUTS</span></span>

## <span data-ttu-id="e623f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e623f-134">NOTES</span></span>

## <span data-ttu-id="e623f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e623f-135">RELATED LINKS</span></span>

[<span data-ttu-id="e623f-136">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e623f-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="e623f-137">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="e623f-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


