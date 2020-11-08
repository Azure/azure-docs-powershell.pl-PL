---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054757"
---
# <span data-ttu-id="b6ad1-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="b6ad1-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="b6ad1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ad1-103">Ustawia rozmiar maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="b6ad1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6ad1-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b6ad1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6ad1-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ad1-106">Polecenie cmdlet **Set-AzureVMSize** umożliwia zaktualizowanie rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="b6ad1-107">Ma dwa parametry: *InstanceSize* , czyli nowy rozmiar maszyny wirtualnej, a *maszyna* wirtualna, która jest obiektem maszyny wirtualnej pobrana przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b6ad1-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="b6ad1-108">Wynik polecenia **Set-AzureVMSize można przetworzyć** do polecenia cmdlet **Update-AzureVM** lub zapisać w zmiennej do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="b6ad1-109">Rzeczywista zmiana nie jest wprowadzana do momentu wykonania instrukcji **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b6ad1-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="b6ad1-110">Uwaga: to polecenie cmdlet wymaga ponownego udostępnienia maszyny wirtualnej i może otrzymać nowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="b6ad1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6ad1-111">EXAMPLES</span></span>

### <span data-ttu-id="b6ad1-112">Przykład 1: Ustawianie rozmiaru maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b6ad1-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="b6ad1-113">To polecenie umożliwia zaktualizowanie maszyny wirtualnej w celu zmiany rozmiaru "mały".</span><span class="sxs-lookup"><span data-stu-id="b6ad1-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="b6ad1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6ad1-114">PARAMETERS</span></span>

### <span data-ttu-id="b6ad1-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b6ad1-115">-InformationAction</span></span>
<span data-ttu-id="b6ad1-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b6ad1-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b6ad1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6ad1-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="b6ad1-118">Continue</span></span>
- <span data-ttu-id="b6ad1-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="b6ad1-119">Ignore</span></span>
- <span data-ttu-id="b6ad1-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="b6ad1-120">Inquire</span></span>
- <span data-ttu-id="b6ad1-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b6ad1-121">SilentlyContinue</span></span>
- <span data-ttu-id="b6ad1-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="b6ad1-122">Stop</span></span>
- <span data-ttu-id="b6ad1-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="b6ad1-123">Suspend</span></span>

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

### <span data-ttu-id="b6ad1-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b6ad1-124">-InformationVariable</span></span>
<span data-ttu-id="b6ad1-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b6ad1-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="b6ad1-126">-InstanceSize</span></span>
<span data-ttu-id="b6ad1-127">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="b6ad1-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b6ad1-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="b6ad1-129">--ExtraSmall--mały--medium--Large--ExtraLarge--A5--A6--</span><span class="sxs-lookup"><span data-stu-id="b6ad1-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ad1-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="b6ad1-130">-Profile</span></span>
<span data-ttu-id="b6ad1-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6ad1-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6ad1-133">-VM</span><span class="sxs-lookup"><span data-stu-id="b6ad1-133">-VM</span></span>
<span data-ttu-id="b6ad1-134">Określa trwały obiekt maszyny wirtualnej, w którym ten aplet cmdlet ustawia rozmiar.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

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

### <span data-ttu-id="b6ad1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ad1-135">CommonParameters</span></span>
<span data-ttu-id="b6ad1-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ad1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ad1-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ad1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ad1-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6ad1-138">INPUTS</span></span>

## <span data-ttu-id="b6ad1-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6ad1-139">OUTPUTS</span></span>

## <span data-ttu-id="b6ad1-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6ad1-140">NOTES</span></span>

## <span data-ttu-id="b6ad1-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6ad1-141">RELATED LINKS</span></span>

[<span data-ttu-id="b6ad1-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b6ad1-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="b6ad1-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b6ad1-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


