---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055114"
---
# <span data-ttu-id="dc744-101">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="dc744-101">Remove-AzurePublicIP</span></span>

## <span data-ttu-id="dc744-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc744-102">SYNOPSIS</span></span>
<span data-ttu-id="dc744-103">Usuwa publiczną konfigurację adresu IP z maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dc744-103">Removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="dc744-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc744-104">SYNTAX</span></span>

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dc744-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc744-105">DESCRIPTION</span></span>
<span data-ttu-id="dc744-106">Polecenie cmdlet **Remove-AzurePublicIP** usuwa publiczną konfigurację adresu IP z maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dc744-106">The **Remove-AzurePublicIP** cmdlet removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="dc744-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc744-107">EXAMPLES</span></span>

### <span data-ttu-id="dc744-108">Przykład 1: usuwanie publicznej konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="dc744-108">Example 1: Remove Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

<span data-ttu-id="dc744-109">To polecenie pobiera maszynę wirtualną o nazwie FTPInstance w usłudze o nazwie FTPInAzure przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="dc744-109">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="dc744-110">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="dc744-110">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dc744-111">Bieżące polecenie cmdlet powoduje usunięcie publicznej konfiguracji adresu IP z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc744-111">The current cmdlet removes Public IP configuration from the virtual machine.</span></span>
<span data-ttu-id="dc744-112">Polecenie przekazanie maszyny wirtualnej do polecenia cmdlet **Update-AzureVM** , które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="dc744-112">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="dc744-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc744-113">PARAMETERS</span></span>

### <span data-ttu-id="dc744-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dc744-114">-InformationAction</span></span>
<span data-ttu-id="dc744-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="dc744-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dc744-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dc744-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dc744-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="dc744-117">Continue</span></span>
- <span data-ttu-id="dc744-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="dc744-118">Ignore</span></span>
- <span data-ttu-id="dc744-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="dc744-119">Inquire</span></span>
- <span data-ttu-id="dc744-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dc744-120">SilentlyContinue</span></span>
- <span data-ttu-id="dc744-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="dc744-121">Stop</span></span>
- <span data-ttu-id="dc744-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="dc744-122">Suspend</span></span>

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

### <span data-ttu-id="dc744-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dc744-123">-InformationVariable</span></span>
<span data-ttu-id="dc744-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="dc744-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dc744-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="dc744-125">-Profile</span></span>
<span data-ttu-id="dc744-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc744-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc744-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="dc744-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc744-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="dc744-128">-PublicIPName</span></span>
<span data-ttu-id="dc744-129">Określa publiczną nazwę IP.</span><span class="sxs-lookup"><span data-stu-id="dc744-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc744-130">-VM</span><span class="sxs-lookup"><span data-stu-id="dc744-130">-VM</span></span>
<span data-ttu-id="dc744-131">Umożliwia określenie maszyny wirtualnej, z której to polecenie cmdlet powoduje usunięcie publicznej konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="dc744-131">Specifies the virtual machine from which this cmdlet removes Public IP configuration.</span></span>

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

### <span data-ttu-id="dc744-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc744-132">CommonParameters</span></span>
<span data-ttu-id="dc744-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc744-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc744-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc744-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc744-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc744-135">INPUTS</span></span>

## <span data-ttu-id="dc744-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc744-136">OUTPUTS</span></span>

### <span data-ttu-id="dc744-137">Microsoft. platformy windowsazure. Commands. servicemanagement. model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="dc744-137">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="dc744-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc744-138">NOTES</span></span>

## <span data-ttu-id="dc744-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc744-139">RELATED LINKS</span></span>

[<span data-ttu-id="dc744-140">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="dc744-140">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="dc744-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="dc744-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="dc744-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="dc744-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)

[<span data-ttu-id="dc744-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="dc744-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


