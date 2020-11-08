---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054639"
---
# <span data-ttu-id="782f3-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="782f3-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="782f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="782f3-102">SYNOPSIS</span></span>
<span data-ttu-id="782f3-103">Pobiera obiekt konfiguracji ACL z maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="782f3-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="782f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="782f3-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="782f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="782f3-105">DESCRIPTION</span></span>
<span data-ttu-id="782f3-106">Polecenie cmdlet **Get-AzureAclConfig** pobiera obiekt konfiguracji listy kontroli dostępu (ACL) z istniejącej maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="782f3-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="782f3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="782f3-107">EXAMPLES</span></span>

### <span data-ttu-id="782f3-108">Przykład 1: uzyskiwanie obiektu konfiguracji ACL dla punktu końcowego maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="782f3-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="782f3-109">Pierwsze polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="782f3-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="782f3-110">Polecenie przekazuje ten obiekt do polecenia cmdlet **Get-AzureAclConfig** za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="782f3-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="782f3-111">To polecenie cmdlet pobiera konfigurację ACL dla punktu końcowego o nazwie sieć Web.</span><span class="sxs-lookup"><span data-stu-id="782f3-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="782f3-112">Polecenie zapisuje ten obiekt konfiguracji ACL w zmiennej $Acl.</span><span class="sxs-lookup"><span data-stu-id="782f3-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="782f3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="782f3-113">PARAMETERS</span></span>

### <span data-ttu-id="782f3-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="782f3-114">-EndpointName</span></span>
<span data-ttu-id="782f3-115">Określa nazwę punktu końcowego, dla którego to polecenie cmdlet pobiera listę ACL.</span><span class="sxs-lookup"><span data-stu-id="782f3-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="782f3-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="782f3-116">-InformationAction</span></span>
<span data-ttu-id="782f3-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="782f3-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="782f3-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="782f3-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="782f3-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="782f3-119">Continue</span></span>
- <span data-ttu-id="782f3-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="782f3-120">Ignore</span></span>
- <span data-ttu-id="782f3-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="782f3-121">Inquire</span></span>
- <span data-ttu-id="782f3-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="782f3-122">SilentlyContinue</span></span>
- <span data-ttu-id="782f3-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="782f3-123">Stop</span></span>
- <span data-ttu-id="782f3-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="782f3-124">Suspend</span></span>

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

### <span data-ttu-id="782f3-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="782f3-125">-InformationVariable</span></span>
<span data-ttu-id="782f3-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="782f3-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="782f3-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="782f3-127">-Profile</span></span>
<span data-ttu-id="782f3-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="782f3-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="782f3-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="782f3-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="782f3-130">-VM</span><span class="sxs-lookup"><span data-stu-id="782f3-130">-VM</span></span>
<span data-ttu-id="782f3-131">Określa obiekt maszyny wirtualnej, dla którego ten aplet polecenia Pobiera konfigurację ACL.</span><span class="sxs-lookup"><span data-stu-id="782f3-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

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

### <span data-ttu-id="782f3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782f3-132">CommonParameters</span></span>
<span data-ttu-id="782f3-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="782f3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782f3-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="782f3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782f3-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="782f3-135">INPUTS</span></span>

## <span data-ttu-id="782f3-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="782f3-136">OUTPUTS</span></span>

## <span data-ttu-id="782f3-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="782f3-137">NOTES</span></span>

## <span data-ttu-id="782f3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="782f3-138">RELATED LINKS</span></span>

[<span data-ttu-id="782f3-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="782f3-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="782f3-140">Nowe — AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="782f3-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="782f3-141">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="782f3-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="782f3-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="782f3-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


