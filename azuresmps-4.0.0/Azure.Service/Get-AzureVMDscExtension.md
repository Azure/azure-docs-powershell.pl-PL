---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9D6D1890-9442-45F1-A3AA-BB1DB5CB33D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 462d40e463edf6894810ac6e00e39b9c7a9eabe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055504"
---
# <span data-ttu-id="4cbfc-101">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4cbfc-101">Get-AzureVMDscExtension</span></span>

## <span data-ttu-id="4cbfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbfc-103">Pobiera ustawienia rozszerzenia DSC na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4cbfc-103">Gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="4cbfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cbfc-104">SYNTAX</span></span>

```
Get-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4cbfc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4cbfc-105">DESCRIPTION</span></span>
<span data-ttu-id="4cbfc-106">Polecenie cmdlet **Get-AzureVMDscExtension** pobiera ustawienia rozszerzenia DSC na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4cbfc-106">The **Get-AzureVMDscExtension** cmdlet gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="4cbfc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cbfc-107">EXAMPLES</span></span>

### <span data-ttu-id="4cbfc-108">Przykład 1: uzyskiwanie ustawienia dla rozszerzenia DSC na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4cbfc-108">Example 1: Get the setting of the DSC Extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMDscExtension -VM $VMModulesUrl
https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zipConfigurationFunction : MyConfiguration.ps1\MyConfigurationProperties            : {ServerName}ExtensionName         : DSCPublisher             : Microsoft.PowershellVersion               : 1.*PrivateConfiguration  :PublicConfiguration   : {"ModulesUrl": "https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zip","ConfigurationFunction": "MyConfiguration.ps1\\MyConfiguration","Properties": {"ServerName": "C:\\MyDirectory"}}ReferenceName         : DSCState                 : EnableRoleName              : my-vm
```

<span data-ttu-id="4cbfc-109">To polecenie pobiera ustawienia rozszerzenia DSC na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4cbfc-109">This command gets the settings of the DSC Extension on a virtual machine.</span></span>

## <span data-ttu-id="4cbfc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cbfc-110">PARAMETERS</span></span>

### <span data-ttu-id="4cbfc-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4cbfc-111">-InformationAction</span></span>
<span data-ttu-id="4cbfc-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="4cbfc-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4cbfc-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4cbfc-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4cbfc-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="4cbfc-114">Continue</span></span>
- <span data-ttu-id="4cbfc-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="4cbfc-115">Ignore</span></span>
- <span data-ttu-id="4cbfc-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="4cbfc-116">Inquire</span></span>
- <span data-ttu-id="4cbfc-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4cbfc-117">SilentlyContinue</span></span>
- <span data-ttu-id="4cbfc-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="4cbfc-118">Stop</span></span>
- <span data-ttu-id="4cbfc-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="4cbfc-119">Suspend</span></span>

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

### <span data-ttu-id="4cbfc-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4cbfc-120">-InformationVariable</span></span>
<span data-ttu-id="4cbfc-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="4cbfc-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4cbfc-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="4cbfc-122">-Profile</span></span>
<span data-ttu-id="4cbfc-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cbfc-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4cbfc-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4cbfc-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4cbfc-125">-VM</span><span class="sxs-lookup"><span data-stu-id="4cbfc-125">-VM</span></span>
<span data-ttu-id="4cbfc-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4cbfc-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="4cbfc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbfc-127">CommonParameters</span></span>
<span data-ttu-id="4cbfc-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbfc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbfc-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbfc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbfc-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cbfc-130">INPUTS</span></span>

## <span data-ttu-id="4cbfc-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cbfc-131">OUTPUTS</span></span>

### <span data-ttu-id="4cbfc-132">Microsoft. platformy windowsazure. Commands. servicemanagement. IaaS. Extensions. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="4cbfc-132">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="4cbfc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cbfc-133">NOTES</span></span>

## <span data-ttu-id="4cbfc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cbfc-134">RELATED LINKS</span></span>

[<span data-ttu-id="4cbfc-135">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4cbfc-135">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="4cbfc-136">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4cbfc-136">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="4cbfc-137">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="4cbfc-137">Get-AzureVMDscExtensionStatus</span></span>](./Get-AzureVMDscExtensionStatus.md)


