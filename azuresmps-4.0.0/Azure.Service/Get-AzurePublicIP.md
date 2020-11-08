---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055297"
---
# <span data-ttu-id="f64de-101">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="f64de-101">Get-AzurePublicIP</span></span>

## <span data-ttu-id="f64de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f64de-102">SYNOPSIS</span></span>
<span data-ttu-id="f64de-103">Pobiera publiczne informacje o adresie IP dla maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f64de-103">Gets the Public IP information for an Azure virtual machine.</span></span>

## <span data-ttu-id="f64de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f64de-104">SYNTAX</span></span>

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f64de-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f64de-105">DESCRIPTION</span></span>
<span data-ttu-id="f64de-106">Polecenie cmdlet **Get-AzurePublicIP** pobiera publiczne informacje o adresie IP dla maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f64de-106">The **Get-AzurePublicIP** cmdlet gets the Public IP information for an Azure virtual machine.</span></span>
<span data-ttu-id="f64de-107">Aby uzyskać adres IP publicznego adresu IP, użyj polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f64de-107">To obtain the IP address of the Public IP, use the **Get-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="f64de-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f64de-108">EXAMPLES</span></span>

### <span data-ttu-id="f64de-109">Przykład 1: uzyskiwanie publicznej konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="f64de-109">Example 1: Get Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

<span data-ttu-id="f64de-110">To polecenie pobiera maszynę wirtualną o nazwie FTPInstance w usłudze o nazwie FTPInAzure przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f64de-110">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f64de-111">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="f64de-111">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f64de-112">Bieżące polecenie cmdlet umożliwia pobieranie publicznej konfiguracji adresów IP z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f64de-112">The current cmdlet gets Public IP configuration from the virtual machine.</span></span>

## <span data-ttu-id="f64de-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f64de-113">PARAMETERS</span></span>

### <span data-ttu-id="f64de-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f64de-114">-InformationAction</span></span>
<span data-ttu-id="f64de-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="f64de-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f64de-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f64de-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f64de-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="f64de-117">Continue</span></span>
- <span data-ttu-id="f64de-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="f64de-118">Ignore</span></span>
- <span data-ttu-id="f64de-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="f64de-119">Inquire</span></span>
- <span data-ttu-id="f64de-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f64de-120">SilentlyContinue</span></span>
- <span data-ttu-id="f64de-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="f64de-121">Stop</span></span>
- <span data-ttu-id="f64de-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="f64de-122">Suspend</span></span>

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

### <span data-ttu-id="f64de-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f64de-123">-InformationVariable</span></span>
<span data-ttu-id="f64de-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="f64de-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f64de-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="f64de-125">-Profile</span></span>
<span data-ttu-id="f64de-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f64de-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f64de-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f64de-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f64de-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="f64de-128">-PublicIPName</span></span>
<span data-ttu-id="f64de-129">Określa publiczną nazwę IP.</span><span class="sxs-lookup"><span data-stu-id="f64de-129">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="f64de-130">-VM</span><span class="sxs-lookup"><span data-stu-id="f64de-130">-VM</span></span>
<span data-ttu-id="f64de-131">Umożliwia określenie maszyny wirtualnej, dla której ten aplet polecenia uzyska publiczną konfigurację adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f64de-131">Specifies the virtual machine for which this cmdlet gets Public IP configuration.</span></span>

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

### <span data-ttu-id="f64de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64de-132">CommonParameters</span></span>
<span data-ttu-id="f64de-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f64de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64de-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f64de-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64de-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f64de-135">INPUTS</span></span>

## <span data-ttu-id="f64de-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f64de-136">OUTPUTS</span></span>

### <span data-ttu-id="f64de-137">Microsoft. platformy windowsazure. Commands. servicemanagement. AssignPublicIPCollection</span><span class="sxs-lookup"><span data-stu-id="f64de-137">Microsoft.WindowsAzure.Commands.ServiceManagement.AssignPublicIPCollection</span></span>

## <span data-ttu-id="f64de-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f64de-138">NOTES</span></span>

## <span data-ttu-id="f64de-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f64de-139">RELATED LINKS</span></span>

[<span data-ttu-id="f64de-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f64de-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f64de-141">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="f64de-141">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="f64de-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="f64de-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)


