---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054470"
---
# <span data-ttu-id="a9d72-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a9d72-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a9d72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9d72-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d72-103">Usuwa rozszerzenie Diagnostyka platformy Azure z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a9d72-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="a9d72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9d72-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a9d72-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9d72-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d72-106">Polecenie cmdlet **Remove-AzureVMDiagnosticsExtension** usuwa rozszerzenie Diagnostyka platformy Microsoft Azure z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a9d72-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="a9d72-107">Musisz przekazać dane wyjściowe tego polecenia cmdlet do polecenia cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a9d72-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="a9d72-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9d72-108">EXAMPLES</span></span>

### <span data-ttu-id="a9d72-109">Przykład 1: Usuwanie rozszerzenia Diagnostyka platformy Azure z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a9d72-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="a9d72-110">To polecenie usuwa rozszerzenie Diagnostyka platformy Azure z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a9d72-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="a9d72-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9d72-111">PARAMETERS</span></span>

### <span data-ttu-id="a9d72-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a9d72-112">-InformationAction</span></span>
<span data-ttu-id="a9d72-113">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="a9d72-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a9d72-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a9d72-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9d72-115">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="a9d72-115">Continue</span></span>
- <span data-ttu-id="a9d72-116">Ignorować</span><span class="sxs-lookup"><span data-stu-id="a9d72-116">Ignore</span></span>
- <span data-ttu-id="a9d72-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="a9d72-117">Inquire</span></span>
- <span data-ttu-id="a9d72-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a9d72-118">SilentlyContinue</span></span>
- <span data-ttu-id="a9d72-119">Przestaw</span><span class="sxs-lookup"><span data-stu-id="a9d72-119">Stop</span></span>
- <span data-ttu-id="a9d72-120">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="a9d72-120">Suspend</span></span>

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

### <span data-ttu-id="a9d72-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a9d72-121">-InformationVariable</span></span>
<span data-ttu-id="a9d72-122">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="a9d72-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a9d72-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="a9d72-123">-Profile</span></span>
<span data-ttu-id="a9d72-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d72-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a9d72-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a9d72-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a9d72-126">-VM</span><span class="sxs-lookup"><span data-stu-id="a9d72-126">-VM</span></span>
<span data-ttu-id="a9d72-127">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a9d72-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="a9d72-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d72-128">CommonParameters</span></span>
<span data-ttu-id="a9d72-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d72-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d72-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d72-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d72-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9d72-131">INPUTS</span></span>

## <span data-ttu-id="a9d72-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9d72-132">OUTPUTS</span></span>

## <span data-ttu-id="a9d72-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9d72-133">NOTES</span></span>

## <span data-ttu-id="a9d72-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9d72-134">RELATED LINKS</span></span>

[<span data-ttu-id="a9d72-135">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a9d72-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="a9d72-136">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a9d72-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="a9d72-137">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a9d72-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


