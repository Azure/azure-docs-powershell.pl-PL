---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525262"
---
# <span data-ttu-id="aa2fb-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="aa2fb-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="aa2fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2fb-103">Sprawdza konfigurację rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa2fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa2fb-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## <span data-ttu-id="aa2fb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa2fb-105">DESCRIPTION</span></span>
<span data-ttu-id="aa2fb-106">Polecenie cmdlet **test-AzureRmVMAEMExtension** sprawdza konfigurację rozszerzenia usługi Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="aa2fb-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="aa2fb-107">Rozszerzenie AEM gromadzi dane dotyczące wydajności.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="aa2fb-108">To polecenie cmdlet sprawdza, czy dane wydajności są dostępne.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="aa2fb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa2fb-109">EXAMPLES</span></span>

### <span data-ttu-id="aa2fb-110">Przykład 1: Sprawdzanie konfiguracji rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="aa2fb-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="aa2fb-111">To polecenie sprawdza konfigurację rozszerzenia AEM dla maszyny wirtualnej o nazwie contoso — Server.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="aa2fb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa2fb-112">PARAMETERS</span></span>

### <span data-ttu-id="aa2fb-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="aa2fb-113">-OSType</span></span>
<span data-ttu-id="aa2fb-114">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="aa2fb-115">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="aa2fb-116">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa2fb-118">Określa nazwę grupy zasobów maszyny wirtualnej, którą to polecenie cmdlet sprawdza.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-118">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="aa2fb-119">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="aa2fb-119">-SkipStorageCheck</span></span>
<span data-ttu-id="aa2fb-120">Wskazuje, że to polecenie cmdlet pomija Sprawdzanie konfiguracji magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-120">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2fb-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="aa2fb-121">-VMName</span></span>
<span data-ttu-id="aa2fb-122">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="aa2fb-123">To polecenie cmdlet testuje rozszerzenie AEM dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-123">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="aa2fb-124">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="aa2fb-124">-WaitTimeInMinutes</span></span>
<span data-ttu-id="aa2fb-125">Określa limit czasu (w minutach) sprawdzania konfiguracji magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-125">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2fb-126">CommonParameters</span></span>
<span data-ttu-id="aa2fb-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2fb-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa2fb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2fb-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa2fb-129">INPUTS</span></span>

### <span data-ttu-id="aa2fb-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aa2fb-130">None</span></span>
<span data-ttu-id="aa2fb-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa2fb-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa2fb-132">OUTPUTS</span></span>

## <span data-ttu-id="aa2fb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa2fb-133">NOTES</span></span>

## <span data-ttu-id="aa2fb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa2fb-134">RELATED LINKS</span></span>

[<span data-ttu-id="aa2fb-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="aa2fb-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="aa2fb-136">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="aa2fb-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="aa2fb-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="aa2fb-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


