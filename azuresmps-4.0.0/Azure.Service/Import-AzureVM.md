---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055221"
---
# <span data-ttu-id="35b95-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="35b95-101">Import-AzureVM</span></span>

## <span data-ttu-id="35b95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35b95-102">SYNOPSIS</span></span>
<span data-ttu-id="35b95-103">Importuje stan maszyny wirtualnej platformy Azure z pliku.</span><span class="sxs-lookup"><span data-stu-id="35b95-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="35b95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35b95-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="35b95-105">Opis</span><span class="sxs-lookup"><span data-stu-id="35b95-105">DESCRIPTION</span></span>
<span data-ttu-id="35b95-106">Polecenie cmdlet **Import-AzureVM** importuje wcześniej zapisany stan maszyny wirtualnej z pliku XML.</span><span class="sxs-lookup"><span data-stu-id="35b95-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="35b95-107">To polecenie cmdlet jest przydatne, gdy chcesz później utworzyć maszynę wirtualną na podstawie zaimportowanych danych.</span><span class="sxs-lookup"><span data-stu-id="35b95-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="35b95-108">Uruchomienie programu **Export-AzureVM** , a następnie polecenie **Remove-AzureVM** , a następnie polecenie **Import-AzureVM** w celu ponownego utworzenia maszyny wirtualnej może spowodować, że wynikowy komputer wirtualny będzie miał inny adres IP niż oryginalny.</span><span class="sxs-lookup"><span data-stu-id="35b95-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="35b95-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35b95-109">EXAMPLES</span></span>

### <span data-ttu-id="35b95-110">Przykład 1: Importowanie stanu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="35b95-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="35b95-111">To polecenie umożliwia zaimportowanie stanu maszyny wirtualnej z pliku VMstate.xml, a następnie utworzenie maszyny wirtualnej w określonej usłudze chmury.</span><span class="sxs-lookup"><span data-stu-id="35b95-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="35b95-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35b95-112">PARAMETERS</span></span>

### <span data-ttu-id="35b95-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="35b95-113">-InformationAction</span></span>
<span data-ttu-id="35b95-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="35b95-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="35b95-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="35b95-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35b95-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="35b95-116">Continue</span></span>
- <span data-ttu-id="35b95-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="35b95-117">Ignore</span></span>
- <span data-ttu-id="35b95-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="35b95-118">Inquire</span></span>
- <span data-ttu-id="35b95-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="35b95-119">SilentlyContinue</span></span>
- <span data-ttu-id="35b95-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="35b95-120">Stop</span></span>
- <span data-ttu-id="35b95-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="35b95-121">Suspend</span></span>

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

### <span data-ttu-id="35b95-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="35b95-122">-InformationVariable</span></span>
<span data-ttu-id="35b95-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="35b95-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="35b95-124">-Path</span><span class="sxs-lookup"><span data-stu-id="35b95-124">-Path</span></span>
<span data-ttu-id="35b95-125">Określa ścieżkę pliku z wcześniej zapisanym stanem maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35b95-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b95-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b95-126">CommonParameters</span></span>
<span data-ttu-id="35b95-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b95-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b95-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35b95-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b95-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35b95-129">INPUTS</span></span>

## <span data-ttu-id="35b95-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35b95-130">OUTPUTS</span></span>

## <span data-ttu-id="35b95-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35b95-131">NOTES</span></span>

## <span data-ttu-id="35b95-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35b95-132">RELATED LINKS</span></span>

[<span data-ttu-id="35b95-133">Eksportowanie — AzureVM</span><span class="sxs-lookup"><span data-stu-id="35b95-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="35b95-134">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="35b95-134">New-AzureVM</span></span>](./New-AzureVM.md)


