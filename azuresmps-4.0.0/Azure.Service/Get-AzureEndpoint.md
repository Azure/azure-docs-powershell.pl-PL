---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054611"
---
# <span data-ttu-id="53ed3-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="53ed3-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="53ed3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="53ed3-103">Pobiera informacje o punktach końcowych przypisanych do maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53ed3-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="53ed3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53ed3-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="53ed3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="53ed3-106">Polecenie cmdlet **Get-AzureEndpoint** pobiera informacje o punktach końcowych przypisanych do maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53ed3-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="53ed3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53ed3-107">EXAMPLES</span></span>

### <span data-ttu-id="53ed3-108">Przykład 1: uzyskiwanie informacji o punkcie końcowym dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="53ed3-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="53ed3-109">To polecenie pobiera konfigurację maszyny wirtualnej o nazwie VirtualMachine12 przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="53ed3-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="53ed3-110">Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="53ed3-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="53ed3-111">To polecenie cmdlet umożliwia pobieranie informacji o punkcie końcowym dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="53ed3-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="53ed3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53ed3-112">PARAMETERS</span></span>

### <span data-ttu-id="53ed3-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="53ed3-113">-InformationAction</span></span>
<span data-ttu-id="53ed3-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="53ed3-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="53ed3-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="53ed3-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53ed3-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="53ed3-116">Continue</span></span>
- <span data-ttu-id="53ed3-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="53ed3-117">Ignore</span></span>
- <span data-ttu-id="53ed3-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="53ed3-118">Inquire</span></span>
- <span data-ttu-id="53ed3-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="53ed3-119">SilentlyContinue</span></span>
- <span data-ttu-id="53ed3-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="53ed3-120">Stop</span></span>
- <span data-ttu-id="53ed3-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="53ed3-121">Suspend</span></span>

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

### <span data-ttu-id="53ed3-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="53ed3-122">-InformationVariable</span></span>
<span data-ttu-id="53ed3-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="53ed3-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="53ed3-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53ed3-124">-Name</span></span>
<span data-ttu-id="53ed3-125">Określa nazwę punktu końcowego, dla którego to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="53ed3-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="53ed3-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="53ed3-126">-Profile</span></span>
<span data-ttu-id="53ed3-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53ed3-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53ed3-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="53ed3-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53ed3-129">-VM</span><span class="sxs-lookup"><span data-stu-id="53ed3-129">-VM</span></span>
<span data-ttu-id="53ed3-130">Umożliwia określenie maszyny wirtualnej, z poziomu której to polecenie cmdlet uzyskuje informacje o punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="53ed3-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

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

### <span data-ttu-id="53ed3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ed3-131">CommonParameters</span></span>
<span data-ttu-id="53ed3-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ed3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ed3-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ed3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ed3-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53ed3-134">INPUTS</span></span>

## <span data-ttu-id="53ed3-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53ed3-135">OUTPUTS</span></span>

## <span data-ttu-id="53ed3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53ed3-136">NOTES</span></span>

## <span data-ttu-id="53ed3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53ed3-137">RELATED LINKS</span></span>

[<span data-ttu-id="53ed3-138">Dodaj-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="53ed3-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="53ed3-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="53ed3-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="53ed3-140">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="53ed3-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="53ed3-141">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="53ed3-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)


