---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718952"
---
# <span data-ttu-id="d4faf-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4faf-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="d4faf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4faf-102">SYNOPSIS</span></span>
<span data-ttu-id="d4faf-103">Pobiera informacje o rozszerzeniu AEM.</span><span class="sxs-lookup"><span data-stu-id="d4faf-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4faf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4faf-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="d4faf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d4faf-105">DESCRIPTION</span></span>
<span data-ttu-id="d4faf-106">Polecenie cmdlet **Get-AzureRmVMAEMExtension** pobiera informacje o rozszerzeniu usługi Azure enhanceing Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="d4faf-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="d4faf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4faf-107">EXAMPLES</span></span>

### <span data-ttu-id="d4faf-108">Przykład 1: uzyskiwanie rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="d4faf-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="d4faf-109">To polecenie pobiera informacje o rozszerzeniu AEM dla maszyny wirtualnej o nazwie contoso — Server.</span><span class="sxs-lookup"><span data-stu-id="d4faf-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="d4faf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4faf-110">PARAMETERS</span></span>

### <span data-ttu-id="d4faf-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4faf-111">-Name</span></span>
<span data-ttu-id="d4faf-112">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d4faf-112">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d4faf-113">To polecenie cmdlet umożliwia pobieranie informacji dotyczących rozszerzenia AEM na maszynie wirtualnej, którą to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="d4faf-113">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4faf-114">-OSType</span><span class="sxs-lookup"><span data-stu-id="d4faf-114">-OSType</span></span>
<span data-ttu-id="d4faf-115">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="d4faf-115">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="d4faf-116">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d4faf-116">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="d4faf-117">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="d4faf-117">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4faf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4faf-118">-ResourceGroupName</span></span>
<span data-ttu-id="d4faf-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d4faf-119">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="d4faf-120">To polecenie cmdlet umożliwia pobieranie informacji dotyczących rozszerzenia AEM na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d4faf-120">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="d4faf-121">-Status</span><span class="sxs-lookup"><span data-stu-id="d4faf-121">-Status</span></span>
<span data-ttu-id="d4faf-122">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="d4faf-122">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4faf-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="d4faf-123">-VMName</span></span>
<span data-ttu-id="d4faf-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d4faf-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d4faf-125">To polecenie cmdlet umożliwia pobieranie informacji o rozszerzeniu AEM dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d4faf-125">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4faf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4faf-126">CommonParameters</span></span>
<span data-ttu-id="d4faf-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4faf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4faf-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4faf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4faf-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4faf-129">INPUTS</span></span>

### <span data-ttu-id="d4faf-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d4faf-130">None</span></span>
<span data-ttu-id="d4faf-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d4faf-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4faf-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4faf-132">OUTPUTS</span></span>

## <span data-ttu-id="d4faf-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4faf-133">NOTES</span></span>

## <span data-ttu-id="d4faf-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4faf-134">RELATED LINKS</span></span>

[<span data-ttu-id="d4faf-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4faf-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="d4faf-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4faf-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="d4faf-137">Test — AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4faf-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


