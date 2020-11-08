---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055471"
---
# <span data-ttu-id="46eab-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="46eab-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="46eab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46eab-102">SYNOPSIS</span></span>
<span data-ttu-id="46eab-103">Pobiera identyfikator URI do odbiornika https https na maszynie wirtualnej lub listę maszyn wirtualnych w hostowanej usłudze.</span><span class="sxs-lookup"><span data-stu-id="46eab-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="46eab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46eab-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="46eab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46eab-105">DESCRIPTION</span></span>
<span data-ttu-id="46eab-106">Polecenie cmdlet **Get-AzureWinRMUri** Pobiera identyfikator URI odbiornika https funkcji Windows Remote Management (WinRM) na maszynę wirtualną lub listę maszyn wirtualnych w hostowanej usłudze.</span><span class="sxs-lookup"><span data-stu-id="46eab-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="46eab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46eab-107">EXAMPLES</span></span>

### <span data-ttu-id="46eab-108">Przykład 1. Uzyskaj identyfikator URI odbiornika https usługi WinRM na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="46eab-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="46eab-109">To polecenie pobiera UIRa odbiornika https usługi WinRM do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="46eab-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="46eab-110">Przykład 2: uzyskiwanie identyfikatora URI odbiornika https usługi WinRM na maszynie wirtualnej określonej usługi</span><span class="sxs-lookup"><span data-stu-id="46eab-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="46eab-111">To polecenie pobiera UIRa odbiornika https usługi WinRM do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="46eab-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="46eab-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46eab-112">PARAMETERS</span></span>

### <span data-ttu-id="46eab-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="46eab-113">-InformationAction</span></span>
<span data-ttu-id="46eab-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="46eab-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="46eab-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="46eab-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46eab-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="46eab-116">Continue</span></span>
- <span data-ttu-id="46eab-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="46eab-117">Ignore</span></span>
- <span data-ttu-id="46eab-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="46eab-118">Inquire</span></span>
- <span data-ttu-id="46eab-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="46eab-119">SilentlyContinue</span></span>
- <span data-ttu-id="46eab-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="46eab-120">Stop</span></span>
- <span data-ttu-id="46eab-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="46eab-121">Suspend</span></span>

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

### <span data-ttu-id="46eab-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="46eab-122">-InformationVariable</span></span>
<span data-ttu-id="46eab-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="46eab-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="46eab-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46eab-124">-Name</span></span>
<span data-ttu-id="46eab-125">Określa nazwę maszyny wirtualnej, do której jest generowany identyfikator URI usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="46eab-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46eab-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="46eab-126">-Profile</span></span>
<span data-ttu-id="46eab-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46eab-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46eab-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="46eab-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46eab-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="46eab-129">-ServiceName</span></span>
<span data-ttu-id="46eab-130">Określa nazwę usługi Microsoft Azure, która obsługuje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="46eab-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46eab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46eab-131">CommonParameters</span></span>
<span data-ttu-id="46eab-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46eab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46eab-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46eab-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46eab-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46eab-134">INPUTS</span></span>

## <span data-ttu-id="46eab-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46eab-135">OUTPUTS</span></span>

## <span data-ttu-id="46eab-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46eab-136">NOTES</span></span>

## <span data-ttu-id="46eab-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46eab-137">RELATED LINKS</span></span>

[<span data-ttu-id="46eab-138">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="46eab-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="46eab-139">Nowe — AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="46eab-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


